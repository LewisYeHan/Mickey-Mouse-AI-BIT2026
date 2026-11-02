# 1.3 Application Software

**Status:** ✅  
**Team Member:** Lu My Ky (`@jojolu11`)

**In this section:** What is Application Software · The Execution Lifecycle · Types of Applications · How Apps Are Built · Practice Questions

---

## 1. What is Application Software?
In [1.2 System Software](02_System_Software.md), we compared a computer to a restaurant: the hardware is the kitchen, and system software is the kitchen staff. **Application software** is the food you actually ordered. It is the reason you use the computer at all.

An **application** (or **app**) is a program made to help a person do a specific task: writing an essay in Word, editing a photo in Photoshop, or watching a video in Chrome. Apps run **on top of** the operating system. They do not control the hardware themselves; they ask the OS to do that for them.

The simplest way to tell the two kinds of software apart is to ask *who it works for*:
* **Application software** works for **you**. You open it on purpose to get something done.
* **System software** works for **the computer**. It runs in the background so that apps can work.

### Where Apps Live: User Space
Every app runs in a protected area of memory called **user space**. From there it cannot directly control devices, reach other programs' memory, or change protected CPU settings. Only the kernel, which runs in **kernel space**, has full access to the hardware. When an app needs something from the hardware, such as saving a file, it has to ask the kernel through a **system call**. (User mode, kernel mode, and system calls are explained in detail in [1.1 §7](01_Operating_Systems.md#7-system-calls).)

---

## 2. What Happens When You Open an App
Double-clicking an icon feels instant, but behind the scenes the app goes through five steps (Arpaci-Dusseau & Arpaci-Dusseau, 2018). Let's follow what happens when you open Google Chrome.

![Application execution lifecycle](../images/execution_lifecycle.png)
*Figure 1.5: The 5 steps of running an app, from a file on the SSD to the kernel sending back a result.*

Figure 1.5 shows the five steps from top to bottom. The dashed arrow on the right is the loop: after the kernel sends back a result, the app goes back to running its instructions in Step 3.

### Step 1: The program file sits on the SSD
Before you click, Chrome is just a file on your drive (`chrome.exe` on Windows). It contains machine code and data, but it is not doing anything. It is like a recipe in a closed cookbook.

### Step 2: The OS loader turns it into a process in RAM
When you click the icon, a part of the OS called the **loader** copies the program from the SSD into RAM, because RAM is far faster for the CPU to read. The OS then creates a **process** (the running copy of the program) and a **Process Control Block (PCB)** to keep track of it.

The OS also gives the process its own memory, divided into four areas:
* **Code:** the program's instructions.
* **Data:** values that exist for the whole time the program runs.
* **Stack:** short-term memory for the function calls in progress (their local variables and where to return to). It grows and shrinks as functions start and finish.
* **Heap:** memory the program asks for while it runs, for example when you open a large photo.

### Step 3: The CPU runs the instructions
The OS scheduler gives the process a turn on the CPU. The CPU then repeats the same three-step cycle billions of times per second:
1. **Fetch** the next instruction from memory.
2. **Decode** it to work out what it means.
3. **Execute** it.

Inside the process, **threads** do the actual work. Chrome, for example, can use one thread to draw the page and another to download an image at the same time.

### Step 4: The app asks for hardware with a system call
Sooner or later the app needs the hardware. It might need to save a file, show a picture, or load a web page. Because it runs in user space, it cannot do this itself. Instead, it makes a **system call**, such as `open()` to open a file, `write()` to save one, or `socket()` to use the network. At this moment the CPU switches from **user mode** into **kernel mode**.

### Step 5: The kernel does the work safely and returns the result
The kernel first checks that the app is allowed to make the request. For example, is this app allowed to write to this folder? It then uses the right **device driver** to do the hardware work, sends the result back to the app, and switches the CPU back to user mode. The app continues from Step 3, and the loop repeats until you close it.

### Why Computers Work This Way
This might seem like a lot of steps just to save a file, but it gives three big benefits (Silberschatz et al., 2018):
* **Safety:** A buggy or harmful app cannot damage the hardware or read another app's memory, because each app has its own private memory space and the kernel checks every hardware request.
* **Sharing:** Many apps can use the same CPU, RAM, and devices at once, because the OS decides who gets what.
* **Simplicity for developers:** App makers do not need to write code for every printer or graphics card in the world. They ask the OS, and the drivers handle the details.

---

## 3. Types of Application Software
There are thousands of apps, but most of them fit into a few groups based on the job they help you do (Silberschatz et al., 2018):

| Type | What it helps you do | Examples |
| :--- | :--- | :--- |
| **Word processing** | Write and format text documents | Microsoft Word, Google Docs, Apple Pages |
| **Spreadsheet** | Organize numbers in rows and columns and calculate with formulas | Microsoft Excel, Google Sheets, Apple Numbers |
| **Presentation** | Build slides for talks and lectures | PowerPoint, Google Slides, Keynote |
| **Multimedia** | Create, edit, and play audio and video | DaVinci Resolve, Audacity, VLC Media Player |
| **Web browser** | Open websites and web apps | Chrome, Firefox, Edge, Safari |
| **Educational** | Learn new skills and track progress | Duolingo, Khan Academy, Moodle |
| **Graphics** | Edit photos, draw, and design in 2D or 3D | Photoshop, Illustrator, Figma, Blender |
| **Simulation** | Model real situations to test them safely | MATLAB/Simulink, Microsoft Flight Simulator |

A few things to notice:
* **The type depends on the job, not the company.** Microsoft makes Word (word processing) and Excel (spreadsheet) and publishes Flight Simulator (simulation): three different types from one company.
* **Some apps fit more than one type.** Canva can make presentations *and* graphics. Blender is used for 3D graphics *and* animation.
* **Simulation software is used where real tests are expensive or dangerous.** Pilots train in flight simulators before flying a real plane, and engineers test a bridge design in software before building it.

