# 2.4 Expert Systems

**Team Member:** Lu My Ky (`@jojolu11`)

**In this section:** [Introduction](#1-introduction) · [Components](#2-how-expert-systems-work) · [Making Decisions](#3-how-an-expert-system-makes-decisions) · [MYCIN, DENDRAL, XCON](#4-real-world-examples-of-expert-systems) · [vs. Traditional Programs](#5-expert-systems-vs-traditional-programs) · [Advantages](#6-advantages-of-expert-systems) · [Limitations](#7-limitations-of-expert-systems) · [Modern AI](#8-expert-systems-and-modern-ai) · [Key Takeaways](#9-key-takeaways) · [Lab: PC Clinic](#lab-professor-pixels-pc-clinic) · [Practice Questions](#10-practice-questions-and-answers) · [References](#11-references)

**Learning goals.** By the end of this section, you can:
* name the parts of an expert system and what each does;
* act as the inference engine: forward chain through a small rule base to a diagnosis and explain *why*;
* use MYCIN, DENDRAL and XCON to show what expert systems do well and where they fall short.

**Before you start:** this builds on rules as knowledge ([2.3](06_Knowledge_Representation.md) §4.5) and forward and backward chaining ([2.2](05_Logic_and_Reasoning.md) §4–5). For the Mission, recall from [1.1](../Part_1/01_System_Software.md) that a PC's start-up check (POST) reports hardware faults with beeps.

> **Pixel's Mission**  
> Byte opens a PC Clinic. The first PC beeps three times. Professor Pixel says: *"Let's put a technician's knowledge inside you."*  
> **Predict first:** If Byte knows five expert rules, which PCs will Byte still fail on? Write down your guess, then check it in the PC Clinic lab and at the start of §10.

---

## 1. Introduction

An **expert system** is a Symbolic AI program that solves problems in one narrow **domain**, such as diagnosing infections, by applying an expert's knowledge stored as explicit facts and rules. It is Symbolic AI's most important practical use.

---

## 2. How Expert Systems Work

An expert system has six parts (Figure 2.14); §3 shows them working on one case.

![Expert system architecture: the User talks to the User Interface, which talks to the Inference Engine in the center. The engine exchanges data with Working Memory (left), uses facts and rules from the Knowledge Base (below) and sends its reasoning to the Explanation Facility (right), which explains back through the User Interface. A Human Expert feeds Knowledge Acquisition, which updates the Knowledge Base. A dashed border marks the system; the User and the Human Expert are outside it](../images/expert_system_architecture.png)

*Figure 2.14: The parts of an expert system. The inference engine (pink) is the reasoning core.*

| Component | What it does |
|---|---|
| Knowledge Base | The domain's facts and rules. Wrong or missing rules mean wrong or missing answers. |
| Inference Engine | Fires rules whose conditions match the facts, deriving new facts by forward or backward chaining ([2.2](05_Logic_and_Reasoning.md) §4–5). If several match at once, **conflict resolution** (2.2 §8) picks one. |
| Working Memory | The facts of the current case (this patient, this PC); grows as rules fire. |
| User Interface | Where the user enters facts and sees results. |
| Explanation Facility | Lists the facts and rules behind a conclusion, so users can check it. |
| Knowledge Acquisition | Turns experts' knowledge into new or updated rules. |

---

## 3. How an Expert System Makes Decisions

A university expert system decides whether a student qualifies for a scholarship:

```text
Rule 1: IF GPA >= 3.8 THEN ExcellentAcademicPerformance
Rule 2: IF ExcellentAcademicPerformance AND CommunityService THEN ScholarshipEligible

Working memory: Student Alex, GPA 3.9, CommunityService true
```

Using **forward chaining**:

1. **Rule 1:** 3.9 ≥ 3.8, so the engine adds `ExcellentAcademicPerformance(Alex)`.
2. **Rule 2:** its first condition was added in Step 1 and its second, `CommunityService`, is in the input, so it adds `ScholarshipEligible(Alex)`.
3. No rule adds anything new, so the engine stops: **Alex qualifies.** The explanation facility can report "Rule 1, then Rule 2".

---

## 4. Real-World Examples of Expert Systems

### 4.1 MYCIN

**MYCIN** (Stanford University, 1970s) helped doctors identify certain bacterial infections and choose antibiotics. Its rules carried **certainty factors**, from −1 to +1, saying how strongly evidence supports a conclusion (not probabilities; [2.2](05_Logic_and_Reasoning.md) §9). It used **backward chaining**, starting from a possible infection and asking for the facts to confirm it, and answered "WHY" and "HOW" questions, an early explanation facility. In tests its advice compared well with specialists', but it was never used routinely in hospitals.

### 4.2 DENDRAL

**DENDRAL** (Stanford, from 1965; Edward Feigenbaum, Joshua Lederberg and Bruce Buchanan) is often called the first expert system. It used chemists' rules to work out which molecular structures could explain mass-spectrometer data. Like every expert system, it worked only on its one narrow task.

### 4.3 XCON

**XCON** (also called R1) was built by John McDermott at Carnegie Mellon University for Digital Equipment Corporation (DEC), starting in 1978, and was in everyday use at DEC from 1980. It configured VAX computers from customers' orders by **forward chaining**: from the order's facts, it applied rules choosing compatible components until the configuration was complete. As DEC's products kept changing, XCON grew to thousands of rules and became hard to maintain, the **maintenance** problem in §7.

---

## 5. Expert Systems vs. Traditional Programs

| Feature | Traditional Programs | Expert Systems |
|---|---|---|
| Knowledge | Mixed into the program's instructions. | Stored separately in a knowledge base, as explicit rules. |
| Decision-making | Fixed, step-by-step procedures. | The engine applies whichever rules match the facts. |
| Explanation | Individual decisions are hard to explain. | The explanation facility shows the rules used. |
| Updating | Changing behavior means changing the code. | Rules can be added or changed without touching the engine. |

This separation of knowledge and reasoning is the defining feature of expert systems.

---

## 6. Advantages of Expert Systems

| Advantage | Explanation |
|---|---|
| Consistency | Applies the same rules to similar cases every time. |
| Availability | Works when no human expert is present. |
| Knowledge Preservation | Keeps an expert's knowledge after the expert leaves. |
| Efficiency | Applies many rules quickly. |
| Explainability | Shows which rules led to a conclusion. |

---

## 7. Limitations of Expert Systems

| Limitation | Explanation |
|---|---|
| Limited Domain | Outside its narrow area, it has no answer. |
| Knowledge Acquisition | Turning experts' know-how into rules is slow and hard. |
| Limited Learning | It does not learn from new experience. |
| Maintenance | Rules must be updated by hand when knowledge changes. |
| Uncertainty | Incomplete or conflicting information makes decisions hard. |

Inaccurate rules lead to incorrect conclusions, so expert systems should support, not replace, human experts in high-risk decisions.

---

## 8. Expert Systems and Modern AI

| Feature | Expert Systems | Machine Learning |
|---|---|---|
| Knowledge | Explicit rules. | Patterns learned from data. |
| Adaptability | Rules are updated by hand. | Improves with more training. |
| Explanation | Reasoning can be traced rule by rule. | Often hard to explain. |
| Best for | Well-defined domains with clear rules. | Finding patterns in large amounts of data. |

### 8.1 Hybrid AI Systems

**Neuro-Symbolic AI** combines the two, for example:

1. A machine learning model spots signs of disease in medical images (pattern recognition).
2. A symbolic reasoning system applies medical knowledge and clinical rules to those findings.
3. The system recommends, citing the supporting rules.

---

## 9. Key Takeaways

* Core parts: **knowledge base** (rules), **inference engine** (reasoning), **working memory** (the case). Rules are separate from the engine, so experts update rules, not code.
* **MYCIN**: medicine, backward chaining, certainty factors. **DENDRAL**: chemistry, often called the first expert system. **XCON**: configured DEC computers, forward chaining.
* Strengths: consistent, available, explainable. Weaknesses: limited domain, hard knowledge acquisition, no learning, manual updates.
* **Neuro-Symbolic AI** combines machine learning's pattern recognition with symbolic reasoning.

---

## Lab: Professor Pixel's PC Clinic

* **Goal:** Be the inference engine: forward chain from facts to a diagnosis, explain it, and see what happens when no rule covers a case.
* **Preparation:** Paper and pen, about 20 minutes; re-read §2–3. The optional extension uses SWISH, a free online Prolog tool.
* **Task:** Byte's knowledge base has five rules (the beep chart is simplified; real codes differ by firmware maker, the kind of detail a real knowledge base must get right):

  ```text
  R1: IF BeepsAtStart AND BlackScreen THEN POSTFailed
  R2: IF POSTFailed AND ThreeBeeps THEN SuspectRAM
  R3: IF POSTFailed AND FiveBeeps THEN SuspectGraphicsCard
  R4: IF SuspectRAM THEN Advice: reseat the RAM, and replace it if the beeps continue
  R5: IF LoginScreenShows AND RunsSlowly AND RAMNearlyFull THEN Advice: close unused programs or add more RAM
  ```

  Three PCs arrive. Each list is that PC's **working memory**:

  ```text
  PC A: BeepsAtStart, ThreeBeeps, BlackScreen, FansSpin
  PC B: LoginScreenShows, RunsSlowly, RAMNearlyFull
  PC C: BlackScreen, NoLights, NoFanNoise
  ```

  **Step 1, predict:** which PC(s) will Byte fail to diagnose?  
  **Step 2, be the inference engine:** for each PC, check the rules in order (R1 to R5, and R6 once you add it). The first rule whose IF facts are **all** in working memory and whose THEN fact is **not** yet there fires: add its THEN fact and restart at R1. Stop when no rule adds a new fact (the stop rule from 2.2 §4). (The engine in the 2.2 lab checked every rule in a full pass before starting again. Restarting at R1 after each rule fires is another common strategy; both reach the same final facts here.)  
  **Step 3, be the explanation facility:** for PC A, answer the customer in one or two sentences: *"Why should I reseat the RAM?"*  
  **Step 4, update the knowledge base:** write a rule R6 that diagnoses PC C, and run PC C again, restarting at R1 and checking R1 to R6.
* **Observation:** For each PC, record the rules fired, in order, the final working memory, and why other rules did **not** fire.
* **Reflection:**
  1. Why did no rule fire for PC C? Does "no conclusion" mean "nothing is wrong"?
  2. In Step 4, did you change the inference engine, the knowledge base, or both? Why does it matter?
  3. Is `SuspectRAM` a proven fact, or advice a technician should check?
* **Optional extension (online, 5 minutes):** in [SWISH](https://swish.swi-prolog.org), create an empty **Program** and type in the left pane:

  ```prolog
  beeps(pc_a, 3).
  black_screen(pc_a).

  post_failed(PC) :- beeps(PC, N), N > 0, black_screen(PC).
  suspect_ram(PC) :- post_failed(PC), beeps(PC, 3).
  advice(PC, reseat_ram) :- suspect_ram(PC).
  ```

  Lines 1–2 are **facts** about PC A; the rest are **rules**, where `:-` means "if" and a comma means "and". Capitalised words (`PC`, `N`) are variables; every line ends with a full stop. Predict, then run `advice(pc_a, What).` and `advice(pc_c, What).` in the query box (bottom right). No SWISH? Use the answers below.

<details>
<summary><b>Feedback: check your diagnosis</b></summary>

* **PC A:** R1 adds `POSTFailed`. Restart: R1 adds nothing new, R2 adds `SuspectRAM`. Restart: R1–R2 add nothing, R3 fails (no `FiveBeeps`), R4 adds *reseat the RAM*. The next pass adds nothing, so Byte stops. Fired: **R1, R2, R4**; working memory ends with the four starting facts plus `POSTFailed`, `SuspectRAM` and the advice.
* **PC B:** R1–R4 do not match (no beeps, screen not black); R5 matches and fires: *close programs or add RAM*. Fired: **R5** (thrashing, from 1.2).
* **PC C:** **no rule fires.** R1 needs `BeepsAtStart`; the others need facts PC C lacks. Byte stops with **no conclusion**.
* **Step 3, for example:** "Your PC beeped and the screen stayed black, so the start-up check failed (R1). Three beeps point to the RAM (R2), and the first fix is to reseat it (R4)." Name facts and rules in the order used, as the explanation facility does.
* **Step 4, for example:** `R6: IF NoLights AND NoFanNoise THEN Advice: check the power cable and power supply`; now R6 fires. You changed only the **knowledge base**, not your checking method (the engine): the knowledge–reasoning separation of §5, and why maintenance means updating rules (§7).
* **Reflection answers:** (1) The fault is outside the five rules. "No conclusion" means "I have no rule for this", not "the PC is fine": the **limited domain** weakness (§7). (2) Only the knowledge base. (3) Neither a proven fact nor the advice itself: `SuspectRAM` is a rule-based suspicion from R2. R4 turns it into the advice *reseat the RAM*, and a technician should check it, especially when stakes are high.
* **Optional extension:** `advice(pc_a, What).` gives `What = reseat_ram`; `advice(pc_c, What).` gives `false`, since there are no facts about PC C. SWISH works back from the question to the facts (**backward chaining**, 2.2 §5); you worked forward. Both reach the same answer for PC A.

</details>

---

## 10. Practice Questions and Answers

**Mission check.** Byte fails on any PC its five rules do not describe (in the lab, PC C), and on new problems, unusual symptoms or two faults at once: the **limited domain** limitation (§7). The fix is to add rules, not to change the inference engine.

Try each question yourself first, then open the answers to check.

### Questions

*Understanding: 1–5 · Application: 6–8 · Critical thinking: 9–11*

**1.** What is an expert system?

**2.** What are the main components of an expert system?

**3.** What is the role of the inference engine?

**4.** Why is a knowledge base important?

**5.** What is the purpose of an explanation facility?

**6.** How would an expert system decide whether a student qualifies for a scholarship?

**7.** How do forward and backward chaining differ in an expert system?

**8.** How did MYCIN, DENDRAL and XCON apply expert knowledge to different domains?

**9.** Why might an expert system produce an incorrect conclusion?

**10.** Why are traditional expert systems limited when information changes constantly?

**11.** How could combining expert systems with machine learning improve AI applications?

<details>
<summary><b>Show answers</b> (try the questions first!)</summary>

**1.** A program that imitates a human expert in one domain, such as medicine, by applying stored expert rules with an inference engine.

**2.** Knowledge base (facts and rules), inference engine (applies them), working memory (facts of this case), user interface (input and results), explanation facility (how a conclusion was reached) and knowledge acquisition (gets knowledge from experts into the rules).

**3.** It matches the rules against the facts in working memory, decides which to fire and in what order (forward or backward chaining, conflict resolution), and so derives new facts and conclusions.

**4.** It holds all the expert knowledge: if it is incomplete or wrong, so are the conclusions, however good the engine.

**5.** It lists the facts and rules behind a conclusion, so users can trust it and experts can check the reasoning.

**6.** As in §3: the knowledge base holds the eligibility rules, working memory holds the student's details, the inference engine forward chains (GPA ≥ 3.8 gives ExcellentAcademicPerformance; that plus CommunityService gives ScholarshipEligible), and the explanation facility shows the rules used.

**7.** **Forward chaining** goes from known facts to conclusions; it suits configuration, where all data is known first (XCON). **Backward chaining** goes from a possible conclusion to the facts that would prove it; it suits diagnosis, testing one hypothesis at a time (MYCIN).

**8.** **MYCIN** used medical rules with certainty factors to identify bacterial infections and choose antibiotics. **DENDRAL** used chemists' rules to find molecular structures that explain mass-spectrometer data. **XCON** used engineering rules to pick compatible parts for DEC computers from customer orders.

**9.** Its rules or facts may be missing, wrong, or outdated; the user may enter wrong data, or the case may lie outside its domain. The engine follows the rules exactly, so wrong knowledge gives wrong conclusions.

**10.** People write the rules. When information changes often, the rules go out of date and must be fixed by hand, which is slow and expensive, because the system cannot learn new rules itself.

**11.** Machine learning finds patterns in messy data, such as signs of disease in images; the expert system applies explicit rules to them and explains its decisions. The result handles real-world data yet stays checkable.

</details>

---

## 11. References

1. Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
2. Buchanan, B. G., & Shortliffe, E. H. (1984). *Rule-Based Expert Systems: The MYCIN Experiments of the Stanford Heuristic Programming Project*. Addison-Wesley.
3. Feigenbaum, E. A. (1977). The art of artificial intelligence: Themes and case studies of knowledge engineering. *Proceedings of the Fifth International Joint Conference on Artificial Intelligence*.
4. Jackson, P. (1998). *Introduction to Expert Systems* (3rd ed.). Addison-Wesley.
5. Poole, D., & Mackworth, A. (2017). *Artificial Intelligence: Foundations of Computational Agents* (2nd ed.). Cambridge University Press. [Online textbook](https://artint.info/2e/html/ArtInt2e.html)

