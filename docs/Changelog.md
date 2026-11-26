# Changelog

The full history is in the Git log. This file lists the main changes between versions. Each version is also marked with a Git tag, so two versions can be compared with `git diff v2.0-stage2 v3.0-final`.

## V3.0 Final (Stage 3, 28 Nov 2026), tag `v3.0-final`

**Teacher feedback on Markdown V2.0**

* Part 1 reordered: System Software is now 1.1 and Operating Systems is 1.2 ("system software should go before operating system"). Files renamed (their history is kept); titles, figures, glossary, quiz tags and every link updated. Kernel designs moved into 1.2 so they are taught once.
* More figures for the other resources to build on: process states (Figure 1.3), a Task Manager screenshot (1.4), the FCFS / Round Robin / SJF comparison (1.5), a folder tree (1.8), a redrawn concept map (1.10), and the forward and backward chaining figures in 2.2 (2.4, 2.5) in place of Mermaid code.

**General Stage 2 feedback (navigation, answers and activities)**

* Clickable contents: the "In this section" line at the top of 1.1, 1.2, 1.3, 1.5, 2.1, 2.2 and the Module Outline now links to every heading, as 2.3 to 2.7 already did.
* Answers no longer sit directly after the exercises: the practice answers in all eight teaching sections are now in fold-out boxes, like the quiz answer keys and lab feedback. The PDF copy prints them open.
* Four new hands-on labs that use real tools, each with steps, an observation task, reflection questions, feedback and a no-computer fallback: *Find Your Computer's System Software* (1.1, Windows System Information and Device Manager), *Follow an App from File to Process* (1.3, Task Manager), *Chat with ELIZA* (2.1, an online copy of the 1966 chatbot) and *Run a Forward-Chaining Engine in Python* (2.2, with a screenshot of the program running).

**Teacher feedback on PPT V1.0 and Stage 1 feedback**

* The two figures with Disney character silhouettes and ALL-CAPS text were replaced with redrawn diagrams that match the text (Figures 1.1 and 1.2). The boot figure's steps now match the six numbered steps.
* `docs/Figure_Sources.md` added: every figure with who made it, how, and its source.

**Mini lecture SW3**

* 1.2 Section 8 now has the mini lecture's content: the Task Manager hook, the chess simul analogy, concurrency vs. parallelism, waiting and finish times, a worked example with jobs A = 3, B = 2 and C = 1 under three methods, starvation, context-switch cost and the time-slice trade-off.
* The *Be the Scheduler* game is in `activities/be_the_scheduler/` and opens offline, with a paper version and answers in 1.2.

**Own review and consistency checks**

* New 1.2 Section 10, Files and File Systems, with practice questions and glossary terms.
* 2.2: a logic-symbol table before the symbols are used; `∀x` added; the forward-chaining stop rule corrected ("until no rule adds a new fact"); conflict resolution now says rules *match* and one *fires*, with a genuinely more specific Rule 2; a worked resolution-by-contradiction example and a numeric Bayes example.
* 2.1: Strengths and Limitations table (replacing a link to a deleted file) and the Physical Symbol System Hypothesis. 2.5: STRIPS named. 2.7: the scholarship story now describes 2.1 correctly (Merit Scholarship for Sammy, Excellence Scholarship for Alex).
* Learning goals and "Before you start" added to 1.1, 1.2, 1.3, 2.1 and 2.2, so every teaching section (1.1–1.3, 2.1–2.5) now has them.
* 2.7: the closing note moved here from the Module Outline, as "A Note from Team Mickey Mouse".
* Part 1 quiz: two scheduling questions added (15 questions).
* Module Outline rewritten with intended learners, prerequisites, learning outcomes, a reading order and correct section descriptions.
* README rewritten for the final version; student ID numbers removed.
* Project plan moved from `content/` to `docs/project/` and corrected; unused and duplicate images removed; draft status markers removed.

## V2.0 (Stage 2, 7 Nov 2026), tag `v2.0-stage2`, commit `0070044`

* Part 2 (Symbolic AI) written: 2.1 to 2.5, glossary, summary and 21-question quiz, with labs in 2.3 to 2.5.
* Part 1 moved into `content/Part_1/` and expanded; glossary and summary added.
* 2.5 Strengths and Limits and 2.7 NLP were planned but dropped on 5 Nov to keep the scope to lecture chapter 4.

## V1.0 (Stage 1 resubmission, 27 Oct 2026), tag `v1.0-stage1`, commit `95f1d18`

* Part 1 (Software) written: Operating Systems, System Software, Application Software, summary.
* ASCII diagrams replaced with images after Stage 1 feedback.
