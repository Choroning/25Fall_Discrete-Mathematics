# HW7 Assignment Handout — Functions and Cardinality

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-24

This is Assignment 7 of Discrete Mathematics and Practice, given in Week 10. It consists of eleven exercises chosen from Sections 7.1 (Functions Defined on General Sets), 7.2 (One-to-One, Onto, and Inverse Functions), 7.3 (Composition of Functions), and 7.4 (Cardinality with Applications to Computability) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

---

<br>

## 1. Exercise 7.1.9: The Sum-of-Positive-Divisors Function

Define a function $S: \mathbf{Z}^{+} \to \mathbf{Z}^{+}$ as follows: for each positive integer $n$, $S(n)$ is the sum of the positive divisors of $n$. Find the following.

- (a) $S(1)$
- (b) $S(15)$
- (c) $S(17)$
- (d) $S(5)$
- (e) $S(18)$
- (f) $S(21)$

---

<br>

## 2. Exercise 7.1.15: Equality of Product Functions

Let $F$ and $G$ be functions from the set of all real numbers to itself. Define the product functions $F \cdot G: \mathbf{R} \to \mathbf{R}$ and $G \cdot F: \mathbf{R} \to \mathbf{R}$ as follows, for every $x \in \mathbf{R}$.

```math
(F \cdot G)(x) = F(x) \cdot G(x), \qquad (G \cdot F)(x) = G(x) \cdot F(x)
```

Does $F \cdot G = G \cdot F$? Explain.

---

<br>

## 3. Exercise 7.1.21: The Logarithm of a Reciprocal

If $b$ is any positive real number with $b \neq 1$ and $x$ is any real number, $b^{-x}$ is defined by $b^{-x} = \frac{1}{b^x}$. Use this definition and the definition of logarithm to prove the following identity for all positive real numbers $u$ and $b$, with $b \neq 1$.

```math
\log_b\left(\frac{1}{u}\right) = -\log_b(u)
```

---

<br>

## 4. Exercise 7.2.10: Whether the Doubling Function Is One-to-One and Onto

- (a) Define $f: \mathbf{Z} \to \mathbf{Z}$ by the rule $f(n) = 2n$, for every integer $n$.
  - (i) Is $f$ one-to-one? Prove or give a counterexample.
  - (ii) Is $f$ onto? Prove or give a counterexample.
- (b) Let $2\mathbf{Z}$ denote the set of all even integers, that is, $2\mathbf{Z} = \lbrace n \in \mathbf{Z} \mid n = 2k \text{ for some integer } k \rbrace$. Define $h: \mathbf{Z} \to 2\mathbf{Z}$ by the rule $h(n) = 2n$, for each integer $n$. Is $h$ onto? Prove or give a counterexample.

---

<br>

## 5. Exercise 7.2.16: Testing a Rational Function for One-to-One

Determine whether or not the following function $f$, defined for each real number $x$, is one-to-one, and justify your answer.

```math
f(x) = \frac{x}{x^2 + 1}
```

---

<br>

## 6. Exercise 7.2.41: Onto Functions and the Image of an Inverse Image

Suppose $F: X \to Y$ is onto. Prove that for every subset $B \subseteq Y$, $F(F^{-1}(B)) = B$.

---

<br>

## 7. Exercise 7.3.7: Composing the Squaring Function and the mod 5 Function

Define $L: \mathbf{Z} \to \mathbf{Z}$ and $M: \mathbf{Z} \to \mathbf{Z}$ by the rules $L(a) = a^2$ and $M(a) = a \bmod 5$ for each integer $a$.

- (a) Find $(L \circ M)(12)$, $(M \circ L)(12)$, $(L \circ M)(9)$, and $(M \circ L)(9)$.
- (b) Is $L \circ M = M \circ L$?

---

<br>

## 8. Exercise 7.3.10: Composing the Doubling Function and the Floor Function

Define $F: \mathbf{Z} \to \mathbf{Z}$ and $G: \mathbf{Z} \to \mathbf{Z}$ by the rules $F(n) = 2n$ and $G(n) = \lfloor n/2 \rfloor$ for every integer $n$.

- (a) Find $(G \circ F)(8)$, $(F \circ G)(8)$, $(G \circ F)(3)$, and $(F \circ G)(3)$.
- (b) Is $G \circ F = F \circ G$? Explain.

---

<br>

## 9. Exercise 7.3.17: Composing a Function with Its Inverse

Prove Theorem 7.3.2(b): if $f: X \to Y$ is a one-to-one and onto function with inverse function $f^{-1}: Y \to X$, then $f \circ f^{-1} = I_Y$, where $I_Y$ is the identity function on $Y$.

---

<br>

## 10. Exercise 7.4.3: The Cardinality of the Integers and the Multiples of 3

Let $3\mathbf{Z} = \lbrace n \in \mathbf{Z} \mid n = 3k \text{ for some integer } k \rbrace$. Prove that $\mathbf{Z}$ and $3\mathbf{Z}$ have the same cardinality.

---

<br>

## 11. Exercise 7.4.10: The Cardinality of Two Open Intervals

Let $S$ denote the set of real numbers strictly between 0 and 1, that is, $S = \lbrace x \in \mathbf{R} \mid 0 < x < 1 \rbrace$, and let $U = \lbrace x \in \mathbf{R} \mid 0 < x < 2 \rbrace$. Prove that $S$ and $U$ have the same cardinality.

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
