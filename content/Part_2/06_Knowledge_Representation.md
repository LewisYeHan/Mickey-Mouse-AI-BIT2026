2.3 Knowledge Representation
Status: ✅
Team Member: Cao Minh Tuan (@mnhtnc)

In this section: What is Knowledge Representation? · Data, Information and Knowledge · Propositional Logic and Logical Equivalences · Predicate Logic · Semantic Networks · Frames and Scripts · Rule-Based Representation · Ontologies and Knowledge Graphs · Comparing Methods · Where KR Is Used · Key Takeaways · Lab: Build a Knowledge Web · Practice Questions

Learning goals. By the end of this section, you can:

explain the difference between data, information and knowledge;
write simple facts in propositional and predicate logic;
store the same facts as a semantic network, a frame and a knowledge graph, and say which suits which job;
answer a question by following the links in a knowledge graph.
Before you start: read 2.1 What is Symbolic AI? first, so that symbol, fact and rule are familiar. No maths is needed beyond "true or false". The logic symbols →, ∧, ∨ and ¬ are taught in §4.1–4.2 and also used in 2.2 Logic and Reasoning.

Pixel's Mission
Byte works at the library desk. A student asks: "Which faculty is Alex's major in?" Byte starts reading 500 loose sentences, one by one.
Predict first: Which is fastest for answering: a list of sentences, a table, or linked facts? Write down your guess, then check it in §5.2, the lab and §10.

1. Where We Are in the Module
2.1 showed that Symbolic AI uses facts and rules; 2.2 showed how it reasons with them. This section asks how a computer stores that knowledge, for example the students, books and loans a library assistant must know. Reasoning (2.2) runs on top of this storage, and 2.4 Expert Systems combines both.

2. What is Knowledge Representation?
Knowledge Representation (KR) is organising and storing information about the world in a form a computer can use to answer questions, solve problems or make decisions. A record such as Name: Alex, Age: 19, Major: Computer Science is already a representation. Stating relationships (Alex is a student; Alex studies Computer Science; Alex attends Beijing Institute of Technology) makes it more useful: the computer now knows an object and how it relates to other things.

Why Do We Need Knowledge Representation?
A human sees at once that "Alex is a student" and "Alex studies Computer Science" describe the same person; a computer knows it only if the structure marks Alex as the subject of both. With that structure it can store, retrieve, relate and reason.

Important: KR does not mean the computer understands like a human. It means the information is organised so that a program can process it.

3. Data, Information and Knowledge
Term	Meaning	Example	Puzzle picture
Data	Raw values without context	19, Computer Science, Alex	Loose pieces
Information	Data in a meaningful context	Alex is 19 and studies Computer Science.	Pieces arranged into a picture
Knowledge	Information organised to support relationships and decisions	Computer Science students belong to the Computer Science department.	Understanding what the picture shows
Example. The record Student: Alex, Age: 19, Major: Computer Science is information. Add the rule

TEXT
复制
IF a student studies Computer Science
THEN the student belongs to the Computer Science department.
and the system can conclude a new fact: Alex belongs to the Computer Science department (Modus Ponens, from 2.2).

