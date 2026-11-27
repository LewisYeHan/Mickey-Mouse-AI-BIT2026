# 2.7 Module Summary & Self-Check Quiz

**Team Member:** Goh Ye Han (`@LewisYeHan`)

**In this section:** [How It All Connects](#1-how-it-all-connects) · [Key Ideas from Each Section](#2-key-ideas-from-each-section) · [Quiz (21 questions)](#3-self-check-quiz) · [Answer Key](#4-answer-key) · [References](#5-references)

**Learning goals.** By the end of this section, you can:
* explain how Sections 2.1 to 2.5 connect, using one scholarship example;
* check your understanding of every Part 2 section and lab with a 21-question quiz.

> **Pixel's Mission**  
> Professor Pixel gives Byte one last case: decide whether Alex qualifies for a scholarship, then plan Alex's application.  
> **Predict first:** Which Part 2 sections will Byte need? Write down your guess, then check it in §1.

---

## 1. How It All Connects

Follow one AI through the module: it decides whether Alex qualifies for a scholarship, then helps Alex apply.

**2.1 Symbolic AI: write knowledge down.** Instead of learning from examples, the system is given explicit facts and rules. In 2.1, Sammy's facts (`GPA(Sammy, 3.8)`, attendance 95%) and the Merit Scholarship rule (GPA ≥ 3.5 and attendance ≥ 90%) are enough to conclude `ScholarshipEligible(Sammy)`. From 2.2 on, we follow Alex and the Excellence Scholarship: the fact `GPA(Alex, 3.9)` and the rule "IF GPA ≥ 3.8 THEN ExcellentAcademicPerformance".

**2.2 Logic and Reasoning: draw conclusions.** Modus Ponens turns that fact and rule into a new fact. Forward chaining repeats this until no rule adds a new fact; backward chaining starts from the goal "Is Alex eligible?" and seeks facts that prove it. Conflict resolution picks a rule when several match; certainty factors and fuzzy logic handle unsure facts.

**2.3 Knowledge Representation: organize what is known.** The same knowledge can be stored as predicate logic (`GPA(Alex, 3.9)`), a semantic network, a frame, rules, an ontology or a knowledge graph, each suited to a different job.

**2.4 Expert Systems: package it.** Rules go into a knowledge base, Alex's details into working memory, and an inference engine chains through them; the explanation facility shows why Alex qualifies. If the requirements change but the rules do not, the answer is wrong.

**2.5 Planning and Problem Solving: act on it.** To apply, Alex must submit a transcript, get a reference and attend an interview. A planner describes each step by its preconditions and effects and searches (BFS, uniform-cost search, A\*) for an order that reaches "application complete".

**The big idea:** represent knowledge explicitly, reason with it, plan with it. The result explains itself, but is only as good as the knowledge people maintain.

---

## 2. Key Ideas from Each Section

| Section | Main question | Key ideas |
| :--- | :--- | :--- |
| **2.1 Symbolic AI** | What is Symbolic AI? | Symbols, facts, rules, logic, explicit knowledge, GOFAI |
| **2.2 Logic and Reasoning** | How does AI reach conclusions? | Modus Ponens, Modus Tollens, forward and backward chaining, resolution, unification, conflict resolution, certainty factors, fuzzy logic, probability |
| **2.3 Knowledge Representation** | How does AI store knowledge? | Propositional logic, De Morgan's laws, predicate logic, semantic networks, frames and scripts, rules, ontologies, knowledge graphs |
| **2.4 Expert Systems** | How is symbolic reasoning applied? | Knowledge base, inference engine, working memory, user interface, explanation facility, knowledge acquisition, MYCIN, DENDRAL, XCON, limitations, Neuro-Symbolic AI |
| **2.5 Planning and Problem Solving** | How does AI find a sequence of actions? | States, actions, preconditions and effects, BFS, DFS, uniform-cost search, heuristics, greedy best-first search, A\*, minimax, alpha-beta pruning, hill climbing, simulated annealing |

**Symbolic AI vs. machine learning:** Symbolic AI reasons with hand-written facts and rules, so it is easy to explain but must be maintained by people; machine learning learns patterns from data, so it handles messy data but is harder to explain. **Neuro-Symbolic AI** combines the two (2.4 §8.1).

**Labs to revisit before the quiz:** *Build a Knowledge Web* (2.3), *Professor Pixel's PC Clinic* (2.4) and *The River Crossing* (2.5). Part D checks them; each question gives all the information you need.

---

## 3. Self-Check Quiz

Try all 21 questions, then check Section 4. Part A checks key concepts, Parts B and C apply and evaluate them, and Part D checks the labs in 2.3–2.5. Each of 2.1–2.5 has at least four questions.

### Part A: Multiple Choice

**Q1. What is the main characteristic of Symbolic AI?**

* A) It learns all knowledge by trial and error.
* B) It represents knowledge with symbols, facts, rules and logic.
* C) It relies entirely on neural networks.
* D) It reaches conclusions without storing knowledge.

