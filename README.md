<p align="center">
  <img src="content/images/banner.svg" alt="Team Mickey Mouse: Software & Symbolic AI" width="100%">
</p>

# Mickey Mouse Team: Software and Symbolic AI

**Final version: Markdown V3.0** · Git tag `v3.0-final` · snapshot of 28 Nov 2026 (the full commit ID is in [`VERSION.txt`](VERSION.txt) in the submitted package and in our submission report)

## About This Project

| | |
| :--- | :--- |
| **Course** | Foundations of CS & AI, Beijing Institute of Technology (2026) |
| **Team** | Mickey Mouse |
| **Module** | Part 1: Software · Part 2: Symbolic AI |
| **Intended learners** | First-year university students with no computer science background |
| **Prerequisites** | None. Basic computer use (apps, a browser, copy and paste). No programming needed |
| **Time** | About 12 hours, for example six sessions of 2 hours |

**Purpose.** This repository holds all the learning material for our module. We write everything in Markdown here first, check it, and then build the Study Guide, Test Bank, slides and videos from it. If we find a mistake in one of those resources, we fix it here first and then update the others.

## Learning Goals

By the end of the module, a learner can:

1. Trace what happens from pressing the power button to the login screen.
2. Explain how an operating system lets hundreds of programs share a few CPU cores, and work out when each process finishes under First Come First Served, Shortest Job First and Round Robin.
3. Explain processes, system calls, deadlock, virtual memory and file systems in their own words.
4. Describe how a file on the SSD becomes a running app, and compare native, web and cross-platform apps.
5. Explain what Symbolic AI is, and reason with facts and rules using Modus Ponens, forward chaining and backward chaining.
6. Represent the same knowledge with logic, semantic networks, frames, ontologies and knowledge graphs.
7. Act as the inference engine of a small expert system, and explain its strengths and limits.
8. Plan a sequence of actions with search (BFS, uniform-cost search, A\*), and choose a game move with minimax.

## Start Here

Open **[`content/00_Module_Outline.md`](content/00_Module_Outline.md)** first. It explains who the module is for and how each section works. Then read the sections in this order:

| Order | Section | File |
| :--- | :--- | :--- |
| 1 | 1.1 System Software | [`content/Part_1/01_System_Software.md`](content/Part_1/01_System_Software.md) |
| 2 | 1.2 Operating Systems | [`content/Part_1/02_Operating_Systems.md`](content/Part_1/02_Operating_Systems.md) |
| 3 | 1.3 Application Software | [`content/Part_1/03_Application_Software.md`](content/Part_1/03_Application_Software.md) |
| 4 | 1.4 Part 1 Glossary | [`content/Part_1/Part_1_Glossary.md`](content/Part_1/Part_1_Glossary.md) |
| 5 | 1.5 Part 1 Summary and Quiz | [`content/Part_1/Part_1_Summary_and_Quiz.md`](content/Part_1/Part_1_Summary_and_Quiz.md) |
| 6 | 2.1 What Is Symbolic AI? | [`content/Part_2/04_What_is_Symbolic_AI.md`](content/Part_2/04_What_is_Symbolic_AI.md) |
| 7 | 2.2 Logic and Reasoning | [`content/Part_2/05_Logic_and_Reasoning.md`](content/Part_2/05_Logic_and_Reasoning.md) |
| 8 | 2.3 Knowledge Representation | [`content/Part_2/06_Knowledge_Representation.md`](content/Part_2/06_Knowledge_Representation.md) |
| 9 | 2.4 Expert Systems | [`content/Part_2/07_Expert_Systems.md`](content/Part_2/07_Expert_Systems.md) |
| 10 | 2.5 Planning and Problem Solving | [`content/Part_2/08_Planning_and_Problem_Solving.md`](content/Part_2/08_Planning_and_Problem_Solving.md) |
| 11 | 2.6 Part 2 Glossary | [`content/Part_2/Part_2_Glossary.md`](content/Part_2/Part_2_Glossary.md) |
| 12 | 2.7 Part 2 Summary and Quiz | [`content/Part_2/Part_2_Summary_and_Quiz.md`](content/Part_2/Part_2_Summary_and_Quiz.md) |

