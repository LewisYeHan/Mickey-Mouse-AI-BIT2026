# 1.4 Module Synthesis & Self-Check Quiz

**Status:** Completed  
**Team Members:** Wong Hiu Chung Samuel (`@Samuel940398`) & Goh Ye Han (`@LewisYeHan`)  

---

## 1. Executive Module Synthesis
Stage One of our module examined how computer software is structured into three cooperative layers above the physical hardware:
<img width="7295" height="3260" alt="Concept map" src="https://github.com/user-attachments/assets/8ad71dbf-4ee0-4e35-818c-f65d4c5b745c" />

---

## 2. Self-Check Assessment Quiz

### Part A: Multiple-Choice Questions (MCQs)

**Q1. When you press the power button on a PC, what runs FIRST?**  
* A) Windows OS Kernel  
* B) Motherboard BIOS / UEFI Firmware  
* C) Web Browser  
* D) Printer Device Driver  

**Q2. In the Linux/PC boot sequence (`System Startup BIOS` → `MBR Bootloader` → `GRUB` → `Kernel Init` → `INIT` → `Run Level`), what is the primary job of GRUB?**  
* A) To edit spreadsheet formulas in user space  
* B) To act as the bootloader that locates and loads the Operating System Kernel into RAM  
* C) To permanently brick the motherboard CMOS battery  
* D) To translate Python code line by line  

**Q3. Which four conditions must ALL be present simultaneously for a process deadlock to occur?**  
* A) Mutual Exclusion, Hold and Wait, No Preemption, and Circular Wait  
* B) Paging, Segmentation, Swapping, and Thrashing  
* C) Fetch, Decode, Execute, and Store  
* D) Preprocessor, Compiler, Assembler, and Linker  

**Q4. Why do applications run in "User Space" instead of touching hardware directly?**  
* A) To isolate apps in a safe sandbox so bugs or malware cannot crash the entire computer system or overwrite other programs' memory  
* B) Because CPUs cannot execute application instructions  
* C) Because User Space is stored permanently inside the BIOS ROM chip  
* D) To bypass the CPU scheduler  

**Q5. Which system software tool combines compiled object files (`.o`) with external code libraries to produce a final `.exe` executable file?**  
* A) Spooler  
* B) Linker  
* C) POST  
* D) Command Interpreter  

**Q6. Why do cross-platform desktop apps built with Electron (such as VS Code and Discord) consume more RAM than native apps?**  
* A) Each Electron app bundles and runs its own private copy of the Chromium browser engine and Node.js  
* B) They run entirely in 16-bit Legacy BIOS mode  
* C) They are written in raw binary machine code  
* D) They cannot use virtual memory  

---

### Part B: True or False Questions

**Q7. (True / False):** *An operating system can use virtual memory on an SSD as extra simulated RAM when physical RAM runs out, but excessive swapping between RAM and disk causes a severe slowdown called "thrashing."*  

**Q8. (True / False):** *A device driver is classified as end-user application software used for word processing.*  

**Q9. (True / False):** *During the 5-step application execution lifecycle, a user-space app must make a system call (such as `write()` or `socket()`) to ask the kernel to perform hardware actions safely.*  

**Q10. (True / False):** *A compiler translates an entire C/C++ program into machine code before execution, whereas an interpreter translates and executes Python code line by line.*  

---

## 3. Complete Answer Key

| Question | Correct Answer | Explanation |
| :--- | :--- | :--- |
| **Q1** | **B** | BIOS/UEFI firmware runs first from motherboard ROM to check hardware via POST before loading the OS. |
| **Q2** | **B** | GRUB (Grand Unified Bootloader) loads the selected OS kernel into RAM and hands over CPU control. |
| **Q3** | **A** | Mutual Exclusion, Hold and Wait, No Preemption, and Circular Wait are the 4 required Coffman deadlock conditions. |
| **Q4** | **A** | User space sandboxing protects overall system stability and prevents unauthorized hardware access. |
| **Q5** | **C (Linker)** | Correction: **B (Linker)** joins compiled object files (`.o`) and libraries into a single `.exe` executable. |
| **Q6** | **A** | Bundling a dedicated Chromium browser engine inside each Electron app increases RAM usage compared to native apps. |
| **Q7** | **True** | Virtual memory extends RAM using disk space, and excessive page swapping causes thrashing. |
| **Q8** | **False** | Device drivers are low-level system software that translate OS commands for hardware peripherals. |
| **Q9** | **True** | System calls act as the controlled doorway from restricted User Space into privileged Kernel Space. |
| **Q10** | **True** | Compilers (`gcc`) translate the whole program ahead of time; interpreters (`python`) run code line by line. |

---

## 4. References
1. Tanenbaum, A. S., & Bos, H. (2022). *Modern Operating Systems* (5th ed.). Pearson.
2. Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). *Operating System Concepts* (10th ed.). Wiley.
3. BIT2026 Course Lecture Slides (Stages 1.1–1.4).