---

## 4. How Apps Are Built: Native vs. Web vs. Cross-Platform
The same kind of app can be built in very different ways, and the choice affects how fast it runs, how much memory it uses, and which devices it works on.

### Native Apps
A **native app** is written for one specific operating system, usually in that platform's main language: **Swift** for iPhone and Mac, **C++ or C#** for Windows, and **Kotlin** for Android. It is built to fit that one OS, and in most cases it is turned into code the CPU can run directly.
* **Pros:** It is usually the fastest option, uses the least memory, and has full access to the device's features (camera, GPU, sensors) through the OS.
* **Cons:** It only works on one OS. To support Windows, macOS, Android, and iPhone, the company must build and maintain four separate versions.
* **Examples:** Microsoft Word on Windows, Final Cut Pro on Mac.

### Web Apps
A **web app** runs inside a web browser and is built with **HTML, CSS, and JavaScript**. There is nothing to install: you just open a link.
* **Pros:** It works on any device that has a browser, and everyone always has the latest version, because the app lives on the server.
* **Cons:** It usually needs an internet connection, has limited access to the hardware, and often runs slower than a native app because the browser sits in between.
* **Examples:** Google Docs, Canva, Figma in the browser.

### Cross-Platform Apps
A **cross-platform app** is written once and then runs on several operating systems. The two most common approaches work quite differently (Electron, n.d.; Flutter, n.d.).

**Electron (desktop)**
* Packs a web app together with its own copy of the Chrome browser engine (Chromium) and Node.js, so it can be installed like a normal desktop app.
* **Pros:** One codebase runs on Windows, macOS, and Linux, which saves a lot of time and money.
* **Cons:** Heavy. Every Electron app carries its own browser engine, so having Discord, Slack, and VS Code open is a bit like running three extra copies of Chrome.
* **Examples:** VS Code, Discord, Slack, Obsidian.

**Flutter and React Native (mainly mobile)**
* Let one codebase build apps for both Android and iPhone, without carrying a whole browser engine.
* **Pros:** One codebase for two platforms, and usually much closer to native speed than Electron.
* **Cons:** Brand-new phone features can take extra work to use, because the framework has to support them first.
* **Examples:** Google Pay (Flutter); parts of the Instagram and Facebook apps (React Native).

### Comparison

| Feature | Native | Web | Electron | Flutter / React Native |
| :--- | :--- | :--- | :--- | :--- |
| **Works on** | One OS | Any device with a browser | Windows, macOS, Linux | Android and iPhone |
| **Layers to the OS** | App → OS | App → browser → OS | App → its own Chromium → OS | App → framework → OS |
| **Speed** | Usually fastest | Usually slowest | In between | Close to native |
| **Memory use** | Lowest | Shares the browser you already have open | Highest (each app has its own engine) | Low to medium |
| **Hardware access** | Full (via OS APIs) | Limited | Good | Good |
| **Install needed?** | Yes | No | Yes | Yes |

**The main trade-off:** the more devices an app can run on from one codebase, the more layers sit between it and the hardware (see the "Layers to the OS" row), so it usually gets slower and heavier. The more native it is, the faster it runs, but the more work it takes to support every platform. Companies choose based on what matters most to them. A video editor needs speed, so it is usually native. A chat app needs to be everywhere quickly, so it often uses Electron.

---

## 5. Practice Questions and Answers
Try answering each question yourself first, then read the answer.

**Questions**
1. What is the simplest way to tell application software apart from system software?
2. You save a document in Word. At that moment, which step of the lifecycle is happening, and what does the CPU switch into?
3. Your app loads a large photo and asks for more memory while it is running. Which part of the process's memory does that come from: code, data, stack, or heap?
4. A music app wants to save a song to your drive. Why can't it just write to the SSD itself, and what does it do instead?
5. What is the difference between a process and a thread?
6. Which type of application is each of these: Duolingo, Excel, Blender, Microsoft Flight Simulator?
7. A small team wants its new app on Windows, macOS, and Linux as fast as possible, and does not mind if it uses more memory. Which way of building it fits best, and why?
8. Why do Discord and VS Code use more RAM than a similar native app?

**Answers**
1. Ask who it works for. Application software works for you and does a task you chose. System software works for the computer and runs in the background so apps can work.
2. **Step 4**, a system call (such as `write()`). The CPU switches from user mode into **kernel mode**; then in Step 5 the kernel saves the file and switches back to user mode.
3. The **heap**, which holds memory that the program asks for while it is running.
4. It runs in **user space**, which has no direct access to the hardware, for safety. It makes a **system call** such as `write()`, and the kernel checks the request and saves the file using the right driver.
5. A **process** is a running program with its own memory. A **thread** is a worker inside a process; all the threads of one process share that process's memory.
6. Duolingo: educational. Excel: spreadsheet. Blender: graphics. Microsoft Flight Simulator: simulation.
7. A **cross-platform app with Electron**. One codebase runs on all three systems, which saves time, and the team has accepted the extra memory use.
8. They are built with **Electron**, so each one carries its own copy of the Chromium browser engine, which takes up a lot of RAM.

---

## 6. References
1. Arpaci-Dusseau, R. H., & Arpaci-Dusseau, A. C. (2018). *Operating Systems: Three Easy Pieces*. Arpaci-Dusseau Books.
2. Electron. (n.d.). *Electron documentation*. https://www.electronjs.org/docs
3. Flutter. (n.d.). *Flutter documentation*. https://docs.flutter.dev
4. Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). *Operating System Concepts* (10th ed.). Wiley.
5. BIT2026 Course Lecture Slides (Application Software Module).
