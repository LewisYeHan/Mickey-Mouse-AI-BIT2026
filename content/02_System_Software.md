# 1.2 Low-Level System Software (BIOS, Firmware, and Drivers)

**Development Status:** `drafted` (Substantive V1.0 Draft)  
**Author:** Lu My Ky (`@jojolu11`)  

---

## 1. Concept Explanations & Terminology

While the Operating System is the most visible type of system software, the OS cannot wake up a powered-off computer by itself, nor does it inherently know the secret electrical commands for millions of different graphics cards, printers, and game controllers on the market. That gap is bridged by **Low-Level System Software**.

### Key Terminology
* **System Software:** Software designed to operate and control the computer hardware and to provide a platform for running application software (includes the OS, BIOS/UEFI, firmware, and device drivers).
* **Firmware:** Permanent or semi-permanent low-level software programmed directly into a hardware device's non-volatile memory chip (ROM/Flash) to control that specific piece of hardware.
* **BIOS (Basic Input/Output System) / UEFI (Unified Extensible Firmware Interface):** The essential motherboard firmware that initializes and tests hardware components the moment you press the power button, and then loads the Operating System from storage into RAM.
* **POST (Power-On Self-Test):** A diagnostic testing sequence run by the BIOS/UEFI at startup to verify that essential hardware (CPU, RAM, keyboard, display) is functioning properly before booting the OS.
* **Device Driver:** A specialized software translator that tells the Operating System exactly how to communicate with and control a specific piece of hardware (e.g., an NVIDIA GPU driver or a Logitech mouse driver).

---

## 2. Visual Sequence: From Power Button to Operating System

```text
+---------------------------------------------------------------+
|               [ 1. User Presses Power Button ]                |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|      [ 2. Motherboard BIOS / UEFI Firmware Wakes Up ]         |
|             (Stored in Motherboard ROM / Flash Chip)          |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|           [ 3. Runs POST (Power-On Self-Test) ]               |
|      (Verifies CPU, RAM, Display, and Keyboard Health)        |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|       [ 4. Locates Bootloader on SSD/HDD & Loads OS ]         |
|               (Transfers OS Kernel into RAM)                  |
+-------------------------------+-------------------------------+
                                |
                                v
+---------------------------------------------------------------+
|      [ 5. OS Loads Device Drivers & Shows Login Screen ]      |
|          (Initializes GPU, Wi-Fi, Audio, and Peripherals)     |
+---------------------------------------------------------------+
