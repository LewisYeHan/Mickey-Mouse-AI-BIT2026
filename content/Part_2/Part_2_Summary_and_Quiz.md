# 2.8 Module Summary & Self-Check Quiz

**Status:** 📝  
**Team Member:** Goh Ye Han (`@LewisYeHan`)

**In this section:** How It All Connects · Key Ideas from Each Section · Quiz (15 questions) · Answer Key · References

---

## 1. How It All Connects

Sections 2.1 to 2.7 explain how Symbolic AI represents knowledge, reasons with it, and uses it to solve problems. Each section builds on the previous one: first, we understand what Symbolic AI is; then we explore how it stores knowledge, how it reasons, how expert systems apply these ideas, and where this approach succeeds and struggles. The last two sections show how the same ideas are used to plan sequences of actions and to understand human language.

The easiest way to understand the whole module is to imagine building an AI system that helps decide whether a student qualifies for a scholarship.

**Understanding the approach (2.1 What Is Symbolic AI?).** Symbolic AI represents knowledge using symbols, facts, rules, and logic. Instead of learning everything from examples, the system receives explicitly represented knowledge that it can use to make decisions.

**Storing knowledge (2.2 Knowledge Representation).** Before the system can reason, it needs to organize what it knows. For example, it might store the facts that a student has a GPA of 3.8 and has completed all required courses. It can represent these facts using predicate logic, semantic networks, frames, ontologies, or knowledge graphs.

**Reasoning with knowledge (2.3 How Symbolic AI Reasons).** The system applies logical rules to its stored facts. For example:

- Fact: The student's GPA is 3.8.
- Rule: If a student's GPA is at least 3.5, they meet the academic requirement.
- Conclusion: The student meets the academic requirement.

This is an example of **Modus Ponens**: if P implies Q, and P is true, then Q follows. The system can also use forward chaining to derive conclusions from facts or backward chaining to investigate a particular goal.

**Applying the knowledge (2.4 Expert Systems).** An expert system combines a knowledge base with an inference engine to solve problems in a specific domain. In our scholarship example, the knowledge base stores eligibility requirements, while the inference engine applies those requirements to the student's information. An explanation facility can show why the system reached its decision.

**Evaluating the approach (2.5 Strengths and Limitations).** Symbolic AI can explain its decisions because its reasoning follows explicit rules. However, it depends on the quality of its knowledge base. If scholarship requirements change and the rules are not updated, the system may produce incorrect decisions.

**Planning the steps (2.6 Planning and Problem Solving).** Some problems need a sequence of actions, not just one conclusion. If the student must submit a transcript, get a reference and attend an interview, a planner can describe each step with preconditions and effects and search for an order that reaches the goal "application complete". Search methods such as breadth-first search, uniform-cost search and A\* find routes through the possible states, and minimax handles games against an opponent.

**Understanding the question (2.7 NLP in Symbolic AI).** A student might simply type "Am I eligible for the scholarship?". Symbolic NLP tags each word, parses the sentence with grammar rules, turns its meaning into a logical query such as `ScholarshipEligible(Student)`, and answers it with the inference methods from 2.3.

**The main idea:** Symbolic AI follows a cycle: represent knowledge, store facts and rules, reason with them, and use the conclusions to solve problems, whether that means answering a question, planning a sequence of actions or understanding a sentence. Its strength is structured and explainable reasoning, but its limitation is that knowledge must be represented and maintained.

---

## 2. Key Ideas from Each Section

| Section | Main question | Key ideas |
| :--- | :--- | :--- |
| **2.1 Symbolic AI** | What is Symbolic AI? | Symbols, facts, rules, logic, explicit knowledge representation |
| **2.2 Knowledge Representation** | How does AI store knowledge? | Propositional logic, predicate logic, semantic networks, frames, ontologies, knowledge graphs |
| **2.3 Logical Reasoning** | How does AI reach conclusions? | Modus Ponens, Modus Tollens, forward chaining, backward chaining, unification, resolution, uncertainty |
| **2.4 Expert Systems** | How is symbolic reasoning applied? | Knowledge base, inference engine, working memory, user interface, explanation facility, knowledge acquisition |
| **2.5 Strengths and Limitations** | Where does Symbolic AI succeed or struggle? | Explainability, consistency, knowledge acquisition bottleneck, ambiguity, limited learning, Neuro-Symbolic AI |
| **2.6 Planning and Problem Solving** | How does AI find a sequence of actions? | States, actions, preconditions and effects, BFS, DFS, uniform-cost search, heuristics, A\*, minimax, hill climbing |
| **2.7 NLP in Symbolic AI** | How does AI understand human language? | Syntax and formal grammars, parse trees, semantics in logic, rule-based NLP (part-of-speech tagging, parsing, information extraction), logic and inference, sentiment analysis, question answering, information retrieval |

