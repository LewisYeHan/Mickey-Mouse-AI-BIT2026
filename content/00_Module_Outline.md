# Module Outline: Software and Symbolic AI

**Team:** Mickey Mouse · **Coordinator:** Yeo Shih Jie (`@ysjie03`)

**In this section:** Who This Module Is For · What You Need · What You Will Learn · Reading Order · Part 1 · Part 2 · How Each Section Works · Your Guides

---

## Who This Module Is For

First-year university students with no computer science background. You will learn how the software inside a computer works (Part 1) and how one classic kind of artificial intelligence reasons with rules (Part 2). Part 2 does not depend on Part 1, but Part 1 makes it easier.

## What You Need

* No programming experience. Every piece of code is given to you and explained.
* Basic computer skills: opening apps, using a browser, copying and pasting.
* Paper and a pen for the activities. A few activities work best with a partner.
* A laptop (Windows, macOS or Linux) for the optional computer activities. Every activity also has a paper version, so you can finish the module offline.

## What You Will Learn

By the end of the module you can:

1. Trace what happens from pressing the power button to the login screen (firmware, BIOS/UEFI, bootloader, kernel, drivers).
2. Explain how an operating system lets hundreds of programs share a few CPU cores, and work out when each process finishes under First Come First Served, Shortest Job First and Round Robin.
3. Explain processes, system calls, deadlock, virtual memory and file systems in your own words.
4. Describe the five steps that turn a file on the SSD into a running app, and compare native, web and cross-platform apps.
5. Explain what Symbolic AI is, and reason with facts and rules using Modus Ponens, forward chaining and backward chaining.
6. Represent the same knowledge with logic, semantic networks, frames, ontologies and knowledge graphs.
7. Act as the inference engine of a small expert system, and explain its strengths and limits.
8. Plan a sequence of actions with search (BFS, uniform-cost search, A\*), and choose a move in a simple game with minimax.

## Reading Order

Read the sections in order. The whole module takes about 12 hours, for example six sessions of 2 hours:

| Session | Read | Time |
| :--- | :--- | :--- |
| 1 | 1.1 System Software | 2 h |
| 2 | 1.2 Operating Systems | 2 h |
| 3 | 1.3 Application Software, 1.4 Glossary, 1.5 Summary and Quiz | 2 h |
| 4 | 2.1 What Is Symbolic AI?, 2.2 Logic and Reasoning | 2 h |
| 5 | 2.3 Knowledge Representation, 2.4 Expert Systems | 2 h |
| 6 | 2.5 Planning and Problem Solving, 2.6 Glossary, 2.7 Summary and Quiz | 2 h |

---

## Part 1: Software

### [1.1 System Software](Part_1/01_System_Software.md)
What system software is and its five kinds; the layers of a computer; firmware, BIOS vs. UEFI and the six steps of the boot process; the kernel and CPU modes; device drivers (with a printing example), utilities, and translators (assembler, compiler, interpreter). Practice questions with answers.

### [1.2 Operating Systems](Part_1/02_Operating_Systems.md)
What an OS is, kernel vs. shell, CLI vs. GUI. Processes, process states and threads; system calls and kernel designs; how hundreds of processes share a few cores (concurrency vs. parallelism); CPU scheduling with a worked FCFS, Round Robin and SJF example and the *Be the Scheduler* activity; deadlock; memory management; files and file systems; I/O and security. History, OS types and a platform comparison are included as *Going further* reading. Practice questions with answers.

### [1.3 Application Software](Part_1/03_Application_Software.md)
User space vs. kernel space, the 5-step execution lifecycle, and system calls. The types of applications, and native vs. web vs. cross-platform apps. Practice questions with answers.

### [1.4 Glossary](Part_1/Part_1_Glossary.md)
Every key term from Sections 1.1 to 1.3 in A–Z order, with the section where each term is explained.

### [1.5 Summary and Quiz](Part_1/Part_1_Summary_and_Quiz.md)
How Sections 1.1 to 1.3 connect, the key ideas from each section, and a 15-question self-check quiz (recall, application, true/false and scheduling) with an answer key.

---

## Part 2: Symbolic AI

### [2.1 What Is Symbolic AI?](Part_2/04_What_is_Symbolic_AI.md)
Symbols, facts and rules; how a rule-based system reaches a conclusion; Good Old-Fashioned AI (GOFAI) and the Physical Symbol System Hypothesis; where Symbolic AI is used; its strengths and limitations.

### [2.2 Logic and Reasoning](Part_2/05_Logic_and_Reasoning.md)
How AI derives conclusions from facts and rules: Modus Ponens and Modus Tollens, forward chaining, backward chaining, resolution and unification, conflict resolution, and reasoning under uncertainty (certainty factors, fuzzy logic, probability), with a short Python example.

### [2.3 Knowledge Representation](Part_2/06_Knowledge_Representation.md)
How AI stores knowledge: data, information and knowledge; propositional and predicate logic (with truth tables and De Morgan's laws); semantic networks, frames, scripts and rules; ontologies and knowledge graphs. Includes the *Build a Knowledge Web* lab.

### [2.4 Expert Systems](Part_2/07_Expert_Systems.md)
How expert systems work: the knowledge base, inference engine, working memory and explanation facility; MYCIN, DENDRAL and XCON; advantages, limitations and modern hybrid AI. Includes the *Dr. Pixel's PC Clinic* lab.

### [2.5 Planning and Problem Solving](Part_2/08_Planning_and_Problem_Solving.md)
How AI finds a sequence of actions that reaches a goal: states, actions with preconditions and effects (STRIPS), uninformed search (BFS, DFS, uniform-cost search), informed search (greedy best-first, A\*), adversarial search (minimax, alpha-beta pruning) and local search (hill climbing, simulated annealing), using a campus map example. Includes the *River Crossing* lab.

### [2.6 Glossary](Part_2/Part_2_Glossary.md)
Key terms from Sections 2.1 to 2.5, organized into seven groups: foundations, knowledge representation, logical reasoning, uncertainty, expert systems, AI approaches and evaluation, and planning and search.

### [2.7 Summary and Quiz](Part_2/Part_2_Summary_and_Quiz.md)
How Sections 2.1 to 2.5 connect through one scholarship example, the key ideas from each section, and a 21-question self-check quiz with explanations in the answer key.

---

## How Each Section Works

Each teaching section (1.1 to 1.3 and 2.1 to 2.5) starts with its learning goals and what to read first, then explains the ideas with examples and figures, and ends with practice questions. The glossaries (1.4, 2.6) and summaries (1.5, 2.7) review the whole part. The answer to each question comes after the questions, so try them first. In the PDF copy, the answers inside fold-out boxes are printed open.

## Your Guides

From 2.3 onward, two characters appear. **Professor Pixel** runs the computing lab: he sets each section's *Pixel's Mission*, a short problem to think about before you read. **Byte** is the lab's new robot intern. Byte follows instructions exactly and takes everything literally, which makes Byte a good picture of a computer. The characters are only there to make the examples memorable; the definitions are always in the main text and the glossaries.
