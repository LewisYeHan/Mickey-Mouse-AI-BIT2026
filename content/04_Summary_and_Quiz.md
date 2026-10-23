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

## 1. Visual Summary: The Software Architecture Hierarchy

```mermaid
classDiagram
    class Root["COMPUTER SOFTWARE ARCHITECTURE"] {
        + 1.1 Kernel Layer(Hardware Control)
        + 1.2 System Layer(OS & Drivers)
        + 1.3 Application Layer(User Tasks)
    }

    class App_1_3["1.3 APPLICATION SOFTWARE"] {
        +Types: Word, Web, Graphics
        +Architecture: Native vs Electron
        +Lifecycle: SSD -> RAM -> Syscall
        +License: Open Source vs Proprietary
    }

    class Sys_1_2["1.2 SYSTEM SOFTWARE"] {
        +Firmware: BIOS/UEFI -> Bootloader
        +Kernel: Monolithic, Micro, Hybrid
        +Translators: Compiler vs Interpreter
        +Utilities and Drivers
    }

    class OS_1_1["1.1 OPERATING SYSTEM"] {
        +OS Types
        +Process Management
        +Memory Management
        +Interface & IO
    }

    class OS_Types["1.1.1 OS_Types"] {
        +Batch
        +Time-sharing
        +Real-time
        +Embedded
    }

    class Process_Mgmt["1.1.2 Process_Management"] {
        +States: New->Ready->Running
        +Scheduling: FCFS, SJF, RR
        +Issues: Deadlock, Aging
    }

    class Memory_Mgmt["1.1.3 Memory_Management"] {
        +RAM vs Storage
        +Paging / Virtual Memory
        +Thrashing (Swap)
    }

    class Interface_IO["1.1.4 Interface_IO"] {
        +CLI vs GUI
        +Syscall (User/Kernel)
        +DMA / Spooling
    }

    Root *-- App_1_3
    Root *-- Sys_1_2
    Root *-- OS_1_1

    OS_1_1 *-- OS_Types
    OS_1_1 *-- Process_Mgmt
    OS_1_1 *-- Memory_Mgmt
    OS_1_1 *-- Interface_IO
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
