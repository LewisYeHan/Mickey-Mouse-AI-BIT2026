# 1.2 System Software (BIOS, Firmware, and Drivers)

**Status:** Completed  
**Team Member:** Cassinis Soulisack (`@DiegoSmiley`)  

---

## 1. What is system software?
System software is software that runs the computer itself, so other programs can run on it.
* **Application software** works for the user (Chrome, Word, games).
* **System software** works for the computer (controls hardware, manages resources).
* **Simple analogy (a restaurant):** Hardware = the kitchen. System software = the kitchen staff. Apps = the dishes. The customer (you) never touches the stove.

### Main types:
* Firmware (including BIOS/UEFI)
* Operating system (OS)
* Device drivers
* Utility programs
* Language translators (compiler, interpreter, assembler)

---

## 2. Layers of a computer
Read from top (user) to bottom (hardware). Each layer only talks to the one next to it.

| Layer | Example | Category |
| :--- | :--- | :--- |
| **User** | You | End User |
| **Application software** | Chrome, Word, games | App Software |
| **Utilities and translators** | Antivirus, `gcc` | *System Software* |
| **Operating system (kernel)** | Windows, Linux | *System Software* |
| **Device drivers** | GPU, Wi-Fi drivers | *System Software* |
| **Firmware (BIOS/UEFI)** | Motherboard chip | *System Software* |
| **Hardware** | CPU, RAM, SSD | Physical Machine |

---

## 3. Firmware
Firmware is software stored on a hardware chip (flash memory/ROM). It gives a device its most basic instructions.
* **Non-volatile:** it stays when power is off.
* **Found in:** motherboards, SSDs, routers, printers, phones, cars.
* Can be updated ("flashing"). A failed update can "brick" the device.
* In simple devices (microwave, washing machine), firmware is the only software.

---

## 4. BIOS and UEFI
**BIOS (Basic Input/Output System)** is the firmware on the motherboard. It is the first software that runs when you turn on the PC.

### What BIOS does:
1. **POST (Power-On Self-Test):** checks CPU, RAM, keyboard, graphics. A problem = beep codes or an error.
2. Sets up hardware so it is ready to use.
3. Reads settings (boot order, clock) from CMOS memory, kept alive by a small CMOS battery.
4. Finds a bootable drive (SSD, USB).
5. Hands control to the bootloader.

**UEFI** is the modern replacement for BIOS (used since around 2012). People still call it "BIOS."

| Feature | Legacy BIOS | UEFI |
| :--- | :--- | :--- |
| **Mode** | 16-bit | 32/64-bit |
| **Disk format** | MBR | GPT |
| **Max boot disk** | ~2 TB | Practically unlimited |
| **Interface** | Text, keyboard only | Graphical, mouse |
| **Security** | None | Secure Boot |
| **Speed** | Slower | Faster |

* **Secure Boot** only lets signed (trusted) bootloaders and OSes start. This blocks malware that tries to load before the OS.

---

## 5. The boot process (step by step)
**Booting** = starting the computer until you see the login screen.

![Booting Process Flowchart](boot_sequence.png)
