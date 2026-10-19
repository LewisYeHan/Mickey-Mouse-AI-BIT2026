# Team Project Plan and Task List
**Course:** Foundations of CS & AI (2026)  
**Team Name:** Mickey Mouse (`Mickey-Mouse-AI-BIT2026`)  
**Selected Module:** Computer Software Architecture (Operating Systems, System Software, and Application Software)  
**Repository URL:** `https://github.com/LewisYeHan/Mickey-Mouse-AI-BIT2026`

---

## A. Team Information and Responsibilities

### 1. Team Roster, Strengths, & Skills to Develop

| Member Name (as on Class Roster) | GitHub Username | Relevant Strengths & Experience | Skills to Develop in This Project | Assigned Primary Responsibilities |
| :--- | :--- | :--- | :--- | :--- |
| **Yeo Shih Jie** | `@ysjie03` | Repository management and Markdown formatting. | Git version control workflows and system-level resource tracking. | **Repository Lead & Section 1.1 Lead:** Manage repository structure and lead development of **1.1 Operating Systems**. |
| **Lu My Ky** | `@jojolu11` | Research and technical documentation structure. | Deepening technical understanding of low-level firmware and boot execution. | **Section 1.2 Lead:** Lead research and drafting for **1.2 System Software (BIOS, Firmware, Drivers)**. |
| **Cao Minh Tuan** | `@mnhtnc` | Analytical breakdown of software processes and interactions. | Explaining OS system calls and user/kernel space memory boundaries. | **Section 1.3 Lead:** Lead research and drafting for **1.3 Application Software & Execution**. |
| **Frederick Samuel Lesmana** | `@Ti4nCi` | Structured synthesis and assessment design. | Designing interactive test banks and comprehensive review summaries. | **Section 1.4 Lead:** Lead **1.4 Summary, Concept Map & Test Bank**. |
| **Wong Hiu Chung Samuel** | `@Samuel1940398` | Content checking and verification. | Technical peer review and testing beginner comprehension. | **Support & Review:** Assist with peer review verification and checking activity calculations. |
| **Goh Ye Han** | `@LewisYeHan` | Systems troubleshooting and project organization. | Coordinating documentation and self-contained submission packaging. | **Coordination & Documentation:** Assist with project plan management, logs, and final report assembly. |

### 2. Fair Workload Distribution Strategy
To ensure a balanced workload, each of the four content leads focuses on their assigned sub-sections (`1.1`, `1.2`, `1.3`, and `1.4`) during Stage 1. In Stage 2 and Stage 3, members take ownership of major production pillars (Study Guide compilation, PPT Slides, and Video Tutorials) while peer-reviewing teammate sections.

---

## B. Project Scope and Learning Goals

### 1. Target Learners & Assumed Background Knowledge
* **Target Audience:** First-year undergraduate students and true beginners taking *Foundations of CS & AI*.
* **Assumed Prerequisite Knowledge:** Learners are assumed to know what basic physical computer hardware components are—specifically the **CPU** (processor), **RAM** (temporary working memory), **Storage** (SSD/HDD), and **Peripherals** (keyboard, mouse, monitor). **No prior programming, terminal, or operating system kernel knowledge is assumed.**

### 2. Learning Goals
After studying our module materials, beginners will be able to:
1. **Classify** software into Low-Level System Software (BIOS/UEFI, firmware, device drivers), Operating Systems, and Application Software, and explain how they stack together from hardware to user.
2. **Explain** how an Operating System acts as a resource manager (allocating CPU time, managing RAM/virtual memory, monitoring performance, and coordinating device I/O) and why desktop OSs (Windows, macOS) differ from mobile OSs (Android).
3. **Trace** the step-by-step execution lifecycle when a user launches an application (from an inactive file on SSD storage $\rightarrow$ an active process in RAM $\rightarrow$ requesting hardware services from the OS via system calls).
4. **Apply** these concepts to diagnose everyday computing scenarios (e.g., distinguishing whether a slow computer or malfunctioning accessory is caused by RAM exhaustion, a missing device driver, or an application freeze).

### 3. Content Outline (Logical Bottom-Up Sequence)
* **Section 1.1: Operating Systems (Core V1.0 Developed Topic)**
  * What is an OS and the OS Kernel?
  * Core OS Functions: Resource Allocation (CPU & RAM), Device Management, and Performance Monitoring (Task Manager / Activity Monitor).
  * Platform Comparison: Architectural differences and design goals of Windows, macOS, Linux, and Android.
* **Section 1.2: Low-Level System Software**
  * The Role of System Software beneath and alongside the OS.
  * BIOS / UEFI and the Computer Boot Sequence (Power-On Self-Test to OS Bootloader).
  * Firmware (embedded permanent instructions) and Device Drivers (translating OS commands for specific hardware).
* **Section 1.3: Application Software & Execution**
  * What makes Application Software different from System Software?
  * How Applications Run: Programs on Disk vs. Active Processes and Threads in RAM.
  * The Relationship with the OS: Why apps cannot touch hardware directly (User Space vs. Kernel Space, APIs, and System Calls).
* **Section 1.4: Module Synthesis, Concept Map & Self-Assessment**
  * End-to-End Hardware-to-User Software Layer Model (Concept Map).
  * Self-Check Quiz (Multiple-Choice & True/False scenario questions with full step-by-step explained solutions).

