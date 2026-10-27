# 1.4 Module Summary & Self-Check Quiz

**Status:** ✅  
**Team Members:** Wong Hiu Chung Samuel (`@Samuel940398`) & Goh Ye Han (`@LewisYeHan`)

**In this section:** How It All Connects · Key Ideas from Each Section · Quiz (13 questions) · Answer Key · References

---

## 1. How It All Connects

![How sections 1.1 to 1.3 connect](images/concept_map.png)
*Figure 1.6: How system software, the OS, and applications work together on top of the hardware.*

Sections 1.1 to 1.3 describe three layers of software that work together every time you use a computer. Figure 1.6 shows them side by side: system software (1.2) starts the computer and loads the OS, the OS (1.1) manages the hardware through drivers, and applications (1.3) never touch the hardware directly; they ask the OS through system calls. Read the figure from left to right: the computer starts with 1.2, so it comes first. The easiest way to see how this works is to follow one story, from the moment you press the power button to the moment an app saves a file.

**Starting up (1.2 System Software).** When you press the power button, the first thing that runs is the **firmware** (BIOS or UEFI) stored on the motherboard. It checks the hardware with **POST**, finds the boot drive, and starts the **bootloader**. The bootloader loads the **kernel** into RAM, and the kernel starts the device drivers and the first process (such as `systemd`), which starts the system services until the login screen appears.

**Managing everything (1.1 Operating Systems).** Once the OS is running, it shares the computer between everything that wants to use it, like a head chef running a busy kitchen. It turns programs into **processes**, decides which one gets the CPU next (**scheduling**), gives each one its own private memory (**virtual memory** and **paging**), and controls devices through **drivers**. It also has to prevent problems like **deadlock** and **thrashing**.

**Doing the user's work (1.3 Application Software).** When you open an app, the OS **loader** copies it from the SSD into RAM as a new process, and the CPU starts running its instructions. The app lives in **user space**, so it cannot touch the hardware directly. Whenever it needs to save a file or use the network, it makes a **system call**, and the kernel does the job safely and sends the result back.

**The main idea:** each layer does its own job and relies on the layer below it. Apps ask the OS, the OS uses drivers, and drivers talk to the hardware. This design keeps the computer **safe** (one bad app cannot crash everything), **shared** (many apps can run at once), and **simple** (app makers do not need to know every hardware model).

---

## 2. Key Ideas from Each Section

| Section | Main question | Key ideas |
| :--- | :--- | :--- |
| **1.1 Operating Systems** | How does the OS share the computer? | Processes and process states, CPU scheduling (FCFS, SJF, Priority, Round Robin), deadlock, virtual memory and paging, I/O and drivers |
| **1.2 System Software** | How does the computer start and control hardware? | Firmware, BIOS vs. UEFI, the boot process, kernel types, device drivers, utilities, compilers and interpreters |
| **1.3 Application Software** | How does an app actually run? | User space vs. kernel space, the 5-step execution lifecycle, system calls, types of apps, native vs. web vs. cross-platform apps |

### Words That Connect All Three Sections

| Term | In 1.2 System Software | In 1.1 Operating Systems | In 1.3 Application Software |
| :--- | :--- | :--- | :--- |
| **Kernel** | Loaded into RAM during boot | Manages processes and memory | Answers system calls from apps |
| **Process** | Started by the kernel at boot (e.g., `systemd`) | Scheduled and moved between states | Created by the loader when you open an app |
| **Driver** | A type of system software | Used by the OS to control devices | Does the hardware work when an app asks |
| **RAM** | Where the kernel is loaded at boot | Managed with paging and virtual memory | Where apps run |

---

## 3. Self-Check Quiz
Try all 13 questions first, then check your answers in Section 4. Part A checks that you remember the key ideas. Parts B and C ask you to **use** them.

### Part A: Multiple Choice

**Q1. When you press the power button on a PC, what runs first?**  
* A) The OS kernel
* B) The bootloader
* C) The BIOS / UEFI firmware
* D) The device drivers

**Q2. During booting, what is the main job of the bootloader (such as GRUB or Windows Boot Manager)?**  
* A) To check the hardware with POST
* B) To show the login screen
* C) To start the background system services
* D) To load the OS kernel into RAM

**Q3. Which of these is NOT one of the four conditions needed for a deadlock?**  
* A) Preemption (resources can be taken away by force)
* B) Mutual exclusion
* C) Circular wait
* D) Hold and wait

**Q4. Why do applications run in user space instead of touching hardware directly?**  
* A) Because user space makes apps run faster than kernel space
* B) Because only the kernel is allowed to use the CPU
* C) So one buggy app cannot crash the whole system or read other apps' memory
* D) So apps can skip the CPU scheduler

