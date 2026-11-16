# HW6 Assignment Handout — Set Theory and Boolean Algebra

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-16

This is Assignment 6 of Discrete Mathematics and Practice, given in Week 9. It consists of twelve exercises chosen from Sections 6.1 (Set Theory: Definitions and the Element Method of Proof), 6.2 (Properties of Sets), 6.3 (Disproofs and Algebraic Proofs), and 6.4 (Boolean Algebras, Russell's Paradox, and the Halting Problem) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

- **Deadline:** One week after the assignment is given; any late assignment receives zero points.
- **Submission:** Each group submits one set of answers.

---

<br>

## 1. Exercise 6.1.15: Venn Diagrams Satisfying Given Conditions

In each of the following, draw a Venn diagram for sets $A$, $B$, and $C$ that satisfy the given conditions.

- (a) $A \cap B = \emptyset$, $A \subseteq C$, $C \cap B \ne \emptyset$
- (b) $A \subseteq B$, $C \subseteq B$, $A \cap C \ne \emptyset$
- (c) $A \cap B \ne \emptyset$, $B \cap C \ne \emptyset$, $A \cap C = \emptyset$, $A \not\subseteq B$, $C \not\subseteq B$

---

<br>

## 2. Exercise 6.1.24: Unions and Intersections of Intervals

Let $W_i = \lbrace x \in \mathbf{R} \mid x > i \rbrace = (i, \infty)$ for each nonnegative integer $i$.

- (a) Find $\bigcup_{i=0}^{4} W_i$.
- (b) Find $\bigcap_{i=0}^{4} W_i$.
- (c) Are $W_0, W_1, W_2, \ldots$ mutually disjoint? Explain.
- (d) Find $\bigcup_{i=0}^{n} W_i$.
- (e) Find $\bigcap_{i=0}^{n} W_i$.
- (f) Find $\bigcup_{i=0}^{\infty} W_i$.
- (g) Find $\bigcap_{i=0}^{\infty} W_i$.

---

<br>

## 3. Exercise 6.1.33: Iterated Power Sets of the Empty Set

Find the following.

- (a) $\mathcal{P}(\emptyset)$
- (b) $\mathcal{P}(\mathcal{P}(\emptyset))$
- (c) $\mathcal{P}(\mathcal{P}(\mathcal{P}(\emptyset)))$

---

<br>

## 4. Exercise 6.2.7: An Element Argument for De Morgan's Law

Assume that all sets are subsets of a universal set $U$. Use an element argument to prove the following statement.

- For all sets $A$ and $B$, $(A \cap B)^c = A^c \cup B^c$.

---

<br>

## 5. Exercise 6.2.20: The Union of Two Subsets

Assume that all sets are subsets of a universal set $U$. Use an element argument to prove the following statement.

- For all sets $A$, $B$, and $C$, if $A \subseteq C$ and $B \subseteq C$ then $A \cup B \subseteq C$.

---

<br>

## 6. Exercise 6.2.30: The Intersection of a Set and Its Complement

Prove the following statement by contradiction.

- For every subset $A$ of a universal set $U$, $A \cap A^c = \emptyset$.

---

<br>

## 7. Exercise 6.3.8: The Union When a Complement Is Contained

Assume that all sets are subsets of a universal set $U$. Prove the following statement if it is true, and find a counterexample if it is false.

- For all sets $A$ and $B$, if $A^c \subseteq B$ then $A \cup B = U$.

---

<br>

## 8. Exercise 6.3.24: Subsets With and Without One Element

Let $A = \lbrace t, u, v, w \rbrace$, and let $S_1$ be the set of all subsets of $A$ that do not contain $w$ and $S_2$ the set of all subsets of $A$ that contain $w$.

- (a) Find $S_1$.
- (b) Find $S_2$.
- (c) Are $S_1$ and $S_2$ disjoint?
- (d) Compare the sizes of $S_1$ and $S_2$.
- (e) How many elements are in $S_1 \cup S_2$?
- (f) What is the relation between $S_1 \cup S_2$ and $\mathcal{P}(A)$?

---

<br>

## 9. Exercise 6.3.31: An Algebraic Proof for a Union Containing a Difference

Construct an algebraic proof for the following statement. Cite a property from Theorem 6.2.2 for every step.

- For all sets $A$ and $B$, $A \cup (B - A) = A \cup B$.

---

<br>

## 10. Exercise 6.4.1: The Idempotent Law for the Product

Assume that $B$ is a Boolean algebra with operations $+$ and $\cdot$. Give the reasons needed to fill in the blanks (a)-(e) in the following proof, using only the axioms for a Boolean algebra.

**Idempotent law for $\cdot$:** For every $a$ in $B$, $a \cdot a = a$.

**Proof.** Let $a$ be any element of $B$. Then the following holds.

```math
\begin{aligned}
a &= a \cdot 1 && \text{(a)} \\
&= a \cdot (a + \overline{a}) && \text{(b)} \\
&= (a \cdot a) + (a \cdot \overline{a}) && \text{(c)} \\
&= (a \cdot a) + 0 && \text{(d)} \\
&= a \cdot a && \text{(e)}
\end{aligned}
```

---

<br>

## 11. Exercise 6.4.3: The Absorption Law

Assume that $B$ is a Boolean algebra with operations $+$ and $\cdot$. Give the reasons needed to fill in the blanks (a)-(f) in the following proof, using only the axioms for a Boolean algebra. Exercise 6.4.1 is the idempotent law for the product, $a \cdot a = a$, and Exercise 6.4.2 is the universal bound law for the sum, $a + 1 = 1$.

**Absorption law for $\cdot$ over $+$:** For all $a$ and $b$ in $B$, $(a + b) \cdot a = a$.

**Proof.** Let $a$ and $b$ be any elements of $B$. Then the following holds.

```math
\begin{aligned}
(a + b) \cdot a &= a \cdot (a + b) && \text{(a)} \\
&= a \cdot a + a \cdot b && \text{(b)} \\
&= a + a \cdot b && \text{by exercise 6.4.1} \\
&= a \cdot 1 + a \cdot b && \text{(c)} \\
&= a \cdot (1 + b) && \text{(d)} \\
&= a \cdot (b + 1) && \text{(e)} \\
&= a \cdot 1 && \text{by exercise 6.4.2} \\
&= a && \text{(f)}
\end{aligned}
```

---

<br>

## 12. Exercise 6.4.6: Uniqueness of 0

Assume that $B$ is a Boolean algebra with operations $+$ and $\cdot$. Prove the following statement using only the axioms for a Boolean algebra and statements proved in the text or in lower-numbered exercises.

- There is only one element of $B$ that is an identity for $+$.

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
