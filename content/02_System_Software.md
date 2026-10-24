# 1.2 Low-Level System Software (BIOS, Firmware, and Drivers)

**Status:** Completed  
**Team Member:** Cassinis Soulisack (`@DiegoSmiley`)  

---

## 1. What is System Software?
* Software that sits between computer hardware and application software.
* Includes the BIOS/UEFI, firmware, and device drivers.
* Prepares the computer so that the Operating System can load and run properly.

### Key Terminology
* **Firmware:** Semi-permanent software built directly into a hardware memory chip (ROM/Flash) to control that specific device.
* **BIOS / UEFI:** Essential motherboard firmware that runs immediately when you turn on the PC to test hardware and load the OS.
* **POST (Power-On Self-Test):** A quick health check of the CPU, RAM, and keyboard done by the BIOS before booting.
* **Device Driver:** A translator program that tells the OS how to talk to a specific piece of hardware (like a printer or graphics card).

---

## 2. Boot Sequence Flowchart
```text
[ 1. Power Button Pressed ]
            |
            v
[ 2. BIOS / UEFI Firmware Wakes Up ]
            |
            v
[ 3. Runs POST (Checks CPU, RAM, Display) ]
            |
            v
[ 4. Loads Bootloader from SSD into RAM ]
            |
            v
[ 5. OS Starts, Loads Drivers, Shows Login ]
