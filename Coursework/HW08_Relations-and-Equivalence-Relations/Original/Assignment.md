# HW8 Assignment Handout — Relations and Equivalence Relations

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-24

This is Assignment 8 of Discrete Mathematics and Practice, given in Week 11. It consists of twelve exercises chosen from Sections 8.1 (Relations on Sets), 8.2 (Reflexivity, Symmetry, and Transitivity), and 8.3 (Equivalence Relations) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

---

<br>

## 1. Exercise 8.1.3: Congruence Modulo 3

The **congruence modulo 3** relation, $T$, is defined from $\mathbf{Z}$ to $\mathbf{Z}$ as follows: for all integers $m$ and $n$, $`m \, T \, n \iff 3 \mid (m - n)`$.

- (a) Is $`10 \, T \, 1`$? Is $`1 \, T \, 10`$? Is $(2, 2) \in T$? Is $(8, 1) \in T$?
- (b) List five integers $n$ such that $`n \, T \, 0`$.
- (c) List five integers $n$ such that $`n \, T \, 1`$.
- (d) List five integers $n$ such that $`n \, T \, 2`$.

---

<br>

## 2. Exercise 8.1.8: Strings with the Same First Two Characters

Let $A$ be the set of all strings of $a$'s and $b$'s of length 4. Define a relation $R$ on $A$ as follows: for every $s, t \in A$, "$`s \, R \, t \iff s`$ has the same first two characters as $t$".

- (a) Is $`abaa \, R \, abba`$?
- (b) Is $`aabb \, R \, bbaa`$?
- (c) Is $`aaaa \, R \, aaab`$?
- (d) Is $`baaa \, R \, abaa`$?

---

<br>

## 3. Exercise 8.1.15: The Directed Graph of a Divisibility Relation

Let $A = \lbrace 2, 3, 4, 5, 6, 7, 8 \rbrace$ and define a relation $R$ on $A$ as follows: for every $x, y \in A$, $`x \, R \, y \iff x \mid y`$. Draw the directed graph of the relation.

---

<br>

## 4. Exercise 8.1.23: Relations in the Cartesian Plane and Their Union and Intersection

Define relations $R$ and $S$ on $\mathbf{R}$ as follows. Graph $R$, $S$, $R \cup S$, and $R \cap S$ in the Cartesian plane.

```math
R = \lbrace (x, y) \in \mathbf{R} \times \mathbf{R} \mid y = \vert x \vert \rbrace, \qquad S = \lbrace (x, y) \in \mathbf{R} \times \mathbf{R} \mid y = 1 \rbrace
```

---

<br>

## 5. Exercise 8.2.3: Properties of a Relation with Two Ordered Pairs

Answer the following questions for the relation $R_3 = \lbrace (2, 3), (3, 2) \rbrace$ on the set $A = \lbrace 0, 1, 2, 3 \rbrace$. Give a counterexample in each case in which the relation does not satisfy one of the properties.

- (a) Draw the directed graph.
- (b) Determine whether the relation is reflexive.
- (c) Determine whether the relation is symmetric.
- (d) Determine whether the relation is transitive.

---

<br>

## 6. Exercise 8.2.11: The Relation of a Nonnegative Product

$D$ is the relation defined on $\mathbf{R}$ as follows: for every $x, y \in \mathbf{R}$, $`x \, D \, y \iff xy \ge 0`$. Determine whether $D$ is reflexive, symmetric, transitive, or none of these, and justify your answers.

---

<br>

## 7. Exercise 8.2.23: The Subset Relation on a Power Set

Let $X$ be a nonempty set and $\mathcal{P}(X)$ the power set of $X$. Define the subset relation $\mathbf{S}$ on $\mathcal{P}(X)$ as follows: for every $A, B \in \mathcal{P}(X)$, $`A \, \mathbf{S} \, B \iff A \subseteq B`$. Determine whether $\mathbf{S}$ is reflexive, symmetric, transitive, or none of these, and justify your answers.

---

<br>

## 8. Exercise 8.2.36: The Inverse of a Transitive Relation

Assume that $R$ is a relation on a set $A$. Prove or disprove the following statement.

- If $R$ is transitive, then $R^{-1}$ is transitive.

---

<br>

## 9. Exercise 8.3.3: Equivalence Classes of a Relation Given as Ordered Pairs

The relation $R$ is an equivalence relation on $A = \lbrace 0, 1, 2, 3, 4 \rbrace$. First find the equivalence classes $[0]$, $[1]$, $[2]$, and $[3]$. Then state the number of distinct equivalence classes for $R$ and list them.

```math
R = \lbrace (0, 0), (0, 4), (1, 1), (1, 3), (2, 2), (3, 1), (3, 3), (4, 0), (4, 4) \rbrace
```

---

<br>

## 10. Exercise 8.3.8: Equivalence Classes of Subsets with the Same Number of Elements

Let $X = \lbrace a, b, c \rbrace$ and $A = \mathcal{P}(X)$. $R$ is defined on $A$ as follows: for all sets $U$ and $V$ in $\mathcal{P}(X)$, $`U \, R \, V \iff N(U) = N(V)`$, that is, the number of elements in $U$ equals the number of elements in $V$. The relation $R$ is an equivalence relation on $A$. Find the distinct equivalence classes of $R$.

---

<br>

## 11. Exercise 8.3.16: Equivalence Classes of Congruence Modulo 3 and 7

- (a) Let $R$ be the relation of congruence modulo 3. Which of the following equivalence classes are equal?

```math
[7], \quad [-4], \quad [-6], \quad [17], \quad [4], \quad [27], \quad [19]
```

- (b) Let $R$ be the relation of congruence modulo 7. Which of the following equivalence classes are equal?

```math
[35], \quad [3], \quad [-7], \quad [12], \quad [0], \quad [-2], \quad [17]
```

---

<br>

## 12. Exercise 8.3.20: Congruence Modulo 4

$E$ is the relation defined on $\mathbf{Z}$ as follows: for every $m, n \in \mathbf{Z}$, $`m \, E \, n \iff 4 \mid (m - n)`$. (1) Prove that $E$ is an equivalence relation, and (2) describe the distinct equivalence classes of $E$.

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