**Q2. Which method describes objects, their properties and their relationships with logical predicates?**

* A) Propositional Logic
* B) Predicate Logic
* C) Semantic Networks
* D) Frames

**Q3. What is a knowledge graph mainly for?**

* A) Training neural networks with numerical weights.
* B) Storing programs as executable instructions.
* C) Representing entities and their relationships as connected information.
* D) Running rules without storing facts.

**Q4. Which reasoning method starts from known facts and repeatedly applies rules to derive new conclusions?**

* A) Backward Chaining
* B) Unification
* C) Resolution
* D) Forward Chaining

**Q5. Which expert-system component applies rules to the available facts?**

* A) User Interface
* B) Inference Engine
* C) Knowledge Acquisition
* D) Working Memory

**Q6. Which is a major limitation of traditional Symbolic AI?**

* A) It cannot represent facts.
* B) It cannot use logical rules.
* C) Its knowledge must be explicitly represented and maintained.
* D) It cannot explain any of its conclusions.

### Part B: Apply It

**Q7. Fact: P is true. Rule: if P is true, then Q is true. What follows by Modus Ponens?**

* A) P is false.
* B) Q is true.
* C) Q is false.
* D) No conclusion.

**Q8. A medical expert system is asked "Does this patient have condition X?" It starts from this goal and searches for symptoms and rules that support it. Which method is this?**

* A) Forward Chaining
* B) Modus Tollens
* C) Backward Chaining
* D) Unification

**Q9. A university system stores: Alice → studies at → BIT; BIT → located in → Beijing; Alice → enrolled in → Computer Science. Which representation fits these connected entities and relationships most naturally?**

* A) Knowledge Graph
* B) Propositional Logic
* C) Machine Learning
* D) Resolution

**Q10. A scholarship expert system gives a wrong result because its eligibility rules are outdated. What should be done?**

* A) Remove the inference engine.
* B) Replace all facts with random data.
* C) Stop using logical reasoning.
* D) Update the knowledge base with the current requirements.

**Q11. A campus route planner has paths with different walking times and a heuristic that never overestimates the remaining time. Which method is guaranteed to find the quickest route while using the heuristic to explore fewer places?**

* A) Breadth-First Search
* B) Depth-First Search
* C) A\* Search
* D) Greedy Best-First Search

**Q12. On the 2.5 campus map (S–A 4, S–B 2, A–C 3, A–G 15, B–C 8, B–G 10, C–G 3), which route does breadth-first search return from S to G?**

* A) S → A → C → G (10 minutes)
* B) S → A → G (19 minutes)
* C) S → B → G (12 minutes)
* D) S → A → C → B → G (25 minutes)

### Part C: True or False

**Q13.** Forward chaining begins with a goal and works backward to find supporting facts.

**Q14.** An expert system's explanation facility helps users understand how a conclusion was reached.

