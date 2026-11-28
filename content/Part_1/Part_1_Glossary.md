# 1.4 Glossary

**Team Members:** Wong Hiu Chung Samuel (`@Samuel940398`) & Goh Ye Han (`@LewisYeHan`)

**In this section:** every key term from Part 1, in A–Z order. The last column shows which section explains it in more detail.

| Term | Meaning | Section |
| :--- | :--- | :--- |
| **Absolute path** | The full address of a file, starting from the top of the folder tree, such as `/home/mei/Documents/essay.txt`. | 1.2 |
| **Aging** | Slowly raising the priority of a process that has been waiting a long time, so it does not starve. | 1.2 |
| **Application software** | Software that does a task you chose, such as writing, gaming or browsing. | 1.3 |
| **Assembler** | A tool that turns assembly language into machine code. | 1.1 |
| **Authentication** | Checking who you are, for example with a password or Face ID. | 1.2 |
| **Authorization** | Deciding what you are allowed to open or change once you are logged in. | 1.2 |
| **BIOS** | Basic Input/Output System. The older startup firmware on a PC motherboard. | 1.1 |
| **Booting** | Starting the computer, from pressing the power button to reaching the login screen. A cold boot starts from power off; a warm boot is a restart. | 1.1 |
| **Bootloader** | The program that finds the OS kernel and loads it into RAM (for example, GRUB or Windows Boot Manager). | 1.1 |
| **Buffer** | A temporary holding area for data in memory. | 1.2 |
| **Bytecode** | A simpler form that Python turns a program into before running it one instruction at a time. | 1.1 |
| **Cache** | Fast memory that keeps copies of often-used data. | 1.2 |
| **Circular wait** | One of the four deadlock conditions: the processes wait for each other in a loop (A waits for B, B waits for A). | 1.2 |
| **CLI** | Command Line Interface. You control the computer by typing text commands. | 1.2 |
| **CMOS** | A small memory chip that stores BIOS settings, kept alive by a coin-cell battery. | 1.1 |
| **Compiler** | A tool that translates a whole program into machine code before it runs. | 1.1 |
| **Concurrency** | Taking turns on one CPU core so quickly that several programs seem to run at once. | 1.2 |
| **Context switch** | Saving one process's progress and loading another's onto the CPU. | 1.2 |
| **Cross-platform app** | An app built from one codebase that runs on several systems (for example, with Electron, Flutter or React Native). | 1.3 |
| **Deadlock** | Processes that are stuck forever, each waiting for something another one holds. | 1.2 |
| **Demand paging** | Loading a page into RAM only when the program actually needs it. | 1.2 |
| **Directory** | Another name for a folder. Folders hold files and other folders, forming a tree. | 1.2 |
| **DMA** | Direct Memory Access. A device copies data straight into RAM without the CPU having to move each byte. | 1.2 |
| **Driver** | Software that lets the OS control one specific hardware device. | 1.1, 1.2 |
| **Electron** | A framework for building desktop apps with web technology. Each app carries its own copy of the Chromium browser engine. | 1.3 |
| **Execution lifecycle** | The 5 steps of running an app: file on SSD → loaded into RAM as a process → CPU runs it → system call → kernel does the work. | 1.3 |
| **FCFS** | First Come, First Served. Processes run in the order they arrive. | 1.2 |
| **File system** | The part of the OS that keeps track of files, folders and which disk blocks each file uses (for example NTFS, APFS, ext4). | 1.2 |
| **Finish time** | The moment a process is completely done. | 1.2 |
| **Firmware** | Software stored on a chip inside a device that gives it its most basic instructions. It keeps its data when the power is off. | 1.1 |
| **GPT** | GUID Partition Table. The modern disk layout used with UEFI. | 1.1 |
| **GUI** | Graphical User Interface. You control the computer with icons, windows and a mouse or touchscreen. | 1.2 |
| **Heap** | The part of a process's memory used for memory the program asks for while it is running. | 1.3 |
| **Hold and wait** | One of the four deadlock conditions: a process keeps what it has while waiting for more. | 1.2 |
| **Hybrid kernel** | A kernel design that mixes the monolithic and microkernel designs: mostly fast like a monolithic kernel, but more modular (for example, Windows and macOS). | 1.2 |
| **Hyper-threading** | A CPU feature that lets one core hold two threads at once, so the OS counts each core as two logical processors. | 1.2 |
| **Interpreter** | A tool that runs a program step by step while it is running (Python first turns the code into bytecode). | 1.1 |
| **Interrupt** | A signal from a device telling the CPU it needs attention. | 1.2 |
| **Journaling** | A file system keeping a short log of changes so the disk is not left broken if the power cuts out. | 1.2 |
| **Kernel** | The core of the OS, with full control of the hardware. | 1.1, 1.2 |
| **Kernel mode** | The CPU mode in which the kernel runs, with full access to the hardware. | 1.1, 1.2, 1.3 |
| **Kernel space** | The protected area of memory where the kernel runs, with full access to the hardware. | 1.3 |
| **Linker** | A tool that joins compiled object files and libraries into one executable file. | 1.1 |
| **Loader** | The part of the OS that copies a program from storage into RAM so it can run. | 1.1, 1.3 |
| **Logical processor** | What the OS counts as one CPU. With hyper-threading, each core shows up as two logical processors. | 1.2 |
| **Machine code** | The instructions a CPU actually understands: long strings of 0s and 1s. | 1.1, 1.2, 1.3 |
| **MBR** | Master Boot Record. The first 512 bytes of a disk, used to start booting on older BIOS systems. | 1.1 |
| **Metadata** | Information about a file, such as its size, dates and owner, kept alongside its data. | 1.2 |
| **Microkernel** | A kernel design kept tiny: drivers and file systems run outside the kernel as separate programs, so if one crashes, it can be restarted. Very stable, but slightly slower (for example, MINIX and QNX). | 1.2 |
| **MMU** | Memory Management Unit. Hardware that turns virtual addresses into real RAM addresses. | 1.2 |
| **Monolithic kernel** | A kernel design in which almost everything, including drivers and file systems, runs inside one big kernel. Very fast, but one bug can crash the whole system (for example, Linux). | 1.2 |
| **Multiprogramming** | Keeping several programs in RAM at once, so the CPU can switch to another one while one waits. | 1.2 |
| **Multitasking** | Running many programs at the same time, with the OS sharing the CPU between them. | 1.2 |
| **Mutual exclusion** | One of the four deadlock conditions: only one process can use a resource at a time. | 1.2 |
| **Native app** | An app built for one specific platform, such as Windows or iOS. It is usually the fastest option. | 1.3 |
| **No preemption** | One of the four deadlock conditions: a resource cannot be taken away from a process by force. | 1.2 |
| **Non-preemptive scheduling** | Scheduling in which a process keeps the CPU until it finishes or waits for I/O. | 1.2 |
| **Open source** | Software whose code anyone can read, change and share. | 1.2 |
| **Operating system (OS)** | The main software that runs the computer and sits between your apps and the hardware. It decides which program gets the CPU, how much memory each one may use, and who can touch which file. | 1.1, 1.2 |
| **Page fault** | When a page a program needs is not in RAM and must be loaded from disk. | 1.2 |
| **Paging** | Splitting memory into equal-sized blocks (pages and frames). | 1.2 |
| **Parallelism** | Several CPU cores really running different work at the same moment. | 1.2 |
| **PCB** | Process Control Block. The OS's record of one process. | 1.2 |
| **PID** | Process ID. The number the OS gives each process; Task Manager shows it on the Details page. | 1.2, 1.3 |
| **Plug and Play** | The OS noticing new hardware, such as a USB mouse, and loading the right driver automatically. | 1.1, 1.2 |
| **Polling** | The CPU checking a device over and over to see if it is ready. | 1.2 |
| **POST** | Power-On Self-Test. The firmware's check that the hardware works at startup. | 1.1 |
| **Preemptive scheduling** | Scheduling in which the OS can stop a running process and give the CPU to another one. | 1.2 |
| **Preprocessor** | The first step of building a C program: it handles lines such as `#include` and `#define`. | 1.1 |
| **Priority scheduling** | Scheduling in which the most important process goes first; aging stops low-priority processes from starving. | 1.2 |
| **Process** | A program that is currently running. | 1.2, 1.3 |
| **Process states** | The five states a process moves between: New, Ready, Running, Waiting (Blocked) and Terminated. | 1.2 |
| **Program counter** | Where a process is in its instructions. It is saved in the PCB during a context switch. | 1.2 |
| **RAM** | Fast main memory that loses its data when the power is off. | 1.2 |
| **Ready queue** | The line of processes that are in memory and waiting for their turn on the CPU. | 1.2 |
| **Relative path** | The address of a file starting from the folder you are already in, such as `Documents/essay.txt`. | 1.2 |
| **Round Robin** | Scheduling that gives each process a short, equal turn on the CPU. | 1.2 |
| **Sandboxing** | Keeping each app in its own closed box so it cannot reach other apps or the rest of the system. | 1.2 |
| **Scheduler** | The part of the OS that decides which process runs next. | 1.2 |
| **Secure Boot** | A UEFI feature that only lets trusted, signed software start. | 1.1 |
| **Segmentation** | Splitting memory into meaningful parts such as code, data and stack. | 1.2 |
| **Shell** | The part of the OS that takes your commands. | 1.2 |
| **SJF** | Shortest Job First. The shortest process runs next; this gives the lowest average waiting time when all jobs are ready together. | 1.2 |
| **Spooling** | Lining up jobs on disk for a slow device, like a print queue. | 1.2 |
| **Stack** | The part of a process's memory that keeps track of function calls and their local variables. | 1.3 |
| **Starvation** | When a process keeps getting skipped and never runs. | 1.2 |
| **Swapping** | Moving an inactive process between RAM and disk. | 1.2 |
| **System call** | A request from an app to the kernel, such as `read()` or `write()`. | 1.2, 1.3 |
| **System software** | Software that runs the computer itself so apps can work, such as the OS, drivers and utilities. | 1.1 |
| **Thrashing** | An extreme slowdown caused by moving too many pages between RAM and disk. | 1.2 |
| **Thread** | A small worker inside a process that shares the process's memory. | 1.2, 1.3 |
| **Time slice** | The short turn each process gets on the CPU in Round Robin. | 1.2 |
| **UEFI** | Unified Extensible Firmware Interface. The modern replacement for BIOS. | 1.1 |
| **User mode** | The CPU mode in which normal apps run, with limited rights. If an app crashes, only that app closes. | 1.1, 1.2, 1.3 |
| **User space** | The protected area where apps run. Apps here cannot touch the hardware directly. | 1.3 |
| **Utility** | A small system program that maintains the computer, such as antivirus or disk cleanup. | 1.1 |
| **Virtual memory** | Giving each program its own memory space, so the OS can keep rarely used parts on disk. | 1.2 |
| **Waiting time** | How long a process spends ready but not running. | 1.2 |
| **Web app** | An app that runs inside a web browser and usually needs no installation. | 1.3 |
