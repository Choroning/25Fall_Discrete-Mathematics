# HW3 Assignment Handout — Multiple Quantifiers and Direct Proof

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-24

This is Assignment 3 of Discrete Mathematics and Practice, given in Week 4. It consists of eleven exercises chosen from Sections 3.3 (Statements with Multiple Quantifiers), 3.4 (Arguments with Quantified Statements), 4.1 (Direct Proof and Counterexample I: Introduction), and 4.2 (Direct Proof and Counterexample II: Writing Advice) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

---

<br>

## 1. Exercise 3.3.2: Truth Values of a Two-Variable Predicate

Let $G(x, y)$ be the predicate "$`x^2 > y`$". Indicate which of the following statements are true and which are false.

- (a) $G(2, 3)$
- (b) $G(1, 1)$
- (c) $G\left(\frac{1}{2}, \frac{1}{2}\right)$
- (d) $G(-2, 2)$

---

<br>

## 2. Exercise 3.3.12: Negations and Truth Values of Multiply-Quantified Statements

Let $D = E = \lbrace -2, -1, 0, 1, 2 \rbrace$. Write negations for each of the following statements and determine which is true, the given statement or its negation.

- (a) $\forall x \in D$, $\exists y \in E$ such that $x + y = 1$.
- (b) $\exists x \in D$ such that $\forall y \in E$, $x + y = -y$.

---

<br>

## 3. Exercise 3.3.22: Order of Quantifiers

Rewrite each statement without using variables or the symbol $\forall$ or $\exists$, and indicate whether the statement is true or false.

- (a) $\forall$ real number $x$, $\exists$ a real number $y$ such that $x + y = 0$.
- (b) $\exists$ a real number $y$ such that $\forall$ real number $x$, $x + y = 0$.

---

<br>

## 4. Exercise 3.3.24: Deriving Negation Rules for Multiple Quantifiers

Use the laws for negating universal and existential statements to derive the following rules.

- (a) $`\sim\big(\forall x \in D\,(\forall y \in E\,(P(x, y)))\big) \equiv \exists x \in D\,(\exists y \in E\,(\sim P(x, y)))`$
- (b) $`\sim\big(\exists x \in D\,(\exists y \in E\,(P(x, y)))\big) \equiv \forall x \in D\,(\forall y \in E\,(\sim P(x, y)))`$

---

<br>

## 5. Exercise 3.4.5: Universal Modus Tollens

Use universal modus tollens to fill in a valid conclusion for the following argument.

- Premise 1: all irrational numbers are real numbers.
- Premise 2: $\frac{1}{0}$ is not a real number.
- Conclusion: \_\_\_\_.

---

<br>

## 6. Exercise 3.4.16: Testing the Validity of an Argument About Twice a Number

State whether the following argument is valid by universal modus ponens or universal modus tollens, or invalid because it exhibits the converse or the inverse error, and justify your answer. According to the instructions of the textbook, some of the arguments in Exercises 3.4.7 through 3.4.18 are valid by universal modus ponens or universal modus tollens, whereas others are invalid and exhibit the converse or the inverse error.

- Premise 1: if a number is even, then twice that number is even.
- Premise 2: the number $2n$ is even, for a particular number $n$.
- Conclusion: the particular number $n$ is even.

---

<br>

## 7. Exercise 3.4.21: Testing Validity with a Diagram

Indicate whether the following argument is valid or invalid, and support your answer by drawing a diagram.

- Premise 1: all people are mice.
- Premise 2: all mice are mortal.
- Conclusion: all people are mortal.

---

<br>

## 8. Exercise 4.1.1: Definitions of Even and Odd

Assume that $k$ is a particular integer. Justify your answers to the following questions by using the definitions of even, odd, prime, and composite numbers.

- (a) Is $-17$ an odd integer?
- (b) Is 0 neither even nor odd?
- (c) Is $2k - 1$ odd?

---

<br>

## 9. Exercise 4.1.12: Negation and Counterexample

For the following statement, (a) write a negation, and (b) use a counterexample to disprove the statement. Explain how the counterexample actually shows that the given statement is false.

- For all real numbers $a$ and $b$, if $a < b$ then $a^2 < b^2$.

---

<br>

## 10. Exercise 4.1.29: Filling in a Direct Proof

Answer the following questions about the theorem and its proof below.

- (a) Rewrite the theorem in three different ways: as "$`\forall`$ \_\_\_\_, if \_\_\_\_ then \_\_\_\_", as "$`\forall`$ \_\_\_\_, \_\_\_\_" (without using the words if or then), and as "If \_\_\_\_, then \_\_\_\_" (without using an explicit universal quantifier).
- (b) Fill in the blanks (a)-(d) in the proof.

**Theorem.** The negative of any even integer is even.

**Proof.** Suppose $n$ is any [particular but arbitrarily chosen] even integer. [It must be shown that $-n$ is even.] By \_\_(a)\_\_, $n = 2k$ for some integer $k$. Then the following holds.

```math
\begin{aligned}
-n &= -(2k) && \text{by \_\_(b)\_\_} \\
&= 2(-k) && \text{by algebra}
\end{aligned}
```

Let $r = -k$. Then $r$ is an integer because $-1$ and $k$ are integers and \_\_(c)\_\_. Hence $-n = 2r$, where $r$ is an integer, and so $-n$ is even by \_\_(d)\_\_. [This is what was to be shown.]

---

<br>

## 11. Exercise 4.2.15: Finding the Mistake in a Proof

Find the mistake in the "proof" offered for the following theorem.

- Theorem: for every integer $k$, if $k > 0$ then $k^2 + 2k + 1$ is composite.
- Offered proof: for $k = 2$, $k > 0$ and $k^2 + 2k + 1 = 2^2 + 2 \cdot 2 + 1 = 9$. And since $9 = 3 \cdot 3$, 9 is composite. Hence the theorem is true.

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
