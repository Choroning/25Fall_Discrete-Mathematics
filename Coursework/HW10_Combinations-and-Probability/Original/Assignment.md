# HW10 Assignment Handout — Combinations and Probability

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-24

This is Assignment 10 of Discrete Mathematics and Practice, given in Week 13. It consists of ten exercises chosen from Sections 9.5 (Counting Subsets of a Set: Combinations), 9.6 (r-Combinations with Repetition Allowed), 9.7 (Pascal's Formula and the Binomial Theorem), 9.8 (Probability Axioms and Expected Value), and 9.9 (Conditional Probability, Bayes' Formula, and Independent Events) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

---

<br>

## 1. Exercise 9.5.7: Choosing Teams under Conditions

A computer programming team has 13 members.

- (a) How many ways can a group of seven be chosen to work on a project?
- (b) Suppose seven team members are women and six are men.
  - (i) How many groups of seven can be chosen that contain four women and three men?
  - (ii) How many groups of seven can be chosen that contain at least one man?
  - (iii) How many groups of seven can be chosen that contain at most three women?
- (c) Suppose two team members refuse to work together on projects. How many groups of seven can be chosen to work on a project?
- (d) Suppose two team members insist on either working together or not at all on projects. How many groups of seven can be chosen to work on a project?

---

<br>

## 2. Exercise 9.5.17: Lines and Triangles Determined by Points

Ten points labeled $A, B, C, D, E, F, G, H, I, J$ are arranged in a plane in such a way that no three lie on the same straight line.

- (a) How many straight lines are determined by the ten points?
- (b) How many of these straight lines do not pass through point $A$?
- (c) How many triangles have three of the ten points as vertices?
- (d) How many of these triangles do not have point $A$ as a vertex?

---

<br>

## 3. Exercise 9.6.10: Number of Nonnegative Integer Solutions

How many solutions are there to the following equation if each $x_i$ is a nonnegative integer?

```math
x_1 + x_2 + x_3 = 20
```

---

<br>

## 4. Exercise 9.6.11: Number of Positive Integer Solutions

How many solutions are there to the following equation if each $x_i$ is a positive integer?

```math
x_1 + x_2 + x_3 = 20
```

---

<br>

## 5. Exercise 9.7.10: Pascal's Triangle

Table 9.7.1 of the textbook is Pascal's triangle through the row $n = 5$, with $\binom{n}{r}$ in row $n$ and column $r$.

| $n$ \\ $r$ | 0 | 1 | 2 | 3 | 4 | 5 |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| 0 | 1 | | | | | |
| 1 | 1 | 1 | | | | |
| 2 | 1 | 2 | 1 | | | |
| 3 | 1 | 3 | 3 | 1 | | |
| 4 | 1 | 4 | 6 | 4 | 1 | |
| 5 | 1 | 5 | 10 | 10 | 5 | 1 |

*Table 1. Pascal's triangle through the row n = 5*

- (a) Use Pascal's triangle in Table 1 to compute the values of $\binom{6}{2}$, $\binom{6}{3}$, $\binom{6}{4}$, and $\binom{6}{5}$.
- (b) Use the result of part (a) and Pascal's formula to compute $\binom{7}{3}$, $\binom{7}{4}$, and $\binom{7}{5}$.
- (c) Complete the row of Pascal's triangle that corresponds to $n = 7$.

---

<br>

## 6. Exercise 9.7.14: A Sum Formula with a Binomial Coefficient

Prove that if $n$ is an integer and $n \ge 1$, then the following identity holds.

```math
1 \cdot 2 + 2 \cdot 3 + \cdots + n(n+1) = 2\binom{n+2}{3}
```

---

<br>

## 7. Exercise 9.8.7: Applying the Probability Axioms

Suppose a sample space $S$ consists of three outcomes: 0, 1, and 2. Let $A = \lbrace 0 \rbrace$, $B = \lbrace 1 \rbrace$, and $C = \lbrace 2 \rbrace$, and suppose $P(A) = 0.4$ and $P(B) = 0.3$. Find each of the following.

- (a) $P(A \cup B)$
- (b) $P(C)$
- (c) $P(A \cup C)$
- (d) $P(A^c)$
- (e) $P(A^c \cap B^c)$
- (f) $P(A^c \cup B^c)$

---

<br>

## 8. Exercise 9.9.5: Conditional Probability Given a Complement

Suppose that $A$ and $B$ are events in a sample space $S$ and that $P(A)$, $P(B)$, and $P(A \mid B)$ are known. Derive a formula for $P(A \mid B^c)$.

---

<br>

## 9. Exercise 9.9.9: Bayes' Theorem for Two Events

Prove Bayes' theorem for $n = 2$. That is, prove that if a sample space $S$ is a union of mutually disjoint events $B_1$ and $B_2$, if $A$ is an event in $S$ with $P(A) \ne 0$, and if $k = 1$ or $k = 2$, then the following identity holds.

```math
P(B_k \mid A) = \frac{P(A \mid B_k)\,P(B_k)}{P(A \mid B_1)\,P(B_1) + P(A \mid B_2)\,P(B_2)}
```

---

<br>

## 10. Exercise 9.9.20: Coin Tosses and Independent Events

Suppose a fair coin is tossed three times. Let $A$ be the event that a head appears on the first toss, and let $B$ be the event that an even number of heads is obtained. Show that $P(A \mid B) = P(A)$ and $P(B \mid A) = P(B)$.

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
