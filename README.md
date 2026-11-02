<p align="center">
  <img src="content/images/banner.svg" alt="Team Mickey Mouse: Software & Symbolic AI" width="100%">
</p>

# Mickey Mouse — Software & Symbolic AI

## About this project

| | |
|---|---|
| Course | Foundations of CS & AI (2026) |
| Team | Mickey Mouse |
| Module | Part 1: Software · Part 2: Symbolic AI |
| Intended learners | First-year students with no CS background |
| Deliverables | Markdown content V2.0 · Study Guide & Test Bank · PPT slides · Video tutorials |
| Current stage | Stage 2 — Markdown V2.0 (due 7 Nov 2026, 23:59 Beijing time) |
| Last updated | 2 Nov 2026 |

**Purpose.** This repo holds all the learning material for our module. We write everything in Markdown here first, review it, and then build the study guide, test bank, slides and videos from it. If we find a mistake while making the slides or video, we fix it here first, then update the other resources.

**How to use this repo as a learner.** Start with [`00_Module_Outline.md`](content/00_Module_Outline.md), then read the sections in number order. Each section ends with practice questions and answers.

## Team

| Member | Student ID | Role | Main job | Sections written | GitHub |
|---|---|---|---|---|---|
| Yeo Shih Jie (杨世杰) | 1820262289 | CEO | Plan, task tracker, coordination | — | @ysjie03 |
| Cassinis Soulisack (苏浩然) | 1820262224 | CIO | Repo setup, submission checks | 1.2, 2.5 | @DiegoSmiley |
| Cao Minh Tuan (高明俊) | 1820262251 | Content lead | Content writing | 1.1, 2.2 | @mnhtnc |
| Frederick Samuel Lesmana (梁天赐) | 1820262240 | Content lead | Content writing, study guide | 1.1, 2.3 | @Ti4nCi |
| Lu My Ky (吕美琪) | 1820262269 | Video & content lead | Content writing, video | 1.3, 2.4 | @jojolu11 |
| Wong Hiu Chung Samuel (王晓聪) | 1820262001 | Visual lead | Diagrams, slide template | 1.4 summary, 2.1 | @Samuel940398 |
| Goh Ye Han (吴宇航) | 1820262002 | Quality lead | Proofreading, quizzes, reviews | 1.4 quiz, Part 2 quiz | @LewisYeHan |

## Folder structure

    .
    ├── README.md                              ← you are here
    └── content/
        ├── 00_Module_Outline.md               ← start here
        ├── 00_Project_Plan_and_Task_List.md   ← tasks, owners, status
        │
        │   Part 1: Software
        ├── 01_Operating_Systems.md            ← 1.1
        ├── 02_System_Software.md              ← 1.2
        ├── 03_Application_Software.md         ← 1.3
        ├── Part_1_Summary_and_Quiz.md         ← 1.4, Part 1 summary + quiz with answers
        ├── Part_1_Glossary.md                 ← A–Z key terms (Parts 1)
        │
        │   Part 2: Symbolic AI
        ├── 04_What_is_Symbolic_AI.md          ← 2.1
        ├── 05_Knowledge_Representation.md     ← 2.2
        ├── 06_How_Symbolic_AI_Reasons.md      ← 2.3
        ├── 07_Expert_Systems.md               ← 2.4
        ├── 08_Strengths_and_Limits.md         ← 2.5
        ├── Part2_Summary_and_Quiz.md          ← Part 2 summary + quiz with answers
        ├── Part_2_Glossary.md                 ← A–Z key terms (Parts 2)
        │
        └── images/
            ├── banner.svg                     ← README banner
            ├── system_layers.jpeg             ← Figure 1.1
            ├── round_robin.jpeg               ← Figure 1.2
            ├── memory_hierarchy.jpeg          ← Figure 1.3
            ├── boot_process.jpeg              ← Figure 1.4
            ├── execution_lifecycle.png        ← Figure 1.5
            └── concept_map.png                ← Figure 1.6

Each content file follows the same pattern: explanation → worked example → diagram (where useful) → practice questions with answers → references → reviewer note.

## Current progress

Status labels: ✅ written and checked by a reviewer · 📝 drafted, not yet reviewed · 🔲 not started

| Part | Writer | Reviewer | Status |
|---|---|---|---|
| README and repo setup | Cassinis Soulisack (Stage 1), Frederick Samuel Lesmana (Stage 2 update) | — | 📝 |
| Module outline | Yeo Shih Jie | Goh Ye Han | ✅ |
| Project plan and task list | Yeo Shih Jie (Stage 1), Frederick Samuel Lesmana (Stage 2 update) | — | 📝 |
| 1.1 Operating Systems | Cao Minh Tuan, Frederick Samuel Lesmana | Goh Ye Han | ✅ |
| 1.2 System Software | Cassinis Soulisack | Goh Ye Han | ✅ |
| 1.3 Application Software | Lu My Ky | Goh Ye Han | ✅ |
| 1.4 Summary and Quiz | Wong Hiu Chung Samuel (summary), Goh Ye Han (quiz) | Goh Ye Han (summary) | ✅ |
| 2.1 What is Symbolic AI? | Wong Hiu Chung Samuel | Goh Ye Han | 🔲 |
| 2.2 Knowledge Representation | Cao Minh Tuan | Goh Ye Han | 🔲 |
| 2.3 How Symbolic AI Reasons | Frederick Samuel Lesmana | Goh Ye Han | 🔲 |
| 2.4 Expert Systems | Lu My Ky | Goh Ye Han | 🔲 |
| 2.5 Strengths and Limits | Cassinis Soulisack | Goh Ye Han | 🔲 |
| Part 2 Summary and Quiz | Goh Ye Han | — | 🔲 |
| Glossary updated with Part 2 terms | Goh Ye Han | — | 🔲 |
| Part 2 diagrams | Wong Hiu Chung Samuel | — | 🔲 |
| Study Guide & Test Bank 1.0 | Frederick Samuel Lesmana, Cao Minh Tuan | — | 🔲 |
| PPT slides 1.0 | Wong Hiu Chung Samuel, Lu My Ky | — | 📝 |
| Video tutorials 1.0 | Lu My Ky | — | 🔲 |

See [`00_Project_Plan_and_Task_List.md`](content/00_Project_Plan_and_Task_List.md) for due dates and the full task list.

## Changes since Stage 1

| Feedback or problem | What we changed | Where |
|---|---|---|
| Placeholders left in the report | Filled in every placeholder | Stage 1 submission report |
| Content was incomplete | Rewrote bullet notes as full explanations; added a written summary | `01`–`04` |
| AI-made ASCII diagrams | Replaced them with real images, each with a caption | `content/images/`, `01`–`03` |
| PDF showed raw Markdown | Re-exported so headings, tables and images display properly | Content PDF |
| Part 2 (Symbolic AI) not yet written | Writing sections 2.1–2.5 with examples, activities and answers | `06`–`11` |

## How we work

- **One section, one owner.** Each writer commits their own section from their own GitHub account, so contributions are traceable.
- **Clear commit messages.** Say what changed and where, e.g. `2.3: add forward-chaining worked example + 3 practice questions`.
- **Peer review.** Every core section is checked by someone who did not write it. The reviewer adds a short "Reviewed by" note at the end of the file.
- **Markdown is the source of truth.** If an error is found in the slides, study guide or video, we fix it here first and then update every affected resource.