### Words That Connect the Seven Sections

| Term | Meaning | Role in Symbolic AI |
| :--- | :--- | :--- |
| **Symbol** | A representation of an object or concept | Allows knowledge to be represented explicitly |
| **Fact** | A statement accepted as true by the system | Provides information for reasoning |
| **Rule** | A condition that connects facts to conclusions | Determines when new conclusions can be derived |
| **Knowledge Base** | A collection of stored facts and rules | Stores the system's domain knowledge |
| **Inference Engine** | The mechanism that applies logical rules | Uses knowledge to derive conclusions |
| **Expert System** | An AI program designed for a specific domain | Applies symbolic reasoning to solve problems |
| **State** | A description of the world at one moment | Lets planners and search methods track progress toward a goal |
| **Formal Grammar** | A set of rules describing sentence structure | Lets NLP systems turn sentences into structured, logical meaning |

### Important Reasoning Methods

| Method | How it works |
| :--- | :--- |
| **Modus Ponens** | If P implies Q, and P is true, conclude Q. |
| **Modus Tollens** | If P implies Q, and Q is false, conclude P is false. |
| **Forward Chaining** | Starts with known facts and works toward conclusions. |
| **Backward Chaining** | Starts with a goal and works backward to find supporting facts. |
| **Unification** | Finds substitutions that make logical expressions match. |
| **Resolution** | Uses logical clauses to derive conclusions or establish contradictions. |
| **A\* Search** | Explores the state with the smallest cost so far plus estimated cost to the goal (f = g + h). |
| **Minimax** | Chooses the move with the best guaranteed result, assuming the opponent also plays its best. |

### Symbolic AI vs. Machine Learning

| Symbolic AI | Machine Learning |
| :--- | :--- |
| Uses explicitly represented facts and rules | Learns patterns from data |
| Reasons through logical rules | Makes predictions based on learned patterns |
| Often easier to explain | Can be difficult to interpret |
| Depends on manually represented knowledge | Depends heavily on training data |
| Effective for structured reasoning | Effective for pattern recognition |

**Neuro-Symbolic AI** combines neural networks with symbolic reasoning to benefit from both approaches.

---

## 3. Self-Check Quiz

Try all 15 questions first, then check your answers in Section 4. Part A checks your understanding of the key concepts. Parts B and C ask you to apply and evaluate them.

### Part A: Multiple Choice

**Q1. What is the main characteristic of Symbolic AI?**

* A) It learns all knowledge through trial and error.
* B) It represents knowledge using symbols, facts, rules, and logic.
* C) It relies entirely on neural networks.
* D) It produces conclusions without storing knowledge.

**Q2. Which knowledge representation method describes objects, their properties, and relationships using logical predicates?**

* A) Propositional Logic
* B) Predicate Logic
* C) Semantic Networks
* D) Frames

**Q3. What is the main purpose of a knowledge graph?**

* A) To train neural networks using numerical weights.
* B) To store computer programs as executable instructions.
* C) To represent entities and their relationships as connected information.
* D) To execute rules without storing facts.

**Q4. Which reasoning method starts with known facts and repeatedly applies rules to derive new conclusions?**

* A) Backward Chaining
* B) Unification
* C) Resolution
* D) Forward Chaining

**Q5. In an expert system, which component applies rules to available facts to derive conclusions?**

* A) User Interface
* B) Inference Engine
* C) Knowledge Acquisition
* D) Working Memory

**Q6. Which of the following is a major limitation of traditional Symbolic AI?**

* A) It cannot represent facts.
* B) It cannot use logical rules.
* C) It requires knowledge to be explicitly represented and maintained.
* D) It cannot explain any of its conclusions.

### Part B: Apply It

**Q7. Consider the following statements:**

* Fact: P is true.
* Rule: If P is true, then Q is true.

What conclusion can be logically derived using Modus Ponens?

* A) P is false.
* B) Q is true.
* C) Q is false.
* D) No conclusion can be derived.

**Q8. A medical expert system is asked: "Does this patient have condition X?" It starts with this goal and searches for symptoms and rules that could support it. Which reasoning method is being used?**

* A) Forward Chaining
* B) Modus Tollens
* C) Backward Chaining
* D) Unification

**Q9. A university AI system stores the following relationships:**

* Alice → studies at → BIT
* BIT → located in → Beijing
* Alice → enrolled in → Computer Science

Which knowledge representation method most naturally represents these connected entities and relationships?

* A) Knowledge Graph
* B) Propositional Logic
* C) Machine Learning
* D) Resolution

**Q10. A scholarship expert system gives a student an incorrect result because its eligibility rules are outdated. What is the most appropriate action?**