**Q5. Which tool joins compiled object files and libraries into one executable (`.exe`) file?**  
* A) Assembler
* B) Linker
* C) Loader
* D) Preprocessor

**Q6. In Round Robin scheduling, what happens when a running process uses up its time slice but is not finished?**  
* A) It is terminated
* B) It moves to the Waiting state
* C) It is suspended to disk
* D) It goes back to the Ready queue

### Part B: Apply It

**Q7. Three processes arrive at the same time in this order: P1 needs 3 units, P2 needs 1 unit, P3 needs 2 units. With Round Robin and a time slice of 2, which process finishes LAST?**  
* A) P1
* B) P2
* C) P3
* D) They all finish at the same time

**Q8. Your PC turns on and the fans spin, but it keeps beeping and nothing appears on the screen. Which part of the boot process has found a problem?**  
* A) The bootloader could not find the kernel
* B) POST in the BIOS/UEFI found a hardware problem
* C) The kernel crashed while starting the drivers
* D) The login service failed to start

**Q9. A student's laptop has 8 GB of RAM. They open 40 browser tabs, a game, and a video editor, and the computer becomes extremely slow while the disk light stays on all the time. What is most likely happening?**  
* A) Deadlock
* B) Starvation
* C) A context switch
* D) Thrashing

**Q10. A small team wants to release an installable desktop app for Windows, macOS, and Linux from one codebase as soon as possible. Using extra memory is acceptable. Which approach fits best?**  
* A) Three separate native apps
* B) One native app written only for Windows
* C) An Electron app
* D) A web app

### Part C: True or False

**Q11.** Firmware is stored inside the operating system on your SSD.

**Q12.** In a deadlock, the system keeps working but one unlucky process keeps getting skipped.

**Q13.** Because each running app gets its own private memory space, one app cannot normally read another app's memory.

---

## 4. Answer Key

<details>
<summary><b>Show answers</b> (try the quiz first!)</summary>

| Question | Answer | Explanation |
| :--- | :--- | :--- |
| **Q1** | **C** | The firmware runs first. It checks the hardware with POST and then starts the bootloader. *(1.2)* |
| **Q2** | **D** | The bootloader finds the OS kernel, loads it into RAM, and hands it control of the CPU. POST happens before it, and services and the login screen come after. *(1.2)* |
| **Q3** | **A** | The real condition is **no** preemption: resources cannot be taken away by force. If they *could* be taken away, the deadlock could be broken. *(1.1)* |
| **Q4** | **C** | User space keeps apps isolated, so a crash or bug in one app cannot damage the hardware or other apps. Apps still run on the CPU; they just cannot control the hardware directly. *(1.3)* |
| **Q5** | **B** | The linker combines object files and libraries into one executable. The loader then copies it into RAM to run it. *(1.2)* |
| **Q6** | **D** | When its time slice ends, the process goes back to the Ready queue to wait for its next turn. It only goes to Waiting if it asks for I/O. *(1.1)* |
| **Q7** | **A** | P1 runs 0–2, P2 runs 2–3 and finishes, P3 runs 3–5 and finishes, then P1 runs 5–6 and finishes last. *(1.1)* |
| **Q8** | **B** | Beep codes come from POST, which runs before the bootloader and before the screen is set up. *(1.2)* |
| **Q9** | **D** | RAM is far too full, so the OS spends most of its time moving pages between RAM and disk. That is thrashing. *(1.1)* |
| **Q10** | **C** | Electron lets one codebase become an installable app on all three desktop systems. Three native apps would take much longer, a Windows-only native app misses macOS and Linux, and a web app is not installed. *(1.3)* |
| **Q11** | **False** | Firmware is stored on a chip *inside the device* itself. Drivers are the part that lives inside the OS. *(1.2)* |
| **Q12** | **False** | That describes **starvation**. In a deadlock, the stuck processes cannot move at all, because each is waiting for something another one holds. *(1.1)* |
| **Q13** | **True** | With virtual memory, each process has its own address space, and the MMU keeps processes from reaching each other's memory. *(1.1, 1.3)* |


</details>

---

## 5. References
1. Arpaci-Dusseau, R. H., & Arpaci-Dusseau, A. C. (2018). *Operating Systems: Three Easy Pieces*. Arpaci-Dusseau Books.
2. Silberschatz, A., Galvin, P. B., & Gagne, G. (2018). *Operating System Concepts* (10th ed.). Wiley.
3. Tanenbaum, A. S., & Bos, H. (2022). *Modern Operating Systems* (5th ed.). Pearson.
4. BIT2026 Course Lecture Slides (Stages 1.1–1.4).
