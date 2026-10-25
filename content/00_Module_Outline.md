# Module Outline: Software and Symbolic AI

**Module Status:** Stage One Completed  
**Coordinator:** Yeo Shih Jie (`@ysjie03`) & Team  

---

## Part 1: Software (Stage One — Completed)

### 1.1 Operating Systems (`Completed`)
* **Core Concepts:** Definition of an Operating System, system layers (Users, Apps, System Software, OS, Hardware), Kernel vs. Shell, the 3 basic functions, and CLI vs. GUI interfaces.
* **History & Classification:** Evolution of operating systems from the 1940s to modern AI integration, the 7 primary OS types, and a full platform comparison across Windows, macOS, Linux, Android, and iOS.
* **Internal Architecture:** The 8 core OS components, processes and process states (with embedded `process_states.png` diagram), system calls, CPU scheduling algorithms, deadlock handling, virtual memory management, I/O device management, performance monitoring, and system security.

### 1.2 System Software (`Completed`)
* **Foundations:** Role of system software vs. application software, the 7-layer computer model, and non-volatile firmware mechanics.
* **Booting & Low-Level Control:** Motherboard BIOS vs. modern UEFI architecture, Secure Boot, and the step-by-step computer boot sequence (`System Startup BIOS` → `MBR Bootloader` → `GRUB` → `Kernel Init` → `INIT` → `Run Level`, with embedded `boot_sequence.png` diagram).
* **Drivers & Translators:** Monolithic vs. Microkernel vs. Hybrid kernels, device driver operation (with printing workflow example), system maintenance utilities, and language translators (Assembler, Compiler, Interpreter).

### 1.3 Application Software (`Completed`)
* **Architecture & Categories:** Definition of application software, the 8 major functional categories, and the separation between User Space, Kernel Space, and System Calls.
* **Program Execution:** The 5-step application execution lifecycle from SSD storage to RAM process creation, thread execution, syscall handling, and kernel response (with embedded `execution_lifecycle.png` diagram).
* **Development Approaches:** Architectural comparison and trade-offs between Native applications, Web applications, and Cross-Platform (Electron) applications, followed by 10 review questions and answers.

### 1.4 Module Synthesis & Self-Check Quiz (`Completed`)
* **Synthesis & Assessment:** Cross-chapter executive summary, 10 comprehensive assessment questions (Multiple-Choice and True/False), and a complete grading key with technical explanations.

---

## Part 2: Symbolic AI (Stage Two — Scheduled for Weeks 7–10)

### 2.1 What is Symbolic AI? (`Scheduled: 28 Oct 2026`)
* Introduction to Good Old-Fashioned AI (GOFAI), explicit knowledge representation, and rule-based decision making.

### 2.2 Types of Symbols and Knowledge Representation (`Scheduled: 30 Oct 2026`)
* Logical, non-logical, object, function, propositional, and action symbols; semantic networks and knowledge graphs.

### 2.3 How Symbolic AI Reasons (`Scheduled: 1 Nov 2026`)
* Inference engines, IF-THEN production rules, forward chaining (data-driven), and backward chaining (goal-driven) deduction.

### 2.4 Expert Systems in the Real World (`Scheduled: 3 Nov 2026`)
* Architecture of expert systems (Knowledge Base, Inference Engine, User Interface) and real-world case studies in medical diagnosis and engineering troubleshooting.

### 2.5 Strengths, Limits, and Hybrid Neuro-Symbolic AI (`Scheduled: 5 Nov 2026`)
* Comparing Symbolic AI with modern Machine Learning: explainability vs. adaptability, the knowledge acquisition bottleneck, and future neuro-symbolic systems.
