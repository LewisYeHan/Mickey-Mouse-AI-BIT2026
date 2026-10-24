# 1.4 Module Synthesis & Self-Check Quiz

**Status:** Completed  
**Team Members:** Samuel Wong (`@Samuel1940398`) & Lewis Goh (`@LewisYeHan`)  

---

## 1. Executive Summary
This module covered the core layers of computing systems:
* **Operating Systems (1.1):** Manage CPU, memory, and provide user interfaces (CLI/GUI).
* **System Software (1.2):** BIOS/UEFI firmware and device drivers that wake up hardware.
* **Application Software (1.3):** User-facing programs running safely in user space using system calls.

---

## 2. Self-Check Quiz

### Multiple-Choice Questions (MCQs)
**Q1. When you press the power button on a PC, what runs FIRST?**  
* A) Windows OS Kernel  
* B) Motherboard BIOS / UEFI Firmware  
* C) Web Browser  

**Q2. Why do apps run in "User Space" instead of touching hardware directly?**  
* A) To prevent bugs or malware from crashing the entire computer system.  
* B) Because CPUs cannot understand application code.  

### True or False
**Q3. (True / False):** *An operating system can use virtual memory on an SSD as extra RAM when physical RAM runs out.*  
**Q4. (True / False):** *A device driver is classified as application software used for word processing.*  

---

## 3. Answer Key

| Question | Correct Answer | Explanation |
| :--- | :--- | :--- |
| **Q1** | **B** | BIOS/UEFI firmware runs first from ROM to check hardware before loading the OS. |
| **Q2** | **A** | User space sandboxing protects system stability and security. |
| **Q3** | **True** | Virtual memory moves inactive pages to storage to prevent crashes. |
| **Q4** | **False** | Device drivers are system software that control hardware peripherals. |

---

## 4. References
1. Tanenbaum, A. S. (2022). *Modern Operating Systems* (5th ed.). Pearson.
2. Course Lecture Slides.