**Q15.** Neuro-Symbolic AI combines machine learning with symbolic reasoning.

**Q16.** GOFAI ("Good Old-Fashioned AI") is another name for classical Symbolic AI.

**Q17.** `IF GPA >= 3.5 THEN AcademicallyEligible` is a fact in the knowledge base.

### Part D: Lab Check

**Q18. (Build a Knowledge Web, 2.3)** Byte's knowledge graph holds these triples: Mei → borrowed → Logic for Beginners; Logic for Beginners → shelved on → Library Floor 3; Mei → studies → Artificial Intelligence; Artificial Intelligence → belongs to → Computing Faculty. Why can't Byte answer "Is Mei's book overdue?" by following links?

* A) The graph is too large to search.
* B) No triple stores a due date or today's date, and no rule says when a book is overdue.
* C) Knowledge graphs cannot store information about books.
* D) Mei is not linked to any book.

**Q19. (Professor Pixel's PC Clinic, 2.4)** The knowledge base has three rules:

* R1: IF BeepsAtStart AND BlackScreen THEN POSTFailed
* R2: IF POSTFailed AND ThreeBeeps THEN SuspectRAM
* R4: IF SuspectRAM THEN Advice: reseat the RAM

A PC's working memory is BeepsAtStart, FiveBeeps, BlackScreen. Forward chaining with only these rules adds which new facts?

* A) POSTFailed, SuspectRAM and the RAM advice
* B) POSTFailed only
* C) Nothing at all
* D) SuspectRAM only

**Q20. (The River Crossing, 2.5)** Byte must row a wolf, a goat and a cabbage across a river; the boat holds Byte and at most one passenger. Without Byte, the wolf must never be left with the goat, nor the goat with the cabbage. Why is taking the goat the only safe first crossing?

* A) The goat is the lightest passenger.
* B) Every other first crossing (alone, with the wolf, or with the cabbage) leaves a dangerous pair alone on the start bank.
* C) The wolf and the cabbage are not allowed in the boat.
* D) Any first crossing works; only the last one matters.

**Q21. (The River Crossing and BFS, 2.5)** With each crossing costing 1, breadth-first search finds a 7-crossing river plan. On the campus map, it returned a 19-minute route although a 10-minute route exists. Why the difference?

* A) Every crossing costs the same, so the fewest-step plan is also the cheapest; on the campus map paths cost different amounts, so the fewest steps need not be cheapest.
* B) Breadth-first search uses a heuristic in the river puzzle but not on the map.
* C) Breadth-first search always finds the cheapest route; the campus trace was wrong.
* D) The river puzzle has only one possible plan, so any method finds it.

---

## 4. Answer Key

The section in brackets says where to revise.

<details>
<summary><b>Show answers</b> (try the quiz first!)</summary>

