# 1.3 Application Software & Execution Lifecycle

**Status:** Completed  
**Team Member:** Lu My Ky (`@jojolu11`)  

---

## 1. What is application software?
* **Application software** = end-user programs for specific tasks (Word, Excel, Figma, Chrome) that run on top of the OS

### 8 categories
1. Word processing
2. Spreadsheet
3. Presentation
4. Multimedia
5. Web browsers
6. Educational
7. Graphics
8. Simulation

### Key ideas
* **User space** — where apps run · restricted sandbox · no direct hardware access
* **Kernel space** — where the OS kernel runs · full hardware access
* **System call (syscall)** — the controlled doorway an app uses to ask the kernel for hardware actions (save a file, send data)

---

## 2. The execution lifecycle

```text
[ 1. Executable on SSD ]
           |
           v
[ 2. OS loader creates a process in RAM ]
           |
           v
[ 3. CPU executes instructions (threads) ] <---+ (result back)
           |                                   |
           v                                   |
[ 4. App requests hardware via syscall ]       |
           |                                   |
           v                                   |
[ 5. Kernel performs the action safely ] ------+
     and returns the result
