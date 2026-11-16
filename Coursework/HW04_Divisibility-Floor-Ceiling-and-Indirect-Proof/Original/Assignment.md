# HW4 Assignment Handout — Divisibility, Floor and Ceiling, and Indirect Proof

[Repository Guide](../../../README.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **Last Updated:** 2026-11-16

This is Assignment 4 of Discrete Mathematics and Practice, given in Week 5. It consists of nine exercises chosen from Sections 4.4 (Direct Proof and Counterexample IV: Divisibility), 4.5 (Direct Proof and Counterexample V: Division into Cases and the Quotient-Remainder Theorem), 4.6 (Direct Proof and Counterexample VI: Floor and Ceiling), and 4.8 (Indirect Argument: Two Famous Theorems) of the textbook Discrete Mathematics with Applications (Epp), and the problem numbers are the exercise numbers of the textbook.

- **Deadline:** One week after the assignment is given; any late assignment receives zero points. Because there were no classes in Week 6 for the Chuseok holiday, it was submitted in Week 7.
- **Submission:** Each group submits one set of answers.

---

<br>

## 1. Exercise 4.4.4: A Product of Three Consecutive Integers and 3

Assume that all variables represent integers. Does 3 divide $(3k+1)(3k+2)(3k+3)$? Give a reason for your answer.

---

<br>

## 2. Exercise 4.4.15: Divisibility of a Sum

Prove the following statement directly from the definition of divisibility.

- For all integers $a, b, c$, if $a \mid b$ and $a \mid c$ then $a \mid (b + c)$.

---

<br>

## 3. Exercise 4.4.24: Divisibility of a Linear Combination

Determine whether the following statement is true or false. Prove the statement directly from the definitions if it is true, and give a counterexample if it is false.

- For all integers $a, b, c$, if $a \mid b$ and $a \mid c$ then $a \mid (2b - 3c)$.

---

<br>

## 4. Exercise 4.4.44: Numbers Ending in 0 and Divisibility by 5

Given any nonnegative integer $n$, the **decimal representation** of $n$ is an expression of the form $d_k d_{k-1} \cdots d_2 d_1 d_0$, where $k$ is a nonnegative integer, $d_0, d_1, d_2, \ldots, d_k$ (called the **decimal digits** of $n$) are integers from 0 to 9 inclusive, $d_k \ne 0$ unless $n = 0$ and $k = 0$, and the following equation holds. For example, $2{,}503 = 2 \cdot 10^3 + 5 \cdot 10^2 + 0 \cdot 10 + 3$.

```math
n = d_k \cdot 10^k + d_{k-1} \cdot 10^{k-1} + \cdots + d_2 \cdot 10^2 + d_1 \cdot 10 + d_0
```

Prove that if $n$ is any nonnegative integer whose decimal representation ends in 0, then $5 \mid n$. (Hint: if the decimal representation of a nonnegative integer $n$ ends in $d_0$, then $n = 10m + d_0$ for some integer $m$.)

---

<br>

## 5. Exercise 4.5.16: The Remainder When d Divides n

Suppose $d$ is a positive integer and $n$ is any integer. If $d \mid n$, what is the remainder obtained when the quotient-remainder theorem is applied to $n$ with divisor $d$?

---

<br>

## 6. Exercise 4.6.7: The Ceiling of an Integer Plus One Half

If $k$ is an integer, what is $\lceil k + \frac{1}{2} \rceil$? Why?

---

<br>

## 7. Exercise 4.6.13: The Floor of Half an Even Integer

Prove that if $n$ is any even integer, then $\lfloor n/2 \rfloor = n/2$.

---

<br>

## 8. Exercise 4.8.6: Deciding Irrationality

Determine whether the following statement is true or false. Prove it if it is true, and disprove it if it is false.

- $6 - 7\sqrt{2}$ is irrational.

---

<br>

## 9. Exercise 4.8.28: Remainders of a Product of Primes Plus 1

Let $N = 2 \cdot 3 \cdot 5 \cdot 7 + 1$. What remainder is obtained when $N$ is divided by 2? 3? 5? 7? Justify your answer.

---

<br>

After solving the problems, see the [assignment explanation](../Assignment-Explanation.md) for the answers and solutions.
