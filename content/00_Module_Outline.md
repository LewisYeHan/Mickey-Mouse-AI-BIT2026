# Module Outline: Computer Software Architecture (System, OS, and Application Software)

## 1. Intended Learning Outcomes
By the end of this module, beginners will be able to:
1. **Distinguish** between low-level system software (BIOS/UEFI, firmware, device drivers), operating systems, and end-user application software.
2. **Explain** how an Operating System manages hardware resources (CPU scheduling, RAM allocation, and device I/O) and why different platforms (Windows, macOS, Linux, Android) are designed differently.
3. **Trace** the step-by-step lifecycle of how an application launches, requests hardware access through the OS via system calls, and executes as a process in memory.
4. **Diagnose** basic real-world software scenarios (e.g., identifying whether a malfunction is caused by a missing driver, high RAM usage, or an application crash).

## 2. Prerequisite Knowledge
* **Required:** Basic familiarity with core computer hardware components—specifically the **CPU** (processor), **RAM** (volatile working memory), **Storage** (SSD/HDD), and **Input/Output (I/O) peripherals** (keyboard, display, printer).
* **Not Required:** No prior programming experience or command-line knowledge is needed.

---

## 3. Logical Learning Sequence & Development Status

> **Status Labels Used:** `checked` (written & peer-reviewed), `drafted` (initial explanations written, pending review), `outline only` (structured plan ready for Stage 2), `needs revision` (flagged during review).

| Section | Major Topics & Subtopics | Assigned Member | Planned Examples, Visuals & Activities | Current Status |
| :--- | :--- | :--- | :--- | :--- |
| **1.1 Operating Systems (Core V1.0 Topic)** | • Role of the OS as resource manager<br>• Resource allocation (CPU & RAM)<br>• Performance monitoring & Device management<br>• Platform comparison (Windows, macOS, Android, Linux) | Yeo Shih Jie (`@ysjie03`) | • **Visual:** OS Kernel Bridge Diagram & OS Comparison Table<br>• **Worked Example:** Tracing CPU & RAM allocation when opening apps simultaneously<br>• **Activity:** Task Manager bottleneck scenario | `checked` *(Full V1.0 Developed)* |
| **1.2 Low-Level System Software** | • What is System Software?<br>• BIOS / UEFI & the boot sequence<br>• Firmware in embedded devices<br>• Device Drivers (translating OS commands for hardware) | Lu My Ky (`@jojolu11`) | • **Visual:** Computer Boot Sequence Flowchart (Power button -> BIOS -> OS)<br>• **Worked Example:** Plug-and-play USB mouse driver handshake<br>• **Activity:** Troubleshooting a "Device Not Recognized" error | `drafted` |
| **1.3 Application Software & Execution** | • Application vs. System software<br>• How apps run: Storage (SSD) -> Process in RAM -> CPU threads<br>• Relationship with the OS (System Calls & APIs) | Cao Minh Tuan (`@mnhtnc`) | • **Visual:** User Space vs. Kernel Space interaction diagram<br>• **Worked Example:** How a Word Processor saves a file to disk via the OS<br>• **Activity:** Matching actions to Application vs. OS responsibilities | `drafted` |
| **1.4 Synthesis, Architecture & Assessment** | • End-to-End Software Layer Model (Hardware <-> User)<br>• Interactive Concept Map<br>• Comprehensive Self-Check Quiz (MCQs + True/False with explained solutions) | Frederick Samuel (`@Ti4nCi`) | • **Visual:** Full-stack Software Architecture Concept Map<br>• **Activity:** 5 Scenario-based MCQs + 5 True/False questions with full step-by-step answer explanations | `drafted` |

---

## 4. Honest Gaps & Uncertainties (Stage 1 Reflection)
* **Scope of OS Scheduling Algorithms (Section 1.1):** We want to explain CPU resource allocation clearly without overwhelming beginners with complex mathematical scheduling algorithms.
* **BIOS vs. Modern UEFI Distinction (Section 1.2):** Most modern computers use UEFI rather than legacy BIOS, though people still call it "BIOS." We are confirming how deeply to distinguish the two.
* **Custom Diagrams (Sections 1.2 & 1.3):** While Section 1.1's visuals are complete, Sections 1.2 and 1.3 currently rely on text tables and need clean custom diagrams drawn for Stage 2 PPT Slides and Study Guide.
