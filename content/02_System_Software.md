# 1.2 System Software

**Status:** ✅  
**Team Member:** Cassinis Soulisack (`@DiegoSmiley`)

**In this section:** What is System Software · Layers · Firmware · BIOS & UEFI · Boot Process · Kernel · Drivers · Utilities & Translators · Summary

---

## 1. What is System Software?
**System software** is software that runs and manages the computer itself so that other programs can run on top of it.
* **Application Software** works directly for the user (e.g., Chrome, Word, games).
* **System Software** works for the computer in the background (controlling hardware and managing system resources).
* **Simple Analogy (A Restaurant):** The **Hardware** is the kitchen and stoves. **System Software** is the kitchen staff who operate the equipment safely. **Applications** are the finished dishes brought to the table. The customer (**You**) never touches the hot stove directly.

### Main Types of System Software
1. **Firmware** (including BIOS and UEFI)
2. **Operating System (OS)**
3. **Device Drivers**
4. **Utility Programs**
5. **Language Translators** (compilers, interpreters, and assemblers)

---

## 2. Layers of a Computer System
Read from top (the user) to bottom (the physical hardware). Each layer relies on the layers below it. The four middle layers are all **System Software**:

| Layer | Example | Type |
| :--- | :--- | :--- |
| **User** | You | End User |
| **Application Software** | Chrome, Word, games | Application Software |
| **Utilities and Translators** | Antivirus, `gcc` compiler | **System Software** |
| **Operating System (Kernel)** | Windows, Linux, macOS | **System Software** |
| **Device Drivers** | GPU driver, Wi-Fi driver, printer driver | **System Software** |
| **Firmware (BIOS / UEFI)** | Motherboard ROM chip | **System Software** |
| **Hardware** | CPU, RAM, SSD | Physical Hardware |

*Note:* Device drivers run inside the OS, together with the kernel. The motherboard firmware (BIOS / UEFI) does its main job **at startup**: once the OS is running, drivers talk to the hardware directly, not through the BIOS.

---

## 3. Firmware
**Firmware** is low-level software stored permanently on a chip (flash memory or ROM) inside a device. It gives the device its most basic startup instructions.
* **Non-Volatile:** Firmware stays on the chip even when the power is off.
* **Where It Is Found:** Motherboards, SSDs, Wi-Fi routers, printers, smartphones, and cars.
* **Updating ("Flashing"):** Firmware can be updated to fix bugs, but losing power during an update can permanently **"brick"** the device.
* **Simple Appliances:** In single-purpose devices like a microwave or washing machine, firmware is the *only* software inside.

---

## 4. BIOS and UEFI
**BIOS (Basic Input/Output System)** is the startup firmware stored on the PC motherboard. It is the very first software that runs when you press the power button.

### What BIOS Does at Startup
1. **POST (Power-On Self-Test):** Checks that the CPU, RAM, keyboard, and graphics card are working. Errors are reported with **beep codes** or on-screen messages.
2. **Initializes Hardware:** Sets up the motherboard and devices so they are ready to use.
3. **Reads CMOS Settings:** Loads saved settings (such as boot order and the system clock) from CMOS memory, which is kept alive by a small coin-cell **CMOS battery**.
4. **Finds a Bootable Drive:** Checks connected SSDs, HDDs, or USB drives in boot order.
5. **Hands Control to the Bootloader:** Starts the OS bootloader stored on the boot drive.

### Legacy BIOS vs. Modern UEFI
**UEFI (Unified Extensible Firmware Interface)** is the modern replacement for BIOS (standard on PCs since around 2012), though people still often call it "BIOS."

| Feature | Legacy BIOS | Modern UEFI |
| :--- | :--- | :--- |
| **Mode** | 16-bit | 32-bit / 64-bit |
| **Disk Format** | MBR (Master Boot Record) | GPT (GUID Partition Table) |
| **Max Boot Disk Size** | ~2 TB | Practically unlimited |
| **Interface** | Plain text, keyboard only | Usually a graphical menu with mouse support |
| **Security** | Basic (e.g., a BIOS password), no Secure Boot | **Secure Boot** |
| **Startup Speed** | Slower | Faster |

* **Secure Boot:** Only lets digitally signed (trusted) bootloaders and operating systems start. This blocks malware that tries to load before the OS.

---

## 5. The Boot Process
**Booting** means starting the computer from power-on until the login screen appears. A **cold boot** starts from power off; a **warm boot** is a restart.

![The boot process](images/boot_process.jpeg)
*Figure 1.4: The 6 steps of booting, from pressing the power button to the login screen. Drawn by Team Mickey Mouse in Canva.*

1. **Power On → BIOS / UEFI:** The CPU wakes up and runs the firmware, which performs **POST** and initializes RAM and devices.
2. **Boot Drive (MBR / GPT):** The firmware follows the boot order and reads the boot information on the main drive (the first 512 bytes, called the **MBR**, on Legacy BIOS; the **EFI System Partition** on UEFI).
3. **Bootloader:** The full bootloader program starts (**GRUB** on Linux, **Windows Boot Manager** on Windows) and chooses which OS kernel to load.
4. **Kernel Loads:** The bootloader loads the **OS kernel** into RAM and hands it control of the CPU. The kernel starts the device drivers.
5. **Init / System Services:** The kernel starts the first process (**`systemd`** on modern Linux, or the older **`init`**; **`smss.exe`** on Windows), which starts the background services.
6. **Login Screen:** The system reaches its normal running mode (called a **run level** on older Linux, a **target** with `systemd`), shows the login screen, and loads your desktop after you sign in.

