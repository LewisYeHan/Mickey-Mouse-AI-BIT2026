# 1.3 Application Software — Project Guide

**Development Status:** `checked` (Consolidated Teammate V1.0 Draft)  
**Author:** Lu My Ly (`@jojolu11`)  

---

## 1. What is application software?
* **Application software** = end-user programs for specific tasks (Word, Excel, Figma, Chrome) that run **on top of the OS**

### 8 Categories
* Word processing
* Spreadsheet
* Presentation
* Multimedia
* Web browsers
* Educational
* Graphics
* Simulation

### Key Ideas
* **User space** — where apps run · restricted sandbox · no direct hardware access
* **Kernel space** — where the OS kernel runs · full hardware access
* **System call (syscall)** — the controlled doorway an app uses to ask the kernel for hardware actions (save a file, send data)

---

## 2. The execution lifecycle

### Execution Lifecycle Flowchart
```text
[ 1. Executable on SSD ]
          |
          v
[ 2. OS loader creates a process in RAM ]
          |
          v
[ 3. CPU executes instructions (threads) ] <--+ (result back)
          |                                  |
          v                                  |
[ 4. App requests hardware via syscall ] ----+
          |
          v
[ 5. Kernel performs the action safely and returns the result ]
