# 2.6 Glossary

**Team Member:** Goh Ye Han (`@LewisYeHan`)

**In this section:** [Foundations](#1-foundations-of-symbolic-ai-taught-in-21) · [Knowledge Representation](#2-knowledge-representation-taught-in-23) · [Logical Reasoning](#3-logical-reasoning-taught-in-22-the-inference-engine-also-in-24) · [Uncertainty](#4-uncertainty-and-reasoning-methods-taught-in-22-section-9) · [Expert Systems](#5-expert-systems-taught-in-24) · [AI Approaches](#6-ai-approaches-and-evaluation-taught-in-21-section-5-22-section-11-and-24-sections-68) · [Planning and Search](#7-planning-and-search-taught-in-25)

Key terms from Sections 2.1 to 2.5, A–Z within each category. Each heading names the section that teaches its terms, so you can go back to the full explanation.

---

## 1. Foundations of Symbolic AI (taught in 2.1)

| Term | Definition |
|---|---|
| Artificial Intelligence (AI) | Building machines that do tasks which normally need human intelligence. |
| ELIZA | A rule-based chatbot by Joseph Weizenbaum at MIT, described in 1966. It looks for keywords in a sentence and answers with a reply pattern for that keyword; it does not understand meaning. |
| Explicit Knowledge | Knowledge written out clearly, in a form a computer can store and process. |
| Fact | A statement the system treats as true, such as "Alex is a student". |
| GOFAI | "Good Old-Fashioned AI": another name for classical Symbolic AI, built on symbols, explicit rules and logic. |
| Inference | Deriving new conclusions from existing facts and rules. |
| Knowledge | Organized information that can be used to understand situations and make decisions. |
| Logic | A formal system for writing statements and checking whether conclusions follow from them. |
| Physical Symbol System Hypothesis | Newell and Simon's claim that storing symbols and changing them by rules is both necessary and sufficient for general intelligent action; the idea behind GOFAI. |
| Symbol | A name or sign that stands for an object, concept or relationship. |
| Symbolic AI | AI that represents knowledge with symbols, facts and rules, and reasons with logic. |

## 2. Knowledge Representation (taught in 2.3)

| Term | Definition |
|---|---|
| Biconditional | The connective ↔ ("if and only if"): both statements are true or both are false. |
| Constant | In predicate logic, a symbol naming one specific object, such as `Alex`. |
| Data | Raw values without context, such as `19` or `Alex`. |
| De Morgan's Laws | ¬(P ∧ Q) ≡ ¬P ∨ ¬Q and ¬(P ∨ Q) ≡ ¬P ∧ ¬Q. |
| Default Value | The value a frame slot takes when nothing more specific is given, such as Major = Undeclared. |
| Entity | An object, person, place or concept that a knowledge system describes. |
| Existential Quantifier | ∃: "there is at least one" object for which the statement is true. |
| Frame | A form-like structure describing an object or concept by its slots and their values. |
| Information | Data in a meaningful context, such as "Alex is 19". |
| Inheritance | A specific concept receiving properties from a general one along IS-A links (a Student gets Name from Person). |
| Instance | One specific member of a general concept, such as Alex of Student; in frames, a filled-in copy of the template. |
| Knowledge Graph | Entities and their relationships stored as a network of linked facts (triples). |
| Knowledge Representation (KR) | How knowledge is organized and stored so that an AI system can use it. |
| Logical Equivalence | ≡: two statements that have the same truth value in every situation. |
| Logical Operator | A connective that joins or changes statements: AND (∧), OR (∨), NOT (¬), → and ↔. |
| Ontology | A formal, shared vocabulary of a domain's concepts, categories and relationships. |
| Predicate | A property of an object or a relation between objects, such as `Studies(Alex, AI)`. |
| Predicate Logic | Logic that uses predicates, variables and quantifiers to describe objects and their relationships. |
| Production Rule | See Rule (Section 3). |
| Proposition | A statement that is either true or false. |
| Propositional Logic | Logic that combines whole true/false statements with logical operators. |
| Quantifier | A symbol saying how many objects a statement covers: ∀ (all) or ∃ (at least one). |
| Relationship | A link between entities, such as "studies" or "is a". |
| Rule-Based Representation | Storing knowledge as a set of IF–THEN rules. |
| Script | A sequence of frames describing a typical series of events, such as borrowing a library book. |
| Semantic Network | A graph whose nodes are concepts and whose labelled edges are relationships. |
| Slot | One attribute of a frame, such as Name or Major. |
| Triple | One knowledge-graph fact: subject → relationship → object, such as Alex → studies → Computer Science. |
| Truth Table | A table listing the value of an expression for every combination of true and false inputs; it can prove that two statements are logically equivalent. |
| Universal Quantifier | ∀: the statement is true for every object in the domain. |
| Variable | In predicate logic, a symbol standing for any object, such as `x`. |

## 3. Logical Reasoning (taught in 2.2; the inference engine also in 2.4)

| Term | Definition |
|---|---|
| Backward Chaining | Reasoning from a goal back to the facts and rules that would prove it. |
| Clause | A statement made of one or more terms joined by OR, such as `P ∨ Q` or `¬P`; resolution works on clauses. |
| Conclusion | A new statement derived from facts and rules. |
| Conflict Resolution | Choosing which rule to fire when several rules match at once. |
| Conflict Set | All the rules whose conditions match the current facts, before one is chosen to fire. |
| Fire | When a matching rule actually runs and adds its conclusion to the facts. If several rules match at once, conflict resolution chooses which one fires. |
| Forward Chaining | Reasoning from known facts, applying rules repeatedly until no rule adds a new fact. |
| Inference Engine | The part of an expert system that applies rules to facts to derive conclusions. |
| Match | A rule matches when all its conditions are true for the current facts. Matching rules are triggered and form the conflict set. |
| Modus Ponens | If P → Q and P is true, then Q is true. |
| Modus Tollens | If P → Q and Q is false, then P is false. |
| Resolution | A proof method that combines clauses to derive conclusions or expose a contradiction. |
| Rule | An IF–THEN statement: when the conditions hold, the conclusion follows. Also called a production rule. |
| Rule-Based System | A system that reaches decisions by applying IF–THEN rules; an expert system is one kind. |
| Specificity | A conflict resolution strategy: prefer the rule whose conditions include all of another rule's conditions plus more. |
| Substitution | Replacing variables with specific values, such as x = Alex. |
| Unification | Finding the substitution that makes two logical expressions identical. |
| Unifier | The substitution that unification finds, such as x = Alex, which makes `Student(x)` and `Student(Alex)` identical. |

## 4. Uncertainty and Reasoning Methods (taught in 2.2, Section 9)

| Term | Definition |
|---|---|
| Certainty Factor | A number from −1 (definitely false) to +1 (definitely true) for confidence in a conclusion, as in MYCIN; not a probability. |
| Fuzzy Logic | Logic in which truth can lie anywhere between false (0) and true (1). |
| Membership Degree | In fuzzy logic, how much something belongs to a vague category, from 0 to 1 (30°C is "hot" to degree 0.8). |
| Probabilistic Reasoning | Handling uncertainty by working with probabilities. |
| Probability | A number from 0 to 1 for how likely something is to be true. |
| Uncertainty | Information too incomplete or unclear to give a definite conclusion. |

## 5. Expert Systems (taught in 2.4)

| Term | Definition |
|---|---|
| DENDRAL | Early expert system (Stanford, from 1965) that found molecular structures from chemical data. |
| Domain | The specific area of expertise a system is built for, such as medicine. |
| Expert System | AI that applies expert knowledge, stored as rules, to solve problems in one domain. |
| Explanation Facility | The part of an expert system that shows how and why it reached a conclusion. |
| Knowledge Acquisition | Collecting experts' knowledge and turning it into rules; slow and difficult, so a major limitation. |
| Knowledge Base | An expert system's stored facts and rules. |
| MYCIN | Early medical expert system (Stanford, 1970s) for bacterial infections and antibiotics. |
| User Interface | The part through which users enter facts and see results. |
| Working Memory | The facts about the current case, which grow as rules fire. |
| XCON | Expert system (also R1) that configured DEC VAX computers from customer orders. |

## 6. AI Approaches and Evaluation (taught in 2.1 Section 5, 2.2 Section 11 and 2.4 Sections 6–8)

| Term | Definition |
|---|---|
| Ambiguity | Information with more than one possible meaning, which is hard to represent as symbols. |
| Brittleness | Failing on situations the rules do not cover; a limitation of Symbolic AI. |
| Explainability | Being able to give understandable reasons for a decision. |
| Knowledge Bottleneck | Experts must write every rule by hand, which is slow and expensive; a limitation of Symbolic AI. |
| Knowledge Maintenance | Updating stored rules and facts; out-of-date rules give wrong answers, however good the engine. |
| Machine Learning (ML) | AI that learns patterns from data instead of following hand-written rules. |
| Neuro-Symbolic AI | Combining machine learning (patterns from data) with symbolic reasoning (rules and logic). |
| Pattern Recognition | Spotting regularities in data, such as signs of disease in images; a strength of machine learning. |

## 7. Planning and Search (taught in 2.5)

| Term | Definition |
|---|---|
| A\* Search | Informed search that explores the state with the smallest f = g + h (cost so far + estimated cost to goal). |
| Action | Something an agent can do to change the state, described by preconditions and effects. |
| Admissible Heuristic | A heuristic that never overestimates the true remaining cost; with it, A\* finds the cheapest solution (if allowed to re-explore a state reached more cheaply). |
| Adversarial Search | Search against an opponent who chooses moves, as in games. |
| Alpha-Beta Pruning | Skipping branches that cannot change minimax's decision; same result, less work. |
| Breadth-First Search (BFS) | Uninformed search that explores all states 1 step away, then 2 steps, and so on. |
| Constraint | A rule every allowed state must obey, such as "the goat is never left alone with the cabbage". |
| Deep Blue | IBM's chess computer that beat world champion Garry Kasparov in 1997, using minimax with alpha-beta pruning and a score for each position. |
| Depth-First Search (DFS) | Uninformed search that follows one path as deep as possible before backing up. |
| Effect | What becomes true or false after an action. |
| Frontier | The states discovered but not yet explored. |
| Goal State | The state, or set of conditions, the search is trying to reach. |
| Goal Test | The check for whether the current state is a goal, such as "Are we at the Teaching Building?" |
| Greedy Best-First Search | Informed search that always explores the state the heuristic says is closest to the goal. |
| Heuristic | An estimate of how far a state is from the goal. |
| Hill Climbing | Local search that keeps moving to a better neighbour until none is better. |
| Informed Search | Search that uses a heuristic to try promising states first. |
| Initial State | The state where the problem starts. |
| Local Maximum | A solution better than all its neighbours but not the best overall. |
| Local Search | Improving one solution step by step instead of building a path from the start. |
| Minimax | Game search in which one player maximises and the other minimises the score, both playing their best. |
| Path Cost | The total cost of a sequence of actions, such as total time. |
| Plan | A sequence of actions that turns the initial state into a goal state. |
| Planning | Finding a plan that reaches a goal. |
| Precondition | What must be true before an action can be done. |
| Simulated Annealing | Local search that sometimes accepts a worse solution, less often over time, to escape local maxima. |
| State | A description of the world at one moment. |
| State Space | All possible states and the actions that connect them. |
| STRIPS | A way of describing actions by preconditions, an add list and a delete list; built for the Shakey robot (1971). |
| Transition Model | What each action leads to: the state you reach when you take an action in a given state. |
| Uniform-Cost Search (UCS) | Uninformed search that always explores the state with the lowest total cost so far. |
| Uninformed Search | Search with no extra knowledge of where the goal is (blind search). |
