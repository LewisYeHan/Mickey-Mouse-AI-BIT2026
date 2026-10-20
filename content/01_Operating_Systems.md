# 1.1 Operating Systems — Project Guide

**Development Status:** `checked` (Consolidated Teammate V1.0 Draft)  
**Author:** Frederick Samuel Lesmana (`@Ti4nCi`)  

---

## 1. What is an operating system?
* **Main software** that runs the computer
* Sits between **users/apps** and **hardware** (CPU, RAM, I/O)
* Shares CPU, memory, and storage between all programs
* Lets you use a computer without machine language
* **Layers:** Users $\rightarrow$ Apps $\rightarrow$ System software $\rightarrow$ OS $\rightarrow$ Hardware
* **Kernel:** core, controls hardware
* **Shell:** what you use (GUI or CLI)

### 3 Basic Functions
* Manage resources
* Provide a user interface
* Run applications (multitasking)

### CLI vs GUI
* **CLI** — type exact commands · must memorize · e.g., DOS, Linux terminal
* **GUI** — click icons on a desktop · user-friendly · e.g., Windows, macOS

---

## 2. How the OS evolved
* **Before 1940s** — no OS, machine code by hand
* **1940s–50s** — Batch: punch-card jobs run in groups
* **1950s–60s** — Multiprogramming: many programs in RAM, CPU switches when one waits
* **1960s–70s** — Time-sharing: each program gets a short CPU turn
* **1970s–80s** — GUI: icons, windows, mouse
* **1980s–90s** — Network OS: file/printer sharing (NetWare, Windows NT)
* **Late 1990s–2000s** — Mobile: iOS, Android
* **2010s–now** — AI: Siri, Google Assistant
* **Also:** personal systems (PCs), parallel systems (many CPUs in one computer)

---

## 3. Types of OS
* **Batch** — similar jobs in a row, no user input · payroll
* **Time-sharing** — short CPU turns, feels simultaneous · Windows, Linux
* **Real-time** — must respond in strict time · airbags, pacemakers
* **Distributed** — many computers act as one, no shared memory/clock · cloud
* **Network** — shares files, printers, users · Windows Server
* **Mobile** — touch, battery, wireless · Android, iOS
* **Embedded** — tiny OS for one job · smart TV, router
* **Also:** single- vs multi-user, single- vs multitasking

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

* **Open source** = anyone can read and change the code
* **Linux comes in distros** (Ubuntu, Fedora)
* **Android is built on Linux**
* **Older OSes:** DOS (MS-DOS / PC-DOS, command line), OS/2 (IBM), Unix (servers)

---

## 5. The 8 OS components
* **Process** — create/delete, suspend/resume, sync, communication
* **Main memory** — track used/free RAM, allocate, free
* **File** — create/delete, edit, map to storage, backup
* **I/O device** — drivers, buffering, caching
* **Secondary storage** — allocate space, free-space, disk scheduling
* **Security** — only authorized users/programs get access
* **Network** — share resources, speed, reliability
* **Command interpreter** — reads and runs commands
  * *Also called:* control card interpreter, command-line interpreter, shell

---

## 6. Processes and states
* **Process** = running program (Chrome: one per tab)
* **Program** = on disk · **Job** = picked to run · **Process** = running in memory
* **PCB** stores: PID, state, program counter, registers, memory, open files, priority
* **States:** New -> Ready -> Running -> Terminated
  * Running -> Waiting/Blocked — needs I/O
  * Waiting -> Ready — I/O done
  * Running -> Ready — time slot ends
  * Suspended — moved to disk
* **Hold** — job waiting to enter memory
* **Context switch** — save one process, load the next
* **Queues:**
  * Job queue — waiting to enter RAM
  * Ready queue — waiting for CPU
  * I/O queue — waiting for a device

### Process State Transition Diagram
```text
[ New ] --(admitted)---> [ Hold ] --(into RAM)---> [ Ready ] <---(I/O done)---+
                                                      |                       |
                                                   (gets CPU)               (waiting I/O)
                                                      |                       |
                                                      v                       |
                                                  [ Running ] --------+-------+
                                                      |
                                                    (done)
                                                      v
                                               [ Terminated ]