* A) Remove the inference engine.
* B) Replace all facts with random data.
* C) Stop using logical reasoning.
* D) Update the knowledge base with the current eligibility requirements.

**Q11. A route planner searches a campus map. Paths have different walking times, and it has a heuristic that never overestimates the remaining time. Which method is guaranteed to find the quickest route while using the heuristic to explore fewer places?**

* A) Breadth-First Search
* B) Depth-First Search
* C) A\* Search
* D) Greedy Best-First Search

**Q12. A course-feedback system uses this sentiment lexicon: clear = +1, boring = −1, and the rule "*not* flips the score of the next sentiment word". What is the total score of: "The lecture was not boring and the notes were clear"?**

* A) −2
* B) 0
* C) +1
* D) +2

### Part C: True or False

**Q13.** Forward chaining begins with a goal and works backward to find supporting facts.

**Q14.** An explanation facility in an expert system helps users understand how a conclusion was reached.

**Q15.** Neuro-Symbolic AI combines neural networks with symbolic reasoning.

---

## 4. Answer Key

<details>
<summary><b>Show answers</b> (try the quiz first!)</summary>

| Question | Answer | Explanation |
| :--- | :--- | :--- |
| **Q1** | **B** | Symbolic AI represents knowledge explicitly through symbols, facts, rules, and logic. It uses these representations to reason and derive conclusions. *(2.1)* |
| **Q2** | **B** | Predicate Logic represents objects, their properties, and relationships. For example, `Student(Alice)` represents that Alice is a student. *(2.2)* |
| **Q3** | **C** | A knowledge graph connects entities through meaningful relationships. It can represent information such as Alice studying at BIT and BIT being located in Beijing. *(2.2)* |
| **Q4** | **D** | Forward chaining begins with known facts and applies matching rules to derive new facts and conclusions. Backward chaining instead starts with a goal. *(2.3)* |
| **Q5** | **B** | The inference engine applies the rules stored in the knowledge base to available facts. The user interface handles interaction, while working memory stores information relevant to the current problem. *(2.4)* |
| **Q6** | **C** | Traditional Symbolic AI depends on explicitly represented knowledge. Building and updating a large knowledge base can be difficult and expensive. *(2.5)* |
| **Q7** | **B** | Modus Ponens states that if P implies Q and P is true, then Q must also be true. Since both conditions are satisfied, Q follows. *(2.3)* |
| **Q8** | **C** | Backward chaining starts with a goal and searches for rules and facts that can prove it. The system begins with the question about condition X rather than starting with known symptoms. *(2.3)* |
| **Q9** | **A** | A knowledge graph represents entities such as Alice and BIT as nodes and their relationships as connections. This is a natural way to organize the information in the question. *(2.2)* |
| **Q10** | **D** | The system's conclusion depends on the accuracy of its stored knowledge. Updating the knowledge base ensures that the inference engine uses current eligibility requirements. *(2.4, 2.5)* |
| **Q11** | **C** | A\* explores the state with the smallest f = g + h. When the heuristic never overestimates (it is admissible), A\* is guaranteed to find the cheapest route. BFS ignores path costs, DFS can return long routes, and greedy search can be fooled by the heuristic. *(2.6)* |
| **Q12** | **D** | *not boring* flips −1 to +1, and *clear* is +1, so the total is +1 + 1 = +2. The feedback is positive. *(2.7)* |
| **Q13** | **False** | This describes backward chaining. Forward chaining starts with known facts and applies rules to reach conclusions. *(2.3)* |
| **Q14** | **True** | An explanation facility shows users the reasoning or rules behind a system's conclusion. This is one reason expert systems can provide transparent decisions. *(2.4)* |
| **Q15** | **True** | Neuro-Symbolic AI combines neural networks, which learn patterns from data, with symbolic methods, which represent knowledge and reason using logic. *(2.5)* |

</details>

---

## 5. References

1. Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
2. Brachman, R. J., & Levesque, H. J. (2004). *Knowledge Representation and Reasoning*. Morgan Kaufmann.
3. Giarratano, J. C., & Riley, G. D. (2005). *Expert Systems: Principles and Programming* (4th ed.). Thomson.
4. Jackson, P. (1998). *Introduction to Expert Systems* (3rd ed.). Addison-Wesley.
5. Hart, P. E., Nilsson, N. J., & Raphael, B. (1968). A formal basis for the heuristic determination of minimum cost paths. *IEEE Transactions on Systems Science and Cybernetics*, 4(2), 100–107.
6. Jurafsky, D., & Martin, J. H. *Speech and Language Processing* (3rd ed. draft). [Online textbook](https://web.stanford.edu/~jurafsky/slp3/)
7. BIT2026 Course Lecture Slides (Part 2 — Symbolic AI).
