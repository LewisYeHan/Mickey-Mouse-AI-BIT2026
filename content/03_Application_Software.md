# 1.3 Application Software

**Status:** ✅  
**Team Member:** Lu My Ky (`@jojolu11`)

**In this section:** What is Application Software · Execution Lifecycle · Types · How Apps Are Built · Review Questions

---

## 1. What is Application Software?
**Application software** is a program made for a specific user task (such as Microsoft Word, Excel, Figma, or Google Chrome). It runs on top of the Operating System. The 8 main types are explained in [Section 3](#3-types-of-application-software).

### Key Ideas
* **User space:** Where applications run. It is a restricted area with **no direct hardware access**.
* **Kernel space:** Where the OS kernel runs, with **full access** to the CPU, RAM, and devices.
* **System call (syscall):** The controlled doorway an app uses to ask the kernel to do hardware work (such as saving a file or sending data over the network).

---

## 2. The Execution Lifecycle
What actually happens when you open an app, in 5 steps:

![Application execution lifecycle](images/execution_lifecycle.png)
*Figure 1.5: The 5 steps of running an app, from a file on the SSD to the kernel sending back a result.*

#### 1. Program file on the SSD
* The app is stored as a file on disk (e.g., `chrome.exe`).
* It contains compiled machine code and data, but it is not running yet.

#### 2. OS loader makes a process in RAM
* The loader copies the program from the SSD into RAM, which is much faster.
* It creates a **process** and its **PCB (Process Control Block)**, which stores the process ID, state, and priority.
* The process gets its own memory areas: **code, data, stack, and heap**.

#### 3. CPU runs the instructions (threads)
* The OS scheduler gives the process a turn on the CPU.
* The CPU repeats the instruction cycle: **fetch → decode → execute**.
* **Threads** inside the process do the actual work and share the process's memory.

#### 4. App asks for hardware: system call
* The app runs in **user space**, so it cannot touch hardware directly.
* Instead, it makes a **system call**, such as `read()`, `write()`, or `socket()`.
* The CPU switches from user mode into **kernel mode**.

#### 5. Kernel does it safely and sends the result
* The kernel checks that the app is allowed to make the request.
* It uses the right **device driver** to reach the hardware.
* It sends the result back to the app and switches the CPU back to **user mode**, so step 3 continues.

### Why Computers Work This Way
* **Safety:** One buggy app cannot damage the hardware or mess up other running apps.
* **Sharing:** Many apps can share the same CPU, RAM, and devices at once.
* **Simplicity:** App developers do not need to write code for every hardware model, because the OS and drivers handle that.

---

## 3. Types of Application Software

### 1. Word processing
* Create and edit text documents with formatting.
* Features: spell check, tables, templates, track changes.
* **Examples:** Microsoft Word, Google Docs, Apple Pages, LibreOffice Writer.

### 2. Spreadsheet
* Organize numbers and data in rows and columns.
* Features: formulas, charts, pivot tables, data analysis.
* **Examples:** Microsoft Excel, Google Sheets, Apple Numbers, LibreOffice Calc.

### 3. Presentation
* Build slide decks for talks, lectures, and pitches.
* Features: slide layouts, animations, transitions, speaker notes.
* **Examples:** Microsoft PowerPoint, Google Slides, Apple Keynote, Canva.

### 4. Multimedia
* Create, edit, and play audio, video, and AR/VR content.
* Features: timeline editing, visual effects, sound mixing.
* **Examples:** Adobe Premiere Pro, DaVinci Resolve, Audacity, VLC Media Player, Unity (AR/VR).

### 5. Web browsers
* Open and use websites and web apps.
* Features: tabs, extensions, sandboxing, built-in security.
* **Examples:** Google Chrome, Mozilla Firefox, Microsoft Edge, Safari, Brave.

### 6. Educational
* Help people learn new skills.
* Features: quizzes, progress tracking, virtual classrooms.
* **Examples:** Duolingo, Khan Academy, Google Classroom, Moodle, Kahoot!

### 7. Graphics
* 2D design, photo editing, and 3D modeling.
* Features: photo editing, vector art, UI/UX design.
* **Examples:** Adobe Photoshop, Adobe Illustrator, CorelDRAW, Blender, Figma.

### 8. Simulation
* Model real-world situations for training, testing, or engineering.
* Features: safe virtual testing without real-world risk.
* **Examples:** MATLAB/Simulink, Microsoft Flight Simulator, Arena Simulation, AnyLogic, SimScale.

---

## 4. How Apps Are Built: Native vs. Web vs. Cross-Platform

### Native apps
* Written for one specific OS in its own language (**Swift** for iOS/macOS, **C++/C#** for Windows, **Kotlin** for Android).
* Compiled into machine code, so they talk to the OS directly.
* **Pros:** Fastest, uses the least memory, full hardware access.
* **Cons:** You need a separate version for every OS.
* **Examples:** Microsoft Word, Adobe Photoshop, Final Cut Pro.

### Web apps
* Run inside a web browser using **HTML, CSS, and JavaScript**.
* Nothing to install: you just open a URL.
* **Pros:** Works on any device with a browser and is always up to date.
* **Cons:** Usually needs internet, limited hardware access, slower than native.
* **Examples:** Google Docs, Figma (web), Canva.

### Cross-platform apps (Electron)
* A web app packed together with its own browser engine (**Electron** = Chromium + Node.js).
* Installed like a normal desktop app, with one codebase for every OS.
* **Pros:** Write once, run on Windows, macOS, and Linux.
* **Cons:** Heavy, because every app carries its own browser engine and uses a lot of RAM.
* **Examples:** VS Code, Discord, Slack, Microsoft Teams.

### Comparison

| Feature | Native | Web | Cross-platform (Electron) |
| :--- | :--- | :--- | :--- |
| **Portability** | Low (one OS) | Highest (any browser) | High (one codebase) |
| **Speed** | Fastest | Slowest | Medium |
| **Memory use** | Lowest | Shares the browser | Highest (own engine) |
| **Hardware access** | Full | Limited | Good |
| **Install needed** | Yes | No | Yes |

**In short:** the more portable an app is, the slower and heavier it usually gets. The more native it is, the faster it runs, but the more work it takes to support every OS.

---

## 5. Review Questions & Answers

**Q1. What is application software?**  
Programs made for specific user tasks that run on top of the OS.

**Q2. What is the difference between application and system software?**  
Application software does user tasks (Word, Chrome). System software runs and manages the computer itself (OS, drivers, BIOS).

**Q3. Why can't apps access hardware directly?**  
They run in **user space** for safety. Only the **kernel** has full hardware access.

**Q4. What is a system call? Give an example.**  
The controlled doorway from an app to the kernel, e.g., `write()` to save a file or `socket()` to send data over the network.

**Q5. List the 5 steps of the execution lifecycle.**  
(1) Program file on the SSD → (2) OS loader makes a process in RAM → (3) CPU runs the instructions → (4) App makes a system call → (5) Kernel does it safely and sends the result.

**Q6. What does the OS loader do?**  
It copies the program from the SSD into RAM, creates the process and PCB, and gives it memory (code, data, stack, heap).

**Q7. What is the difference between a process and a thread?**  
A **process** is a running program with its own memory. A **thread** is a worker inside a process that shares that memory.

**Q8. Why are VS Code and Discord heavier than native apps?**  
They are built with **Electron**, so each one carries its own Chromium browser engine, which uses more RAM.

**Q9. Native or web app: which is faster, and why?**  
**Native**, because it is compiled into machine code and talks to the OS directly, without a browser in between.

**Q10. Name 2 examples each of graphics and simulation software.**  
**Graphics:** Adobe Photoshop, Blender. **Simulation:** MATLAB/Simulink, Microsoft Flight Simulator.

---

## 6. References
1. Arpaci-Dusseau, R. H., & Arpaci-Dusseau, A. C. (2018). *Operating Systems: Three Easy Pieces*. Arpaci-Dusseau Books.
2. Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). *Operating System Concepts* (10th ed.). Wiley.
3. BIT2026 Course Lecture Slides (Application Software Module).
