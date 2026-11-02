
# 2.1 What Is Symbolic AI?

**Status:** ✅  
**Team Member:** Frederick Samuel Lesmana (@Ti4nCi)

**In this section:** What is Symbolic AI · Symbols, Facts & Rules · How Symbolic AI Works · GOFAI · Real-World Applications · Summary · Practice Questions

---

## 1. What Is Symbolic AI?

Imagine you are applying for a university scholarship. The university has two requirements:

- Your GPA must be at least 3.5.
- Your attendance must be at least 90%.

Someone gives a computer these requirements and asks it to determine whether you qualify. The computer checks your information against the requirements and produces an answer.

This is a simple example of **Symbolic AI**.

**Symbolic AI** is an approach to Artificial Intelligence that represents knowledge using symbols, facts, and logical rules. It uses these representations to reason about information and reach conclusions.

Instead of learning everything from large amounts of data, Symbolic AI works with knowledge that has been explicitly represented and provided to the system.

There are three important ideas behind Symbolic AI:

1. **Symbols:** Represent objects, concepts, or relationships.
2. **Facts:** Store information that the system treats as true.
3. **Rules:** Tell the system how to use information to reach conclusions.

The main idea is simple: give the computer knowledge, provide rules, and let it reason.

---

## 2. Symbols, Facts, and Rules

To understand Symbolic AI, you first need to understand how it represents knowledge. Think of it like teaching a new student about the world: you give them information, explain relationships, and establish rules.

### Symbols

A **symbol** is a representation of something, such as a person, object, concept, or relationship.

For example:

| Symbol | Represents |
| :--- | :--- |
| `Sammy` | A particular person |
| `Student` | The concept of a student |
| `GPA` | Grade Point Average |
| `Scholarship` | A scholarship opportunity |

Symbols allow computers to represent real-world concepts in a structured way.

### Facts

A **fact** is a statement that the system treats as true within its knowledge base.

For example:

```text
Student(Sammy)
GPA(Sammy, 3.8)
Attendance(Sammy, 95%)
```

These facts tell the system that Sammy is a student, has a GPA of 3.8, and has an attendance rate of 95%.

### Rules

A **rule** describes what should happen when certain conditions are satisfied.

Rules are commonly written using the **IF–THEN** format:

```text
IF GPA >= 3.5
AND Attendance >= 90%
THEN Scholarship_Eligible = TRUE
```

The system checks whether the conditions are satisfied before reaching a conclusion.

**Remember the difference:**

- Symbols represent things.
- Facts describe what the system knows.
- Rules tell the system how to reason.

---

## 3. How Does Symbolic AI Work?

Now let's put everything together using our scholarship example.

Suppose the system has the following information:

**Facts:**

```text
Student = Sammy
GPA = 3.8
Attendance = 95%
```

**Rule:**

```text
IF GPA >= 3.5
AND Attendance >= 90%
THEN Scholarship_Eligible = TRUE
```

The system follows these steps:

1. It receives Sammy's information.
2. It checks whether his GPA meets the minimum requirement.
3. It checks whether his attendance meets the minimum requirement.
4. Both conditions are satisfied.
5. It applies the rule and concludes that Sammy meets the scholarship requirements.

![Symbolic AI reasoning process](images/symbolic_ai_process.png)
*Figure 2.1: How Symbolic AI uses facts and rules to derive a conclusion.*

This process is called **logical inference**. It means deriving new conclusions from information that the system already knows.

The computer does not need to guess whether Sammy qualifies. It follows the rules that were provided to it.

**Important:** This example only checks two scholarship requirements. A real scholarship decision may involve additional conditions.

---

## 4. Good Old-Fashioned AI (GOFAI)

You may come across the term **Good Old-Fashioned AI (GOFAI)** when studying the history of Artificial Intelligence.

GOFAI is an informal term used to describe traditional approaches to AI that relied heavily on symbols, explicit knowledge, and logical reasoning.

Early AI researchers believed that computers could demonstrate intelligent behaviour by representing knowledge and manipulating symbols according to formal rules.

### What Did GOFAI Focus On?

![Timeline of Symbolic AI](../images/symbolic_ai_timeline.png)

*Figure 2.3: Key milestones in the development of Symbolic AI.*

GOFAI commonly involved:

- Representing knowledge using symbols.
- Storing information as facts and relationships.
- Defining rules for solving problems.
- Applying logical reasoning to derive conclusions.
- Using structured search and planning to solve problems.

![Early artificial intelligence research](../images/gofai_history.png)
*Figure 2.2: Early AI research focused heavily on symbolic representations and logical problem-solving.*

### Symbolic AI vs. GOFAI

These terms are closely related, but they are not exactly interchangeable.

