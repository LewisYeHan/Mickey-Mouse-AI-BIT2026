# 1.1 Operating Systems

**Status:** Completed  
**Team Members:** Cao Minh Tuan (`@mnhtnc`) & Frederick Samuel Lesmana (`@Ti4nCi`)  

---

## 1. What is an operating system?
* An operating system (OS) is the main software that runs the computer.
* It sits right between users/apps and the hardware (CPU, RAM, storage).
* It shares CPU, memory, and storage fairly between all open programs.
* Without an OS, we would have to type raw machine code by hand.
* **Layers:** Users -> Apps -> System software -> OS -> Hardware.
* **Kernel:** The core part of the OS that directly controls the hardware.
* **Shell:** What the user interacts with (can be a GUI or CLI).

### 3 Basic Functions
* Manage system resources (CPU, memory, storage).
* Provide a user interface to interact with the PC.
* Run applications smoothly (multitasking).

### CLI vs GUI
* **CLI (Command Line Interface):** Type exact text commands, must memorize them (e.g., DOS, Linux terminal).
* **GUI (Graphical User Interface):** Click icons on a desktop, very user-friendly (e.g., Windows, macOS).

---

## 2. How the OS evolved
* **Before 1940s:** No OS, people wrote machine code by hand.
* **1940s–50s (Batch):** Punch-card jobs run together in groups.
* **1950s–60s (Multiprogramming):** Many programs kept in RAM; CPU switches when one waits for I/O.
* **1960s–70s (Time-sharing):** Each program gets a very short CPU turn so it feels simultaneous.
* **1970s–80s (GUI):** Introduction of icons, windows, and mice.
* **1980s–90s (Network OS):** File and printer sharing across networks (NetWare, Windows NT).
* **Late 1990s–2000s (Mobile):** Smartphones running iOS and Android.
* **2010s–now (AI):** Smart assistants like Siri and Google Assistant.

---

## 3. Types of OS
* **Batch OS:** Similar jobs run in a row with no user input (e.g., payroll processing).
* **Time-sharing OS:** Short CPU turns so multiple users feel they have the computer at once (Windows, Linux).
* **Real-time OS:** Must respond within strict time limits (e.g., car airbags, medical pacemakers).
* **Distributed OS:** Many computers act as one without sharing memory or clock (cloud systems).
* **Network OS:** Designed to share files, printers, and user accounts (Windows Server).
* **Mobile OS:** Built for touch screens, battery saving, and wireless connectivity (Android, iOS).
* **Embedded OS:** Tiny OS built into a single device for one job (smart TVs, routers).

---

## 4. Windows vs macOS vs Linux vs Android vs iOS

| Feature | Windows | macOS | Linux | Android | iOS |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Maker** | Microsoft | Apple | Community | Google | Apple |
| **Cost** | Paid | Free with Mac | Free | Free | Free with iPhone |
| **Source** | Closed | Closed | Open | Open base | Closed |
| **Kernel** | NT | XNU (Unix) | Linux | Linux | XNU |
| **Runs on** | Most PCs | Macs only | Almost anything | Many phones | Apple only |
| **Security** | Most targeted | Strong | Very strong | Good | Very strong |
| **File system**| NTFS | APFS | ext4 | ext4/F2FS | APFS |
| **Best for** | Games, office | Design, video | Servers, coding | Most phones | Apple users |

* **Open source:** Anyone can read and change the code.
* **Distros:** Linux comes in different distributions like Ubuntu and Fedora.

---

## 5. The 8 OS Components
* **Process management:** Create, delete, suspend, resume, and sync processes.
* **Main memory management:** Track used/free RAM and allocate space.
* **File management:** Create, delete, edit, and backup files.
* **I/O device management:** Handle drivers, buffering, and caching.
* **Secondary storage:** Allocate disk space and manage file scheduling.
* **Security:** Ensure only authorized users get access.
* **Network:** Share resources and handle connection reliability.
* **Command interpreter:** Read and run user commands (Shell).

---

## 6. Processes and States
* **Process:** A program currently running in memory (e.g., each Chrome tab is a process).
* **Program vs Job vs Process:** Program is on disk, Job is picked to run, Process is running in RAM.
* **PCB (Process Control Block):** Stores PID, state, program counter, registers, and priority.
* **Process States:** New -> Ready -> Running -> Terminated
  * Running -> Waiting (needs I/O)
  * Waiting -> Ready (I/O finished)
  * Running -> Ready (time slot ended)

### State Transition Diagram
```text
[ New ] ---> [ Hold ] ---> [ Ready ] <---> [ Running ] ---> [ Terminated ]
                                              |
                                              v
                                         [ Waiting ]
