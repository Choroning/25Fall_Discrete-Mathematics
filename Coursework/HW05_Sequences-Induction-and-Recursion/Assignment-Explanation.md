# HW5 Assignment Explanation — Sequences, Mathematical Induction, and Recursion

[Repository Guide](../../README.md) | [English](Assignment-Explanation.md) | [한국어](Assignment-Explanation.ko.md)

> **Last Updated:** 2026-11-04
>
> Discrete Mathematics with Applications, Epp, Ch 5

> **Learning Objectives:**
> 1. Find the general term of a finite sum with alternating signs, write the sum in summation notation, and explain why different expressions of the same sum agree
> 2. Derive a formula for a geometric sum whose exponents run from $m$ to $m + n$ by using the formula for the sum of a geometric sequence, and treat the case $r = 1$ separately
> 3. Write $P(a)$, $P(k)$, and $P(k+1)$ for a proof of an inequality by mathematical induction and state exactly what must be shown in the inductive step
> 4. Prove the inequality $2^n < (n+1)!$ by mathematical induction
> 5. Compute the terms of a sequence defined by a recurrence relation and initial conditions, and reveal its structure through an auxiliary sequence

---

## Table of Contents

- [1. Exercise 5.1.47: An Alternating Sum](#1-exercise-5147-an-alternating-sum)
- [2. Exercise 5.2.34: A Formula for a Geometric Sum](#2-exercise-5234-a-formula-for-a-geometric-sum)
- [3. Exercise 5.3.5: An Inequality Between a Power and a Factorial](#3-exercise-535-an-inequality-between-a-power-and-a-factorial)
- [4. Exercise 5.6.8: Terms of a Recursively Defined Sequence](#4-exercise-568-terms-of-a-recursively-defined-sequence)
- [Summary](#summary)
- [Self-Check Questions](#self-check-questions)

---

<br>

## 1. Exercise 5.1.47: An Alternating Sum

**Problem.** Rewrite $1 - r + r^2 - r^3 + r^4 - r^5$ compactly with summation or product notation.

**Concept used.** Summation notation from [Chapter 5, Section 1](../../Lecture-Notes/Ch05_Sequences-Mathematical-Induction-and-Recursion/Concepts_Lecture.md). For integers $m \le n$, $\sum_{k=m}^{n} a_k = a_m + a_{m+1} + \cdots + a_n$, where $k$ is the index, $m$ the lower limit, and $n$ the upper limit. The given expression adds terms, so summation notation is used, and for that the general term $a_k$ expressing each term as a formula in the index $k$ must be found.

**Solution.** Analyze the terms one at a time. The first term 1 equals $r^0$, so every term is a power of $r$ with a sign, and the exponents increase by 1 from 0 to 5. The signs alternate as $+, -, +, -, \ldots$, with $+$ for even exponents and $-$ for odd exponents. Since $(-1)^k$ equals 1 when $k$ is even and $-1$ when $k$ is odd, it represents these signs exactly.

| $k$ | 0 | 1 | 2 | 3 | 4 | 5 |
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|:-----:|
| Sign $(-1)^k$ | $1$ | $-1$ | $1$ | $-1$ | $1$ | $-1$ |
| Power $r^k$ | $1$ | $r$ | $r^2$ | $r^3$ | $r^4$ | $r^5$ |
| Term $(-1)^k r^k$ | $1$ | $-r$ | $r^2$ | $-r^3$ | $r^4$ | $-r^5$ |

*Table 1. The sign, power, and term for each index k*

Hence the term with index $k$ is $(-1)^k r^k$, and since $k$ runs from 0 to 5 the sum is written as follows.

```math
1 - r + r^2 - r^3 + r^4 - r^5 = \sum_{k=0}^{5} (-1)^k r^k
```

**Answer.** $\sum_{k=0}^{5} (-1)^k r^k$. Expanding the summation reproduces the last row of Table 1, so it equals the original expression.

> **Caution:** The parentheses in $(-1)^k$ cannot be omitted. $-1^k$ is read as $-(1^k) = -1$, which would make every sign negative. Also, the first term 1 must be seen as $r^0$ so that all terms follow one general term with the index starting at 0. For sums and polynomials, $0^0 = 1$ by convention, so that the first term is 1 even when $r = 0$.

> **Note:** The same sum can be written in several ways. (1) Since $(-1)^k r^k = (-r)^k$, it can be written $\sum_{k=0}^{5} (-r)^k$. (2) Changing the index to $j = k + 1$ gives $\sum_{j=1}^{6} (-1)^{j-1} r^{j-1}$. (3) The sum is a geometric sum with ratio $-r$, so substituting $-r$ into Theorem 5.2.2 gives, for $r \ne -1$, $\sum_{k=0}^{5} (-r)^k = \frac{(-r)^6 - 1}{-r - 1} = \frac{1 - r^6}{1 + r}$.

---

<br>

## 2. Exercise 5.2.34: A Formula for a Geometric Sum

**Problem.** For integers $m$ and $n$ with $n \ge 0$ and real numbers $a$ and $r$, express the sum $ar^m + ar^{m+1} + ar^{m+2} + \cdots + ar^{m+n}$ by a formula in $a, r, m, n$, with justification.

**Concept used.** Theorem 5.2.2 (the sum of a geometric sequence) in [Chapter 5, Section 2](../../Lecture-Notes/Ch05_Sequences-Mathematical-Induction-and-Recursion/Concepts_Lecture.md) states that the following holds for any real number $r$ except 1 and any integer $n \ge 0$, and it is proved there by mathematical induction.

```math
\sum_{i=0}^{n} r^i = \frac{r^{n+1} - 1}{r - 1} \qquad (r \ne 1)
```

In addition, the generalized distributive law $c \cdot \sum_{i} a_i = \sum_{i} c \cdot a_i$ of Theorem 5.1.1 lets a common factor be moved outside a summation.

**Solution.** Let $S$ denote the required sum.

1. The exponents are $m, m+1, \ldots, m+n$, so for each $i = 0, 1, \ldots, n$ there is exactly one term with exponent $m + i$. Hence there are $n + 1$ terms and $S = \sum_{i=0}^{n} ar^{m+i}$.
2. By the laws of exponents $ar^{m+i} = ar^m \cdot r^i$, so the generalized distributive law moves the common factor $ar^m$ outside.

```math
S = \sum_{i=0}^{n} ar^{m+i} = \sum_{i=0}^{n} ar^m \cdot r^i = ar^m \sum_{i=0}^{n} r^i
```

3. If $r \ne 1$, Theorem 5.2.2 applies, so $S = ar^m \cdot \frac{r^{n+1} - 1}{r - 1}$.
4. If $r = 1$, the denominator $r - 1$ is 0 and Theorem 5.2.2 does not apply. In this case every term is $a \cdot 1^{m+i} = a$ and there are $n + 1$ terms, so $S = a(n + 1)$.

**Answer.**

```math
ar^m + ar^{m+1} + \cdots + ar^{m+n} = \begin{cases} ar^m \cdot \dfrac{r^{n+1} - 1}{r - 1} & (r \ne 1) \\ a(n + 1) & (r = 1) \end{cases}
```

For example, with $a = 3$, $r = 2$, $m = 2$, $n = 3$, direct addition gives $12 + 24 + 48 + 96 = 180$, and the formula gives $3 \cdot 2^2 \cdot \frac{2^4 - 1}{2 - 1} = 12 \cdot 15 = 180$. With $a = 5$, $r = 1$, $m = 7$, $n = 3$, the sum is $5 + 5 + 5 + 5 = 20 = 5 \cdot 4$.

> **Caution:** Do not leave out the case $r = 1$. Theorem 5.2.2 assumes $r \ne 1$, and for $r = 1$ the denominator $r - 1$ of the formula is 0, so the expression is undefined. The problem allows $r$ to be any real number, so a complete answer must cover both cases.

> **Note:** The formula can also be obtained without Theorem 5.2.2. Since $rS = ar^{m+1} + ar^{m+2} + \cdots + ar^{m+n+1}$, computing $S - rS$ cancels all the middle terms and gives $(1 - r)S = ar^m - ar^{m+n+1} = ar^m(1 - r^{n+1})$. If $r \ne 1$, dividing both sides by $1 - r$ gives $S = ar^m \cdot \frac{1 - r^{n+1}}{1 - r}$, and multiplying numerator and denominator by $-1$ yields the answer above. The result can also be remembered as $\frac{(\text{last term}) \cdot r - (\text{first term})}{r - 1}$.

> **Caution:** If $m$ is negative, $r^m$ is defined only when $r \ne 0$. In that case the sum in the problem itself makes sense only for $r \ne 0$, and the same condition carries over to the formula in the answer.

---

<br>

## 3. Exercise 5.3.5: An Inequality Between a Power and a Factorial

**Problem.** For a positive integer $n$, $P(n)$ denotes the inequality $2^n < (n+1)!$.

- (a) Write $P(2)$ and decide whether it is true.
- (b) Write $P(k)$.
- (c) Write $P(k+1)$.
- (d) State the goal of the inductive step when the inequality is proved by mathematical induction for every integer $n \ge 2$.

**Concept used.** The method of proof by mathematical induction from [Chapter 5, Sections 2 and 3](../../Lecture-Notes/Ch05_Sequences-Mathematical-Induction-and-Recursion/Concepts_Lecture.md). To prove "for every integer $n \ge a$, $P(n)$", show in the basis step that $P(a)$ is true, and show in the inductive step that for every integer $k \ge a$, if $P(k)$ is true then $P(k+1)$ is true. $P(k)$ and $P(k+1)$ are written by copying $P(n)$ and replacing every $n$ by $k$ and by $(k+1)$, respectively. The factorial is $n! = n \cdot (n-1) \cdots 2 \cdot 1$ with $0! = 1$, and $(k+2)! = (k+2) \cdot (k+1)!$.

**Solution.**

- **(a)** $P(2)$ is $2^2 < (2+1)!$, that is, $4 < 3!$. Since $3! = 3 \cdot 2 \cdot 1 = 6$ and $4 < 6$, $P(2)$ is true.
- **(b)** $P(k)$ is $2^k < (k+1)!$.
- **(c)** $P(k+1)$ is $2^{k+1} < ((k+1)+1)!$, that is, $2^{k+1} < (k+2)!$.
- **(d)** It must be shown that for every integer $k \ge 2$, if $2^k < (k+1)!$ then $2^{k+1} < (k+2)!$. That is, for a particular but arbitrarily chosen integer $k \ge 2$, suppose the inductive hypothesis $2^k < (k+1)!$ is true and derive $2^{k+1} < (k+2)!$ from it.

Comparing the two sides for small $n$ shows why the proof starts at $n = 2$.

| $n$ | 1 | 2 | 3 | 4 | 5 |
|:-----|:-----:|:-----:|:-----:|:-----:|:-----:|
| $2^n$ | 2 | 4 | 8 | 16 | 32 |
| $(n+1)!$ | 2 | 6 | 24 | 120 | 720 |
| $P(n)$ | False | True | True | True | True |

*Table 2. Comparison of the power and the factorial for n = 1 to 5*

$P(1)$ is $2 < 2$, which is false. So although $P(n)$ is defined for every positive integer, the statement to be proved concerns integers $n \ge 2$, and the basis step is $P(2)$.

**Completing the proof.** Carrying out the inductive step described in (d) completes the proof of the inequality (exercise 5.3.16).

**Basis step: show that $P(2)$ is true.** This was shown in (a).

**Inductive step: show that for every integer $k \ge 2$, if $P(k)$ then $P(k+1)$.** Suppose $k$ is an integer with $k \ge 2$ and the inductive hypothesis $2^k < (k+1)!$ is true. It must be shown that $2^{k+1} < (k+2)!$.

```math
\begin{aligned}
2^{k+1} &= 2 \cdot 2^k && \text{(1)} \\
&< 2 \cdot (k+1)! && \text{(2)} \\
&< (k+2) \cdot (k+1)! && \text{(3)} \\
&= (k+2)! && \text{(4)}
\end{aligned}
```

Step (1) is a law of exponents, and step (2) multiplies both sides of the inductive hypothesis by the positive number 2. Step (3) uses the fact that $k \ge 2$ gives $k + 2 \ge 4 > 2$ and $(k+1)! > 0$, so $2 \cdot (k+1)! < (k+2) \cdot (k+1)!$, and step (4) is the definition of factorial. By the transitivity of order, $2^{k+1} < (k+2)!$, so $P(k+1)$ is true. Since both the basis step and the inductive step have been proved, $2^n < (n+1)!$ for every integer $n \ge 2$.

> **Caution:** $P(k)$ is a sentence (an inequality), not a number. Do not write "$`P(k) = 2^k`$"; write the whole property, as in "$`P(k)`$: $2^k < (k+1)!$". Also, writing $P(k+1)$ replaces $n$ by the parenthesized $(k+1)$, so $(n+1)!$ becomes $((k+1)+1)! = (k+2)!$. Writing it as $(k+1)! + 1$ is wrong.

> **Note:** Step (3) needs only $k + 2 > 2$, that is, $k \ge 1$, so the inductive step itself also holds for $k = 1$. The proof still cannot start at $n = 1$ because $P(1)$ is false and the basis step fails. This example shows that neither of the two steps of mathematical induction can be omitted.

---

<br>

## 4. Exercise 5.6.8: Terms of a Recursively Defined Sequence

**Problem.** A sequence $v_1, v_2, v_3, \ldots$ is defined by the recurrence relation $v_k = v_{k-1} + v_{k-2} + 1$ for every integer $k \ge 3$ and the initial conditions $v_1 = 1$, $v_2 = 3$. Find the first four terms of the sequence.

**Concept used.** Recursive definition from [Chapter 5, Section 6](../../Lecture-Notes/Ch05_Sequences-Mathematical-Induction-and-Recursion/Concepts_Lecture.md). A **recurrence relation** expresses each term in terms of earlier terms, and the **initial conditions** fix the values of the first few terms before the recurrence relation is applied. This recurrence relation uses the two immediately preceding terms, so two initial conditions are needed.

**Solution.**

1. $v_1 = 1$ and $v_2 = 3$ are given by the initial conditions.
2. Substituting $k = 3$ into the recurrence relation gives $v_3 = v_2 + v_1 + 1 = 3 + 1 + 1 = 5$.
3. Substituting $k = 4$ into the recurrence relation gives $v_4 = v_3 + v_2 + 1 = 5 + 3 + 1 = 9$.

| $k$ | 1 | 2 | 3 | 4 |
|:-----|:-----:|:-----:|:-----:|:-----:|
| Reason | Initial condition | Initial condition | $v_2 + v_1 + 1$ | $v_3 + v_2 + 1$ |
| $v_k$ | 1 | 3 | 5 | 9 |

*Table 3. The first four terms obtained from the initial conditions and the recurrence relation*

**Answer.** The first four terms are $v_1 = 1$, $v_2 = 3$, $v_3 = 5$, and $v_4 = 9$.

> **Caution:** The recurrence relation applies only for $k \ge 3$. Substituting $k = 2$ would require $v_0$, which is not defined. The first two terms are determined by the initial conditions, not by the recurrence relation.

> **Note:** For the auxiliary sequence $w_k = v_k + 1$, obtained by adding 1 to each term, the recurrence relation becomes $w_k = v_{k-1} + v_{k-2} + 2 = w_{k-1} + w_{k-2}$, the same form as the Fibonacci sequence. Its initial conditions are $w_1 = 2$ and $w_2 = 4$. For the Fibonacci numbers of Chapter 5, $F_0 = F_1 = 1$ and $F_k = F_{k-1} + F_{k-2}$, the numbers $2F_n$ satisfy the same recurrence relation with $2F_1 = 2$ and $2F_2 = 4$, so by strong mathematical induction $w_n = 2F_n$ for every $n \ge 1$, that is, $v_n = 2F_n - 1$. Indeed $v_5 = 2 \cdot 8 - 1 = 15$ and $v_6 = 2 \cdot 13 - 1 = 25$, which agree with the values $v_5 = 9 + 5 + 1 = 15$ and $v_6 = 15 + 9 + 1 = 25$ computed directly from the recurrence relation.

---

<br>

## Summary

| Concept | Key Summary |
|:-----|:-----|
| Writing in summation notation | Write each term as a general term in the index, fix the lower and upper limits of the index, and multiply by $(-1)^k$ when the signs alternate. |
| Different expressions of the same sum | $\sum_{k=0}^{5} (-1)^k r^k$ equals $\sum_{k=0}^{5} (-r)^k$, and shifting the index does not change the sum. |
| Formula for a geometric sum | If $r \ne 1$, $\sum_{i=0}^{n} ar^{m+i} = ar^m \cdot \frac{r^{n+1} - 1}{r - 1}$, and if $r = 1$ the sum is $a(n + 1)$. |
| Number of terms | A sum whose exponents run from $m$ to $m + n$ has $n + 1$ terms. |
| Writing P(k) and P(k+1) | Replace every $n$ in $P(n)$ by $k$ and by the parenthesized $(k+1)$, and remember that $P(k)$ is a sentence, not a number. |
| Inductive step | It proves a conditional statement by supposing $P(k)$ for every integer $k$ at least the base value and deriving $P(k+1)$. |
| Power and factorial | Since $2^{k+1} = 2 \cdot 2^k < 2 \cdot (k+1)! < (k+2)!$, $2^n < (n+1)!$ for every integer $n \ge 2$. |
| Recursive definition | The initial conditions fix the first terms, and the recurrence relation is applied only for $k$ in its stated range to obtain the next terms in order. |
| Auxiliary sequence | Adding 1 to $v_k$ gives $w_k = v_k + 1$, which satisfies a Fibonacci-type recurrence relation, so $v_n = 2F_n - 1$. |

---

<br>

## Self-Check Questions

1. **Summation notation:** Express $1 + r^2 + r^4 + r^6$ in summation notation.

   <details>
   <summary>Answer</summary>

   The exponents 0, 2, 4, 6 increase by 2, so the term with index $k$ is $r^{2k}$ with $k$ running from 0 to 3. Hence the sum is $\sum_{k=0}^{3} r^{2k}$.

   </details>

2. **Alternating sum:** Express $-1 + 2 - 3 + 4 - 5$ in summation notation.

   <details>
   <summary>Answer</summary>

   The absolute values run from 1 to 5 and the odd-numbered terms are negative, so the term with index $k$ is $(-1)^k k$. Hence the sum is $\sum_{k=1}^{5} (-1)^k k$, which gives $-1$ for $k = 1$ and $2$ for $k = 2$, matching the original expression.

   </details>

3. **Geometric sum:** Compute $5 \cdot 2^3 + 5 \cdot 2^4 + \cdots + 5 \cdot 2^8$ with the formula of exercise 5.2.34.

   <details>
   <summary>Answer</summary>

   Here $a = 5$, $r = 2$, $m = 3$, and the last exponent is $m + n = 8$, so $n = 5$. The formula gives $5 \cdot 2^3 \cdot \frac{2^6 - 1}{2 - 1} = 40 \cdot 63 = 2520$, which matches the direct sum $40 + 80 + 160 + 320 + 640 + 1280 = 2520$.

   </details>

4. **The case r = 1:** Why must the case $r = 1$ be written separately in the answer to exercise 5.2.34?

   <details>
   <summary>Answer</summary>

   The formula of Theorem 5.2.2 has the denominator $r - 1$, so it is undefined for $r = 1$. For $r = 1$ every term equals $a$ and there are $n + 1$ terms, so the sum is $a(n + 1)$.

   </details>

5. **Setting up induction:** The goal is to prove by mathematical induction that $2^n < n!$ for every integer $n \ge 4$. Write $P(4)$, decide whether it is true, and state what must be shown in the inductive step.

   <details>
   <summary>Answer</summary>

   $P(4)$ is $2^4 < 4!$, that is, $16 < 24$, which is true. In the inductive step it must be shown that for every integer $k \ge 4$, if $2^k < k!$ then $2^{k+1} < (k+1)!$.

   </details>

6. **Completing the inductive step:** Prove the inductive step of question 5.

   <details>
   <summary>Answer</summary>

   Suppose $k \ge 4$ and $2^k < k!$. Then $2^{k+1} = 2 \cdot 2^k < 2 \cdot k! < (k+1) \cdot k! = (k+1)!$. The first inequality multiplies both sides of the inductive hypothesis by 2, the second holds because $k + 1 \ge 5 > 2$ and $k! > 0$, and the last equality is the definition of factorial.

   </details>

7. **Recursive definition:** Find the first four terms of the sequence with $u_k = 2u_{k-1} + 1$ for every integer $k \ge 2$ and $u_1 = 1$.

   <details>
   <summary>Answer</summary>

   $u_1 = 1$, $u_2 = 2 \cdot 1 + 1 = 3$, $u_3 = 2 \cdot 3 + 1 = 7$, and $u_4 = 2 \cdot 7 + 1 = 15$. Each term equals $2^k - 1$.

   </details>
