# 1.4 Module Synthesis & Self-Check Quiz

**Development Status:** `checked` (Peer-Reviewed & Finalized V1.0)  
**Author:** Cao Minh Tuan (`@mnhtnc`)  

---

# 1.4 Module Synthesis & Self-Check Quiz

**Development Status:** `checked` (Peer-Reviewed & Finalized V1.0)
**Author:** Cao Minh Tuan (@mnhtnc)

---

# 1.4 Module Synthesis & Self-Check Quiz

**Development Status:** `checked` (Peer-Reviewed & Finalized V1.0)
**Author:** Cao Minh Tuan (@mnhtnc)

---

# 1.4 Module Synthesis & Self-Check Quiz

**Development Status:** `checked` (Peer-Reviewed & Finalized V1.0)
**Author:** Cao Minh Tuan (@mnhtnc)

---

## 1. Visual Sequence: Computer Software Architecture

```text
+-----------------------------------------------------------------------------------+
|                    [ 1. THE USER / APPLICATION LAYER ]                            |
|  (Apps run in User Space / Sandbox - e.g., Chrome, Word, VS Code)                 |
|  - Types: Word, Web, Graphics, Simulation                                         |
|  - Architecture: Native (Fast) vs Cross-platform (Electron - Heavy RAM)           |
|  - License: Open Source vs Proprietary                                            |
+-----------------------------------------------------------------------------------+
                                         |
                                         | (Requests hardware access via System Call)
                                         v
+-----------------------------------------------------------------------------------+
|                        [ 2. SYSTEM SOFTWARE LAYER ]                               |
|  (Bridges the gap between Apps and the Kernel)                                    |
|  - Firmware: BIOS/UEFI -> POST -> Bootloader                                      |
|  - Translators: Compiler (Whole file) vs Interpreter (Line-by-line)               |
|  - Drivers & Utilities: Translate OS commands to hardware                         |
+-----------------------------------------------------------------------------------+
                                         |
                                         | (Kernel manages and allocates resources)
                                         v
+-----------------------------------------------------------------------------------+
|                        [ 3. OPERATING SYSTEM CORE ]                               |
|  (The central manager of hardware and software resources)                         |
|  - OS Types: Batch, Time-sharing, Real-time, Distributed                          |
|  - Process Mgmt: States (New -> Ready -> Running -> Waiting -> Terminated)        |
|  - Scheduling: FCFS, SJF, Round Robin, Aging                                      |
|  - Memory Mgmt: Paging, Virtual Memory, Thrashing                                 |
|  - I/O Mgmt: DMA, Buffering, Spooling (Print queue)                               |
+-----------------------------------------------------------------------------------+
                                         |
                                         | (Direct Hardware Access)
                                         v
+-----------------------------------------------------------------------------------+
|                            [ 4. HARDWARE LAYER ]                                  |
|  (The physical foundation)                                                        |
|  - CPU, RAM, SSD/HDD, and I/O Devices                                             |
+-----------------------------------------------------------------------------------+
## 2. Comprehensive Self-Check Quiz

Test your understanding of the core concepts covered in Sections 1.1 through 1.3 by answering the questions below.

**Q1. (Multiple Choice) In an operating system, which part is considered the "brain" that directly controls the hardware?**
*   A) Shell
*   B) Kernel
*   C) Application
*   D) BIOS

**Q2. (Multiple Choice) When a computer boots up, which software runs FIRST to check the hardware (POST)?**
*   A) Windows
*   B) Chrome
*   C) BIOS/UEFI
*   D) Driver

**Q3. (Multiple Choice) Application software like Word or Chrome runs in which area for safety?**
*   A) Kernel Space
*   B) Hardware Space
*   C) User Space
*   D) BIOS Space

**Q4. (True/False) When RAM is full, the OS uses the hard drive (SSD/HDD) as temporary memory. This concept is called Virtual Memory.**
*   A) True
*   B) False

**Q5. (Multiple Choice) Which of the following applications is built with Electron and is known to consume a lot of RAM?**
*   A) Microsoft Word
*   B) VS Code
*   C) Calculator
*   D) Notepad

---
<details>
<summary><b>Click to reveal Answers</b></summary>

*   **Q1: B** (The Kernel is the core of the OS, directly controlling hardware).
*   **Q2: C** (BIOS/UEFI is the first software to run and performs POST).
*   **Q3: C** (Apps run in User Space, a restricted sandbox, for safety).
*   **Q4: A** (True. Virtual Memory uses disk space as an extension of RAM).
*   **Q5: B** (VS Code is built with Electron, bundling a full browser and consuming high RAM).

</details>
