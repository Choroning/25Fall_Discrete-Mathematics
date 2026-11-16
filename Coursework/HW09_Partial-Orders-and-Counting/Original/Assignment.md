# HW9 Assignment Handout — Partial Orders and Counting

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-16

This is Assignment 9 of Discrete Mathematics and Practice, given in Week 12. It consists of twelve exercises chosen from Sections 8.5 (Partial Order Relations), 9.1 (Introduction to Probability), 9.2 (Possibility Trees and the Multiplication Rule), 9.3 (Counting Elements of Disjoint Sets: The Addition Rule), and 9.4 (The Pigeonhole Principle) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

- **Deadline:** One week after the assignment is given; any late assignment receives zero points.
- **Submission:** Each group submits one set of answers.

---

<br>

## 1. Exercise 8.5.1: Deciding Antisymmetry

Each of the following is a relation on $\lbrace 0, 1, 2, 3 \rbrace$. Draw directed graphs for each relation, and indicate which relations are antisymmetric.

- (a) $R_1 = \lbrace (0, 0), (0, 2), (1, 0), (1, 3), (2, 2), (3, 0), (3, 1) \rbrace$
- (b) $R_2 = \lbrace (0, 1), (0, 2), (1, 1), (1, 2), (1, 3), (2, 2), (3, 2) \rbrace$
- (c) $R_3 = \lbrace (0, 0), (0, 3), (1, 0), (1, 3), (2, 2), (3, 3), (3, 2) \rbrace$
- (d) $R_4 = \lbrace (0, 0), (1, 0), (1, 2), (1, 3), (2, 0), (2, 1), (3, 2), (3, 0) \rbrace$

---

<br>

## 2. Exercise 8.5.7: Inclusion of Prime Factors

Define a relation $R$ on $\mathbf{Z}$, the set of all integers, as follows: for every $m, n \in \mathbf{Z}$, "$`m \, R \, n \iff`$ every prime factor of $m$ is a prime factor of $n$". Is $R$ a partial order relation? Prove or give a counterexample.

---

<br>

## 3. Exercise 8.5.17: Hasse Diagrams of Power Sets

Consider the subset relation on $\mathcal{P}(S)$ for each of the following sets $S$. Draw the Hasse diagram for each relation.

- (a) $S = \lbrace 0, 1 \rbrace$
- (b) $S = \lbrace 0, 1, 2 \rbrace$

---

<br>

## 4. Exercise 8.5.31: Deciding a Total Order

Let $A = \lbrace a, b, c, d \rbrace$, and let $R$ be the following relation. Is $R$ a total order on $A$? Justify your answer.

```math
R = \lbrace (a, a), (b, b), (c, c), (d, d), (c, a), (a, d), (c, d), (b, c), (b, d), (b, a) \rbrace
```

---

<br>

## 5. Exercise 9.1.12: The Genders of Three Children

Suppose that each child born is equally likely to be a boy or a girl. Consider a family with exactly three children. Let $BBG$ indicate that the first two children born are boys and the third child is a girl, let $GBG$ indicate that the first and third children born are girls and the second is a boy, and so forth.

- (a) List the eight elements in the sample space whose outcomes are all possible genders of the three children.
- (b) Write each of the following events as a set and find its probability.
  - (i) The event that exactly one child is a girl.
  - (ii) The event that at least two children are girls.
  - (iii) The event that no child is a girl.

---

<br>

## 6. Exercise 9.1.25: The Size of a Subarray and a Probability

Suppose $A[1], A[2], \ldots, A[n]$ is a one-dimensional array and $n \ge 2$. Consider the following subarray.

```math
A[\lfloor n/2 \rfloor], \ A[\lfloor n/2 \rfloor + 1], \ \ldots, \ A[n]
```

- (a) How many elements are in the subarray (i) if $n$ is even? and (ii) if $n$ is odd?
- (b) What is the probability that a randomly chosen array element is in the subarray (i) if $n$ is even? and (ii) if $n$ is odd?

---

<br>

## 7. Exercise 9.2.16: Counting Two-Digit Integers

- (a) How many integers are there from 10 through 99?
- (b) How many odd integers are there from 10 through 99?
- (c) How many integers from 10 through 99 have distinct digits?
- (d) How many odd integers from 10 through 99 have distinct digits?
- (e) What is the probability that a randomly chosen two-digit integer has distinct digits? has distinct digits and is odd?

---

<br>

## 8. Exercise 9.2.41: An Identity about Numbers of Permutations

Prove that the following identity holds for every integer $n \ge 2$.

```math
P(n + 1, 2) - P(n, 2) = 2P(n, 1)
```

---

<br>

## 9. Exercise 9.3.7: Counting Passwords

At a certain company, passwords must be from 3-5 symbols long and composed from the 26 uppercase letters of the Roman alphabet, the ten digits 0-9, and the 14 symbols `!`, `@`, `#`, `$`, `%`, `^`, `&`, `*`, `(`, `)`, `-`, `+`, `{`, and `}`.

- (a) How many passwords are possible if repetition of symbols is allowed?
- (b) How many passwords contain no repeated symbols?
- (c) How many passwords have at least one repeated symbol?
- (d) What is the probability that a password chosen at random has at least one repeated symbol?

---

<br>

## 10. Exercise 9.3.40: The Euler Phi Function of a Product of Two Primes

The Euler phi function $\varphi$ is the function defined in Section 7.1, exercises 51-53: for each integer $n \ge 1$, $\varphi(n)$ is the number of positive integers less than or equal to $n$ that have no common factors with $n$ except $\pm 1$. Use the inclusion/exclusion principle to prove the following statement.

- If $n = pq$, where $p$ and $q$ are distinct prime numbers, then $\varphi(n) = (p - 1)(q - 1)$.

---

<br>

## 11. Exercise 9.4.10: n + 1 Integers and an Odd Integer

If $n + 1$ integers are chosen from the set $\lbrace 1, 2, 3, \ldots, 2n \rbrace$, where $n$ is a positive integer, must at least one of them be odd? Why?

---

<br>

## 12. Exercise 9.4.16: How Many Picks Guarantee a Multiple of 5

How many integers from 1 through 100 must you pick in order to be sure of getting one that is divisible by 5?

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