---

## 6. The Kernel
The **Operating System** manages processes, memory, files, devices, security, and the user interface (see [1.1 Operating Systems](01_Operating_Systems.md) for details). Its most important part is the **Kernel**, the core of the OS that stays in memory and controls the hardware directly.

* **Kernel Mode:** Full hardware access (used by the kernel and most drivers). A crash here crashes the whole PC (e.g., the Blue Screen of Death).
* **User Mode:** Limited access (used by normal apps). A crash here only closes that one app.
* **System Call:** How a user-mode app asks the kernel for help (e.g., in C, `printf()` uses the `write()` system call).
* **Interrupt:** A hardware signal that tells the CPU *"stop, I need attention"* (e.g., pressing a key). The CPU handles it, then continues what it was doing.

### Kernel Types

| Kernel Type | Core Idea | Examples |
| :--- | :--- | :--- |
| **Monolithic** | Everything runs inside one big kernel. Very fast, but one bug can crash the whole system. | Linux |
| **Microkernel** | Tiny core; drivers and file systems run outside it. Very stable, slightly slower. | MINIX, QNX |
| **Hybrid** | Mixes both: fast like monolithic, but more modular. | Windows, macOS |

---

## 7. Device Drivers
A **Device Driver** is a small program that lets the OS talk to one specific hardware device. Every device speaks its own language, and the driver translates.

### Example: Printing a Document
1. You click **Print** in Microsoft Word.
2. Word asks the OS to print the document.
3. The OS puts the job in the **print queue (spooling)**.
4. The OS sends the job to the **printer driver**.
5. The driver translates it into commands your specific printer understands.
6. The printer prints and reports back (e.g., *"Done"* or *"Out of paper"*).

### Key Points About Drivers
* Most drivers run in **kernel mode**, so a buggy driver can crash the whole PC.
* **Plug and Play:** The OS detects new hardware automatically and loads the right driver.
* Drivers need updates for bug fixes and new OS versions.
* **Driver vs. Firmware:** **Firmware** lives on a chip *inside the device*; a **driver** lives *inside the OS* on your drive.

---

## 8. Utilities and Language Translators

### Utility Programs (Keeping the Computer Healthy)
* **Antivirus:** Finds and removes malware.
* **Disk Cleanup:** Deletes temporary junk files to free up space.
* **Defragmenter:** Rearranges scattered data on hard drives (HDDs) to speed them up *(not needed for SSDs)*.
* **Backup:** Copies important data in case of hardware failure.
* **Compression:** Shrinks files into smaller archives (`.zip`).
* **Firewall:** Watches and filters network traffic in and out.

### Language Translators (Human Code → Machine Code)

| Translator | Input | How It Works | Example |
| :--- | :--- | :--- | :--- |
| **Assembler** | Assembly code | Converts assembly instructions directly into machine code | `NASM` |
| **Compiler** | C, C++ | Translates the whole program before it runs; together with the assembler and linker, this produces an executable file | `gcc` |
| **Interpreter** | Python | Translates and runs the code step by step while the program is running | `python` |

*Note:* Python actually turns the code into a simpler form called **bytecode** first, then runs it one instruction at a time. "Line by line" is a useful way to picture it.

### From C Source Code to a Running Program
1. **Preprocessor:** Handles `#include` and `#define`.
2. **Compiler:** Turns C code into **assembly code**.
3. **Assembler:** Turns assembly into a binary **object file** (`.o` on Linux, `.obj` on Windows).
4. **Linker:** Joins object files and libraries into one **executable** (`.exe` on Windows).
5. **Loader (part of the OS):** Copies the executable into RAM and starts it.

---

## 9. Summary

| Comparison | Difference |
| :--- | :--- |
| **System vs. Application Software** | Runs the computer vs. serves the user |
| **Firmware vs. Driver** | Stored on the device's chip vs. stored inside the OS |
| **BIOS vs. UEFI** | Older 16-bit, MBR vs. modern 64-bit, GPT, Secure Boot |
| **OS vs. Kernel** | The kernel is the core part of the whole OS |
| **Kernel Mode vs. User Mode** | Full hardware access vs. limited access |
| **Compiler vs. Interpreter** | Whole program before running vs. step by step while running |

### Key Points to Remember
1. **System software** sits between the hardware and user applications.
2. **BIOS/UEFI** runs first, performs **POST**, and starts the bootloader.
3. The **bootloader** (e.g., GRUB) loads the **kernel** into RAM.
4. **Drivers** let the OS talk to each hardware device.
5. **Utilities** keep the PC healthy, and **translators** turn human code into machine code.

---

## 10. References
1. Mueller, S. (2015). *Upgrading and Repairing PCs* (22nd ed.). Que Publishing.
2. Patterson, D. A., & Hennessy, J. L. (2020). *Computer Organization and Design* (6th ed.). Morgan Kaufmann.
3. BIT2026 Course Lecture Slides (System Software Module).