| Term | Meaning |
| :--- | :--- |
| **Symbolic AI** | An AI approach that represents and processes knowledge using symbols and formal rules. |
| **GOFAI** | An informal term for traditional AI approaches that relied heavily on symbolic methods. |

In simple terms, GOFAI is strongly associated with the early development of Symbolic AI.

---

## 5. Real-World Applications of Symbolic AI

Symbolic AI is useful when knowledge can be clearly represented and decisions can be made using defined rules.

Some common applications include:

| Application | How It Is Used |
| :--- | :--- |
| **Expert Systems** | Uses stored expert knowledge and rules to provide recommendations. |
| **Medical Decision Support** | Applies medical rules to patient information to assist with diagnosis. |
| **Rule-Based Chatbots** | Uses predefined rules to respond to specific questions. |
| **Automated Planning** | Uses goals, actions, and conditions to determine a sequence of steps. |
| **Configuration Systems** | Applies rules to determine compatible components and configurations. |

For example, a medical expert system may examine a patient's symptoms and compare them against medical rules to suggest possible diagnoses.

However, it does not automatically understand medicine like a human doctor. Its conclusions depend on the knowledge and rules available to it.

---

## 6. Why Is Symbolic AI Important?

Symbolic AI played an important role in the development of Artificial Intelligence because it demonstrated that computers could solve certain problems through explicit knowledge and logical reasoning.

One of its biggest advantages is **explainability**.

Because a symbolic system uses identifiable facts and rules, it can often show how it reached a particular conclusion.

For example:

```text
Fact: GPA = 3.8
Rule: IF GPA >= 3.5 THEN Academically_Eligible
Conclusion: Academically_Eligible = TRUE
```

A person can follow the same reasoning and understand why the system produced its answer.

However, Symbolic AI also has limitations. It can struggle when information is incomplete, ambiguous, or difficult to represent using predefined rules.

These strengths and limitations will be explored further in [2.5 Strengths and Limitations](08_Strengths_and_Limits.md).

---

## 7. Summary

| Concept | Meaning |
| :--- | :--- |
| **Symbolic AI** | An AI approach that represents knowledge using symbols, facts, and rules. |
| **Symbol** | A representation of an object, concept, or relationship. |
| **Fact** | A statement that the system treats as true. |
| **Rule** | A condition that determines what conclusion or action should follow. |
| **Logical Inference** | Deriving conclusions from existing facts and rules. |
| **GOFAI** | Traditional AI approaches that relied heavily on symbolic methods. |
| **Explainability** | The ability to understand how a system reaches a conclusion. |

### Key Points to Remember

1. **Symbolic AI** represents knowledge using symbols, facts, and rules.
2. **Symbols** represent objects and concepts, while facts describe information.
3. **Rules** tell the system how to use information to reach conclusions.
4. **Logical inference** allows the system to derive new conclusions.
5. **GOFAI** refers to traditional AI approaches heavily associated with symbolic reasoning.
6. Symbolic AI is useful when knowledge and decision-making rules can be clearly defined.

---

## 8. Practice Questions and Answers

Try answering each question yourself first, then read the answer.

**Questions**

1. What is Symbolic AI, and what are its three main components?
2. What is the difference between a fact and a rule?
3. A system contains the rule `IF temperature > 38°C THEN fever = TRUE`. If the recorded temperature is 39°C, what conclusion should the system reach?
4. What does GOFAI stand for, and what was its main approach to Artificial Intelligence?
5. Why can Symbolic AI explain how it reaches certain conclusions?
6. A scholarship system requires a GPA of at least 3.5 and attendance of at least 90%. A student has a GPA of 3.2 and attendance of 98%. Does the student satisfy both requirements? Explain your answer.

**Answers**

1. Symbolic AI is an approach to AI that represents knowledge using symbols, facts, and rules. Its three main components are symbols (representations), facts (stored information), and rules (conditions used for reasoning).
2. A fact is information that the system treats as true, while a rule describes what conclusion follows when certain conditions are satisfied.
3. The system concludes `fever = TRUE` because 39°C is greater than 38°C, satisfying the rule.
4. GOFAI stands for Good Old-Fashioned AI. It describes traditional approaches to AI that relied heavily on symbols, explicit knowledge, and logical reasoning.
5. Symbolic AI uses identifiable facts and rules. These can often be traced to show how the system reached its conclusion.
6. No. Although the student's attendance meets the requirement, the GPA of 3.2 is below the required 3.5. Both conditions must be satisfied.

---

## 9. References

1. Russell, S. J., & Norvig, P. (2021). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson.
2. Haugeland, J. (1985). *Artificial Intelligence: The Very Idea*. MIT Press.
3. Newell, A., & Simon, H. A. (1976). Computer Science as Empirical Inquiry: Symbols and Search. *Communications of the ACM, 19*(3), 113–126.
4. BIT2026 Course Lecture Slides (Symbolic AI Module).