| Question | Answer | Explanation |
| :--- | :--- | :--- |
| **Q1** | **B** | Symbolic AI stores knowledge explicitly as symbols, facts and rules and reasons with logic; learning from trial and error or data is machine learning. *(2.1)* |
| **Q2** | **B** | Predicate logic describes objects, properties and relationships, e.g. `Student(Alice)`; propositional logic only handles whole true/false statements. *(2.3)* |
| **Q3** | **C** | A knowledge graph links entities through named relationships, such as Alice → studies at → BIT. *(2.3)* |
| **Q4** | **D** | Forward chaining works from known facts to new conclusions; backward chaining starts from a goal. *(2.2)* |
| **Q5** | **B** | The inference engine applies the knowledge-base rules to the facts; working memory only holds the current facts, and the user interface handles input and output. *(2.4)* |
| **Q6** | **C** | Someone must write and update all the knowledge, which is slow and costly. A and B are wrong because facts and rules are exactly what Symbolic AI uses; D because explainability is its main strength. *(2.1, 2.2, 2.4)* |
| **Q7** | **B** | Modus Ponens: if P → Q and P is true, then Q is true. *(2.2)* |
| **Q8** | **C** | It starts from the goal (condition X) and looks for supporting facts, which is backward chaining; forward chaining would start from the symptoms. *(2.2)* |
| **Q9** | **A** | Alice, BIT and Beijing are entities (nodes) joined by named relationships (links): a knowledge graph. *(2.3)* |
| **Q10** | **D** | Conclusions are only as good as the stored rules, so the fix is to update the knowledge base; the inference engine and reasoning are not at fault. *(2.4)* |
| **Q11** | **C** | A\* explores the smallest f = g + h, and with an admissible heuristic it is guaranteed the cheapest route. BFS ignores costs, DFS may return a long route, and greedy search can be misled by the heuristic. *(2.5)* |
| **Q12** | **B** | BFS ignores costs and (alphabetical tie rule) expands A before B; expanding A already reaches G, so it returns S → A → G: 2 steps but 19 minutes. The 10-minute route (A) needs uniform-cost search or A\*. *(2.5)* |
| **Q13** | **False** | That is backward chaining; forward chaining starts from known facts. *(2.2)* |
| **Q14** | **True** | It shows the facts and rules behind a conclusion, which makes expert systems transparent. *(2.4)* |
| **Q15** | **True** | For example, a learned model spots signs of disease in an image and rules then apply clinical knowledge to it. *(2.4)* |
| **Q16** | **True** | GOFAI is Haugeland's name for classical Symbolic AI, built on symbols, explicit knowledge and logic. *(2.1)* |
| **Q17** | **False** | It has an IF–THEN form, so it is a **rule**; a fact simply states something true, such as `GPA(Alex, 3.9)`. *(2.1)* |
| **Q18** | **B** | Following links only retrieves stored facts. Byte needs new facts (due date, today's date) and a rule ("IF the due date is before today THEN overdue"); D is wrong because Mei → borrowed → Logic for Beginners is there. *(2.3, Lab: Build a Knowledge Web)* |
| **Q19** | **B** | R1 matches and adds POSTFailed, but R2 needs ThreeBeeps (this PC has FiveBeeps), so R2 and then R4 cannot fire. Byte knows the start-up check failed but not why; the full clinic needs R3, the five-beep rule. *(2.4, Lab: Dr. Pixel's PC Clinic)* |
| **Q20** | **B** | Going alone leaves all three together, taking the wolf leaves goat with cabbage, and taking the cabbage leaves wolf with goat. The goat is in both dangerous pairs, so it must go first. *(2.5, Lab: The River Crossing)* |
| **Q21** | **A** | BFS finds the fewest steps, which is the cheapest plan only when every step costs the same. On the map, S → A → G has 2 steps but 19 minutes, while S → A → C → G has 3 steps and 10 minutes; D is wrong because the puzzle has two 7-crossing plans. *(2.5 §4.1 and §8; Lab: The River Crossing)* |

</details>

---

## A Note from Team Mickey Mouse

Congratulations on making it through the foundations of Software and Symbolic AI! Learning AI is not just about understanding how intelligent systems work. It is about learning how to build, question and improve them.

**Stay curious. Keep building. And don't be afraid to make mistakes.**

---

## 5. References

1. Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
2. Brachman, R. J., & Levesque, H. J. (2004). *Knowledge Representation and Reasoning*. Morgan Kaufmann.
3. Giarratano, J. C., & Riley, G. D. (2005). *Expert Systems: Principles and Programming* (4th ed.). Thomson.
4. Jackson, P. (1998). *Introduction to Expert Systems* (3rd ed.). Addison-Wesley.
5. Hart, P. E., Nilsson, N. J., & Raphael, B. (1968). A formal basis for the heuristic determination of minimum cost paths. *IEEE Transactions on Systems Science and Cybernetics*, 4(2), 100–107.
6. BIT2026 Foundations of CS & AI, course lecture slides, Chapter 4: Symbolic AI (2026).