### 4. Scope Boundaries & Uncertainties
* **Detailed Explanation (In Scope):** High-level conceptual mechanics of CPU time-slicing, RAM allocation/swapping, the boot sequence (BIOS $\rightarrow$ OS), device driver translation, and how applications request OS services.
* **Brief Introduction Only (Boundary):** Specific kernel architectures (monolithic vs. microkernel) and mobile sandboxing will only be introduced briefly for platform comparison. Mathematical CPU scheduling calculations and assembly-level interrupt vectors are **out of scope** to keep the material beginner-friendly.
* **Uncertainties Identified:** We plan to confirm with the teacher how deeply we should distinguish legacy **BIOS** from modern **UEFI** in Section 1.2, and the ideal number of test bank questions expected for the Stage 2 Study Guide.

---

## C. Planned Learning Resources and Mini Lecture

| Component | Initial Plan & Description |
| :--- | :--- |
| **1. Shared Markdown Content** | All explanations, terminology definitions, worked examples, custom diagrams (`assets/`), practice activities, explained answers, and verified references will be written and peer-reviewed in our GitHub repository (`content/` folder) first. |
| **2. Study Guide and Test Bank** | Exported and refined from our Markdown foundation into a structured, self-paced PDF guide following a consistent pedagogical pattern: Concept Explanation -> Terminology -> Diagram -> Worked Example -> Activity -> Solution. |
| **3. PPT Slides** | Designed to visually explain abstract software layers including hardware-to-software stack diagrams, RAM/CPU allocation diagrams, and boot sequence flowcharts. |
| **4. Video Tutorials** | Short, focused screen-recorded tutorials with clear voice narration demonstrating real-time task manager resource monitoring and application process execution. |
| **5. Live Mini Lecture** | • **Proposed Manageable Question:** *"What actually happens inside your computer in the 2 seconds after you double-click an app—and why doesn't one frozen app crash your whole laptop?"*<br>• **Planned Demo / Audience Activity:** A 60-second live interactive poll diagnosing a frozen laptop Task Manager screenshot, followed by a visual demo of OS memory isolation. |

---

## D. Workflow, Schedule, and Coordination

### 1. Stage Checkpoints & Internal Deadlines
* **Stage 1 (Oct 24, 2026):** Planning & Content Foundation (Team Project Plan, GitHub Repo & Markdown V1.0, Project Log, Personal Logs).
* **Stage 1.5 (Oct 30, 2026):** Live Status Report.
* **Stage 2 (Nov 7, 2026):** Complete Markdown V2.0, First Full Versions of Study Guide, PPT Slides, Video Tutorials, and Live Mini Lecture delivery.
* **Stage 3 (Nov 28, 2026):** Comprehensive Feedback Revision and Final Delivery Package.

### 2. Operational Workflow & Quality Control
* Content is drafted directly in `.md` files inside the `content/` folder on GitHub. Before approval, a second team member must inspect it against the Quality Checklist.
* Every member commits their own work using their individual GitHub account with clear, descriptive commit messages.
* Markdown serves as our single source of truth; any corrections are updated in `.md` files first before propagating to slides and videos.

---

## E. Master Task List

| ID | Task (Specific Action) | Expected Result / Deliverable | Responsible Member(s) | Internal Deadline | Status | Dependencies |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **S1-01** | Create shared GitHub repo, configure access, and invite members. | Live GitHub repo with all collaborators. | Yeo Shih Jie (Lead) | Oct 19, 2026 | `completed` | None |
| **S1-02** | Draft Team Project Plan, learning goals, scope, and task list. | Project Plan & `content/00_Project_Plan_and_Task_List.md`. | Goh Ye Han (Lead) | Oct 20, 2026 | `completed` | S1-01 |
| **S1-03** | Populate `README.md` with team roster, purpose, and structure. | Complete `README.md` on main branch. | Goh Ye Han | Oct 20, 2026 | `completed` | S1-01 |
| **S1-04** | Develop `content/00_Module_Outline.md` with sequence and status labels. | `content/00_Module_Outline.md` committed. | Yeo Shih Jie & Frederick Samuel | Oct 20, 2026 | `in progress` | S1-02 |
| **S1-05** | Fully develop V1.0 content for **1.1 Operating Systems**. | `content/01_Operating_Systems.md` + asset. | Yeo Shih Jie | Oct 21, 2026 | `in progress` | S1-04 |
| **S1-06** | Draft content for **1.2 System Software (BIOS, Firmware, Drivers)**. | `content/02_System_Software.md` + asset. | Lu My Ky | Oct 21, 2026 | `not started` | S1-04 |
| **S1-07** | Draft content for **1.3 Application Software**. | `content/03_Application_Software.md` + asset. | Cao Minh Tuan | Oct 21, 2026 | `not started` | S1-04 |
| **S1-08** | Draft concept map and quiz for **1.4 Summary**. | `content/04_Summary_and_Quiz.md` + asset. | Frederick Samuel | Oct 21, 2026 | `not started` | S1-04 |
| **S1-09** | Conduct Peer Review on V1.0 content and log outcomes. | GitHub commit/issue showing review fix. | Wong Hiu Chung Samuel & Yeo Shih Jie | Oct 22, 2026 | `not started` | S1-05 to S1-08 |
| **S1-10** | Compile Stage 1 Submission Report, render PDF, and verify ZIP. | Submission ZIP package tested. | Goh Ye Han (Lead) | Oct 23, 2026 | `not started` | S1-09 |
| **S1-11** | Finalize Project Log, Meeting Summaries, and Personal Logs. | Submitted Project & Personal Logs. | All Members | Oct 23, 2026 | `in progress` | S1-02 to S1-10 |