The Part 2 file names start at `04` because they were numbered before the Part 1 files were split out. The section number (2.1 to 2.7) is what matters.

## Folder Guide

| Folder or file | What is inside |
| :--- | :--- |
| `README.md` | This page |
| `VERSION.txt` | The final version label; Git fills in the commit ID when the snapshot is exported |
| `content/` | All the learning content: the Module Outline, `Part_1/` and `Part_2/` |
| `content/images/` | Every figure, photo and lab screenshot used in the content (each one is listed in `docs/Figure_Sources.md`) |
| `activities/be_the_scheduler/` | The *Be the Scheduler* game from our mini lecture, used in 1.2 Section 8. Opens offline |
| `docs/Figure_Sources.md` | Who made each figure, how, and its source |
| `docs/Resource_Mapping.md` | Where each topic appears in the Study Guide, Test Bank, slides and videos |
| `docs/Changelog.md` | The main changes in each version |
| `docs/project/` | The team's project plan and task list (a project record, not learning content) |

## Learning Resources Built From This Content

These were submitted under their own assignments and are not stored in this repository. [`docs/Resource_Mapping.md`](docs/Resource_Mapping.md) shows which topic appears where.

| Resource | Submitted as | Files |
| :--- | :--- | :--- |
| Study Guide and Test Bank V1.0 | *Study Guide and Test Bank V1.0* | `MickeyMouse_Stage2_StudyGuide_V1.pdf`, `MickeyMouse_Stage2_TestBank_V1.docx` |
| PPT Slides V1.0 (159 slides) | *PPT Slides V1.0* | `MickeyMouse_Stage2_PPT_V1.pptx` |
| Video Tutorials V1.0 | *Video Tutorials V1.0* | `MickeyMouse_Video01_Software.mp4` (19:47), `MickeyMouse_Video02_SymbolicAI.mp4` (15:50), `MickeyMouse_Video03_SymbolicAI.mp4` (16:50) |
| Mini lecture SW3 | Mini lecture assignment | Pre-recorded video, slides and the *Be the Scheduler* game (online copy: <https://schedulercpu.netlify.app>) |

**Part 1 numbering.** These resources were made before Stage 3, when Operating Systems was 1.1 and System Software was 1.2. In this final version the two are swapped: their old 1.1 is our 1.2, and their old 1.2 is our 1.1.

## How to Open the Materials

* **On GitHub:** click any file in the table above. GitHub shows the formatted page with its figures.
* **Offline:** open this folder in Visual Studio Code and press `Ctrl + Shift + V` (`Cmd + Shift + V` on a Mac) on any `.md` file to see it formatted. Typora or any other Markdown viewer also works. All links and images are relative, so they work from any folder.
* **PDF:** the submitted package includes the whole module as one PDF, in reading order, with every answer shown.
* **Answers:** practice answers, quiz answer keys and lab feedback are inside fold-out boxes. Click the title of a box (for example *Show answers*) to open it. The PDF prints them all open.
* **Activities:** to play *Be the Scheduler*, double-click `activities/be_the_scheduler/index.html`. The labs in 1.1 and 1.3 use tools built into Windows (System Information, Device Manager and Task Manager), with a note for Mac users. The 2.1 lab uses an online copy of ELIZA, <https://www.masswerk.at/elizabot/eliza.html>. The 2.2 lab runs a short Python program in IDLE or any online Python editor. The 2.4 Prolog extension uses the free website <https://swish.swi-prolog.org>. Every lab and activity has a no-computer fallback: its feedback box shows the expected results.

## Team

| Member | Role | Main sections (final numbering) | GitHub |
| :--- | :--- | :--- | :--- |
| Yeo Shih Jie (杨世杰) | CEO, coordinator | Module Outline, 2.5 Planning and Problem Solving, project plan | [@ysjie03](https://github.com/ysjie03) |
| Cassinis Soulisack (苏浩然) | CIO, repository and submission checks | 1.1 System Software | [@DiegoSmiley](https://github.com/DiegoSmiley) |
| Cao Minh Tuan (高明俊) | Content lead | 1.2 Operating Systems, 2.3 Knowledge Representation | [@mnhtnc](https://github.com/mnhtnc) |
| Frederick Samuel Lesmana (梁天赐) | Content lead | 1.2 Operating Systems, 2.2 Logic and Reasoning | [@Ti4nCi](https://github.com/Ti4nCi) |
| Lu My Ky (吕美琪) | Video and content lead | 1.3 Application Software, 2.4 Expert Systems | [@jojolu11](https://github.com/jojolu11) |
| Wong Hiu Chung Samuel (王晓聪) | Visual lead | 2.1 What Is Symbolic AI?, 1.5 summary, Part 2 diagrams | [@Samuel940398](https://github.com/Samuel940398) |
| Goh Ye Han (吴宇航) | Quality lead, repository owner | 1.5 quiz, 2.6 glossary, 2.7 summary and quiz, reviews | [@LewisYeHan](https://github.com/LewisYeHan) |

Each section file names its writers at the top. The Git history shows who committed each change.

## Version History

| Version | Date | Git tag | What it was |
| :--- | :--- | :--- | :--- |
| **V3.0 Final** | 28 Nov 2026 | `v3.0-final` | Final Markdown content (Stage 3). See [`docs/Changelog.md`](docs/Changelog.md) |
| V2.0 | 7 Nov 2026 | `v2.0-stage2` | Stage 2: Part 2 written, Part 1 expanded |
| V1.0 | 27 Oct 2026 | `v1.0-stage1` | Stage 1 resubmission: Part 1 |

### Main changes since Stage 2

| Feedback | What we changed | Where |
| :--- | :--- | :--- |
| Teacher: system software should go before operating system | Part 1 reordered; System Software is now 1.1 | `content/Part_1/` |
| Teacher: more images and figures for the other resources to build on | Six new or redrawn figures in Part 1; chaining figures in 2.2 | `content/images/`, 1.1, 1.2, 1.5, 2.2 |
| Teacher (PPT): more real images, not only AI-generated ones | Disney-silhouette figures replaced; real photos of a CPU, BIOS chip, RAM, SSD and Deep Blue; real screenshots in Figure 1.4 and the labs; credits for every image | 1.1, 1.2, 1.3, 2.5, `docs/Figure_Sources.md` |
| Mini lecture SW3 | Scheduling worked example, concurrency vs. parallelism, *Be the Scheduler* activity with an offline copy | 1.2 Section 8, `activities/` |
| Teacher (general Stage 2 feedback): clickable contents, answers kept apart from exercises, activities with real tools and screenshots | Linked contents at the top of every section; practice answers moved into fold-out boxes; four new hands-on labs | 1.1, 1.3, 2.1 and 2.2 labs; every teaching section |
| Own review | Files and file systems; 2.2 logic fixes; 2.1 strengths and limitations; learning goals in every teaching section; new Module Outline | See `docs/Changelog.md` |

## Known Limitations

* The Study Guide, Test Bank, PPT and videos (V1.0) still use the old Part 1 numbering, and the Study Guide still contains the two old Part 1 figures. Video 1 teaches Operating Systems before System Software (System Software starts at 11:40).
* A few wording differences remain in those resources, for example Test Bank MC16 and PPT slide 101 say "both rules fire" where 2.2 now says the rules *match* and one *fires*. All known differences are listed in `docs/Resource_Mapping.md`.
* The original source and licence of the historical photo in Figure 2.3 (an IBM 7090 set up to play chess) have not been confirmed.
* Some Study Guide labs (for example Prolog Family Detective and Little Man Computer) are in the Study Guide only, not in this Markdown.
* The online copy of *Be the Scheduler*, the online ELIZA, online Python editors and the SWISH website need internet. Each has an offline alternative: the local game file, IDLE, or the expected results in the feedback boxes.
* The labs in 1.1 and 1.3 give full steps for Windows only. Mac users get a short note and can use the expected results in the feedback.

## How We Work

* **One section, one owner.** Each section names its writers at the top. In Stages 1 and 2, each writer committed their own section from their own GitHub account. The Stage 3 revisions were made and committed by Yeo Shih Jie.
* **Review.** Before each submission, members check one another's sections and record the results in the submission report.
* **Clear commit messages.** Say what changed and where, for example `1.2 Section 8: add scheduling worked example (mini lecture)`.
* **Markdown is the source.** If an error is found in the slides, Study Guide or videos, we fix it here first and then update every affected resource.
