# HW4 Assignment Explanation — Divisibility, Floor and Ceiling, and Indirect Proof

[Repository Guide](../../README.md) | [English](Assignment-Explanation.md) | [한국어](Assignment-Explanation.ko.md)

> **Last Updated:** 2026-11-04
>
> Discrete Mathematics with Applications, Epp, Ch 4

> **Learning Objectives:**
> 1. Decide from the definition of divisibility whether an algebraic expression is divisible by a given integer, and prove properties of divisibility directly
> 2. Prove divisibility facts about the last digit by rewriting a decimal representation as an expression
> 3. Determine a remainder by using the uniqueness part of the quotient-remainder theorem
> 4. Compute values of floor and ceiling from their defining inequalities and prove their properties
> 5. Prove irrationality by contradiction, and explain the role that the remainders of a product of primes plus 1 play in the proof that there are infinitely many primes

---

## Table of Contents

- [1. Exercise 4.4.4: A Product of Three Consecutive Integers and 3](#1-exercise-444-a-product-of-three-consecutive-integers-and-3)
- [2. Exercise 4.4.15: Divisibility of a Sum](#2-exercise-4415-divisibility-of-a-sum)
- [3. Exercise 4.4.24: Divisibility of a Linear Combination](#3-exercise-4424-divisibility-of-a-linear-combination)
- [4. Exercise 4.4.44: Numbers Ending in 0 and Divisibility by 5](#4-exercise-4444-numbers-ending-in-0-and-divisibility-by-5)
- [5. Exercise 4.5.16: The Remainder When d Divides n](#5-exercise-4516-the-remainder-when-d-divides-n)
- [6. Exercise 4.6.7: The Ceiling of an Integer Plus One Half](#6-exercise-467-the-ceiling-of-an-integer-plus-one-half)
- [7. Exercise 4.6.13: The Floor of Half an Even Integer](#7-exercise-4613-the-floor-of-half-an-even-integer)
- [8. Exercise 4.8.6: Deciding Irrationality](#8-exercise-486-deciding-irrationality)
- [9. Exercise 4.8.28: Remainders of a Product of Primes Plus 1](#9-exercise-4828-remainders-of-a-product-of-primes-plus-1)
- [Summary](#summary)
- [Self-Check Questions](#self-check-questions)

---

<br>

## 1. Exercise 4.4.4: A Product of Three Consecutive Integers and 3

**Problem.** If $k$ is an integer, is $(3k+1)(3k+2)(3k+3)$ divisible by 3? Give the answer and a reason.

**Concept used.** The definition of divisibility from [Chapter 4, Section 4](../../Lecture-Notes/Ch04_Elementary-Number-Theory-and-Methods-of-Proof/Concepts_Lecture.md). For integers $n$ and $d$, $d \mid n$ means that there is an integer $m$ with $n = dm$ and $d \ne 0$. So to show that an expression is divisible by 3, rewrite it in the form $3 \times (\text{an integer})$ and explain why the multiplied quantity is an integer.

**Solution.** Observe that 3 can be factored out of the last factor $3k + 3$.

$$
\begin{aligned}
(3k+1)(3k+2)(3k+3) &= (3k+1)(3k+2) \cdot 3(k+1) && \text{(1)} \\
&= 3 \cdot \big[(3k+1)(3k+2)(k+1)\big] && \text{(2)}
\end{aligned}
$$

Step (1) writes $3k + 3 = 3(k+1)$ by the distributive law, and step (2) moves 3 to the front by the commutative and associative laws of multiplication. Now let $m = (3k+1)(3k+2)(k+1)$. Since $k$ is an integer and sums and products of integers are integers, $m$ is an integer. Hence $(3k+1)(3k+2)(3k+3) = 3m$ with $3 \ne 0$, and by the definition of divisibility 3 divides $(3k+1)(3k+2)(3k+3)$.

**Answer.** Yes. $(3k+1)(3k+2)(3k+3) = 3\big[(3k+1)(3k+2)(k+1)\big]$, and the quantity in brackets is an integer.

For example, $k = 1$ gives $4 \cdot 5 \cdot 6 = 120 = 3 \cdot 40$, and $k = -2$ gives $(-5)(-4)(-3) = -60 = 3 \cdot (-20)$. The definition allows negative integers, so the conclusion holds even when the product is negative.

> **Caution:** Do not name the integer in the definition with the same letter as a variable of the problem. Writing $(3k+1)(3k+2)(3k+3) = 3k$ mixes it up with the $k$ already in use and produces an entirely different equation. When applying the definition, use a new letter ($m$ here).

> **Note:** $3k + 1$, $3k + 2$, and $3k + 3$ are three consecutive integers. Splitting the integers into the forms $3q$, $3q + 1$, and $3q + 2$ by the quotient-remainder theorem shows that one of any three consecutive integers is a multiple of 3, so the product of three consecutive integers is always divisible by 3. In this problem that multiple appears openly as $3k + 3$.

---

<br>

## 2. Exercise 4.4.15: Divisibility of a Sum

**Problem.** Using only the definition of divisibility, show that an integer $a$ that divides both integers $b$ and $c$ also divides $b + c$.

**Concept used.** The definition of divisibility and direct proof. The statement is a universal conditional statement of the form "for all integers $a, b, c$, if $a \mid b$ and $a \mid c$ then $a \mid (b + c)$". So, following the method of generalizing from the generic particular in [Chapter 4, Section 1](../../Lecture-Notes/Ch04_Elementary-Number-Theory-and-Methods-of-Proof/Concepts_Lecture.md), start from particular but arbitrarily chosen integers that satisfy the hypothesis and derive the conclusion.

**Proof.**

1. Suppose $a, b, c$ are particular but arbitrarily chosen integers such that $a \mid b$ and $a \mid c$. [It must be shown that $a \mid (b + c)$.]
2. Since $a \mid b$, by the definition of divisibility there is an integer $r$ with $b = ar$, and $a \ne 0$.
3. Since $a \mid c$, by the same definition there is an integer $s$ with $c = as$.
4. Substituting the equations of steps 2 and 3 gives $b + c = ar + as = a(r + s)$. The last equality is the distributive law.
5. Let $t = r + s$. Since $r$ and $s$ are integers and a sum of two integers is an integer, $t$ is an integer.
6. Hence $b + c = at$ with $a \ne 0$, so by the definition of divisibility $a \mid (b + c)$. [This is what was to be shown.]

For example, if $a = 3$, $b = 6$, and $c = 9$, then $r = 2$, $s = 3$, and $b + c = 15 = 3 \cdot 5$, where indeed $t = r + s = 5$.

> **Caution:** Do not use the same letter for the two integers in steps 2 and 3. Writing $b = ak$ and $c = ak$ adds the condition $b = c$, which is not in the hypothesis, and the proof then fails to cover the cases with $b \ne c$. Integers obtained from different existential statements need different letters.

> **Note:** The same method proves that if $a \mid b$ and $a \mid c$ then $a \mid (b - c)$ (exercise 4.4.16), because $b - c = ar - as = a(r - s)$. This property of sums is also used to prove the test that a number whose digit sum is divisible by 9 is itself divisible by 9 (exercise 4.4.47).

---

<br>

## 3. Exercise 4.4.24: Divisibility of a Linear Combination

**Problem.** Decide whether the statement "for all integers $a, b, c$, if $a \mid b$ and $a \mid c$ then $a \mid (2b - 3c)$" is true; if it is, give a direct proof from the definitions, and if not, give a counterexample.

**Concept used.** The definition of divisibility and direct proof. When the truth value is unknown, test small examples first. With $a = 4$, $b = 8$, $c = 12$, $2b - 3c = 16 - 36 = -20 = 4 \cdot (-5)$, which is divisible by 4. Examples are not a proof, but when the statement holds in several examples it is likely to be true, so attempt a proof.

**Proof.**

1. Suppose $a, b, c$ are particular but arbitrarily chosen integers such that $a \mid b$ and $a \mid c$. [It must be shown that $a \mid (2b - 3c)$.]
2. By the definition of divisibility there are integers $r, s$ with $b = ar$ and $c = as$, and $a \ne 0$.
3. Substitution gives $2b - 3c = 2(ar) - 3(as) = a(2r - 3s)$, by the associative and commutative laws of multiplication and the distributive law.
4. Let $t = 2r - 3s$. Products and differences of integers are integers, so $t$ is an integer.
5. Hence $2b - 3c = at$ with $a \ne 0$, so by the definition of divisibility $a \mid (2b - 3c)$.

**Answer.** True.

In the earlier example $r = 2$ and $s = 3$, so $t = 2 \cdot 2 - 3 \cdot 3 = -5$, and indeed $2b - 3c = -20 = 4 \cdot (-5)$. The value $2b - 3c$ may be negative, which causes no problem because the definition also allows divisibility of negative integers.

> **Note:** The coefficients 2 and $-3$ play no special role in the proof. The same argument shows that for all integers $x, y$, if $a \mid b$ and $a \mid c$ then $a \mid (xb + yc)$. An expression of the form $xb + yc$ is called a **linear combination** of $b$ and $c$, and this property is a basic tool in the study of greatest common divisors and the Euclidean algorithm.

---

<br>

## 4. Exercise 4.4.44: Numbers Ending in 0 and Divisibility by 5

**Problem.** Show that a nonnegative integer $n$ whose decimal representation has last digit 0 is divisible by 5 ($5 \mid n$). The hint is that a nonnegative integer $n$ with last digit $d_0$ can be written as $n = 10m + d_0$ for some integer $m$.

**Concept used.** The definitions of decimal representation and of divisibility.

> **Definition:** The **decimal representation** of a nonnegative integer $n$ is an expression of the form $d_k d_{k-1} \cdots d_1 d_0$. Here $k$ is a nonnegative integer, the **decimal digits** $d_0, d_1, \ldots, d_k$ are integers from 0 to 9 inclusive, $d_k \ne 0$ unless $n = 0$ and $k = 0$, and $n = d_k \cdot 10^k + d_{k-1} \cdot 10^{k-1} + \cdots + d_1 \cdot 10 + d_0$.

For example, $2{,}530 = 2 \cdot 10^3 + 5 \cdot 10^2 + 3 \cdot 10 + 0$. The equation in the hint is obtained by factoring 10 out of all terms except the last term $d_0$.

$$
n = 10\big(d_k \cdot 10^{k-1} + \cdots + d_2 \cdot 10 + d_1\big) + d_0 = 10m + d_0
$$

The quantity $m$ in parentheses is a sum of products of integers, so it is an integer. If $k = 0$, the parentheses contain no terms and $m = 0$.

**Proof.**

1. Suppose $n$ is a particular but arbitrarily chosen nonnegative integer whose decimal representation ends in 0. [It must be shown that $5 \mid n$.]
2. By the hint there is an integer $m$ with $n = 10m + d_0$, and since the last digit is 0, $d_0 = 0$. Hence $n = 10m$.
3. By the associative law of multiplication, $10m = (5 \cdot 2)m = 5 \cdot (2m)$.
4. $2m$ is a product of integers, so it is an integer.
5. Hence $n = 5 \cdot (2m)$ with $5 \ne 0$, so by the definition of divisibility $5 \mid n$.

For example, $2{,}530 = 10 \cdot 253 = 5 \cdot 506$.

> **Note:** Showing from $n = 10m$ that $n/5 = 2m$ is an integer leads to the same conclusion, because for $d \ne 0$, $d \mid n$ is equivalent to $n/d$ being an integer. Since the definition is stated as a product, however, writing $n = 5 \cdot (\text{an integer})$ is the proof that applies the definition as it stands.

> **Note:** The case of last digit 5 is the same: $n = 10m + 5 = 5(2m + 1)$, so $5 \mid n$ (exercise 4.4.45). Conversely, if $5 \mid n$, then since $5 \mid 10m$, the difference property of exercise 4.4.16 shows that $d_0 = n - 10m$ is divisible by 5, and since $0 \le d_0 \le 9$, $d_0$ is 0 or 5. Therefore a nonnegative integer is divisible by 5 if, and only if, its last digit is 0 or 5.

---

<br>

## 5. Exercise 4.5.16: The Remainder When d Divides n

**Problem.** For a positive integer $d$ and an integer $n$ with $d \mid n$, find the remainder that the quotient-remainder theorem gives when $n$ is divided by $d$.

**Concept used.** The quotient-remainder theorem (Theorem 4.5.1) from [Chapter 4, Section 5](../../Lecture-Notes/Ch04_Elementary-Number-Theory-and-Methods-of-Proof/Concepts_Lecture.md). For any integer $n$ and positive integer $d$ there exist **unique** integers $q$ and $r$ with $n = dq + r$ and $0 \le r < d$; this $q$ is called the quotient ($n$ div $d$) and $r$ the remainder ($n$ mod $d$).

**Solution.**

1. Since $d \mid n$, by the definition of divisibility there is an integer $k$ with $n = dk$.
2. This equation can be written as $n = dk + 0$, so $q = k$ and $r = 0$ satisfy the equation $n = dq + r$.
3. Since $d$ is positive, $0 \le 0 < d$. Hence $r = 0$ also satisfies the remainder condition $0 \le r < d$.
4. By the quotient-remainder theorem only one pair of integers $(q, r)$ satisfies both conditions, so the pair $(k, 0)$ found in steps 2 and 3 is that pair.

**Answer.** The remainder is 0. That is, if $d \mid n$ then $n$ mod $d = 0$.

For example, for $n = 42$ and $d = 7$, $42 = 7 \cdot 6 + 0$; for $n = -12$ and $d = 4$, $-12 = 4 \cdot (-3) + 0$, so the remainder is 0 even when $n$ is negative.

> **Caution:** The uniqueness in step 4 is what determines the answer. The equation $n = dq + r$ alone is satisfied by other pairs as well, as in $12 = 4 \cdot 2 + 4$, but such a pair fails $r < d$. The quotient-remainder theorem guarantees that exactly one pair also satisfies $0 \le r < d$, so once a pair meeting all the conditions is found, it is the unique quotient and remainder.

> **Note:** Uniqueness can be shown as follows. Suppose $n = dq_1 + r_1 = dq_2 + r_2$ with $0 \le r_1 < d$ and $0 \le r_2 < d$. Then $r_2 - r_1 = d(q_1 - q_2)$, so $r_2 - r_1$ is a multiple of $d$. But the two inequalities give $-d < r_2 - r_1 < d$, and the only multiple of $d$ in this range is 0, so $r_1 = r_2$, and since $d \ne 0$, $q_1 = q_2$.

> **Key Point:** For a positive integer $d$ and an integer $n$, $d \mid n$ and $n$ mod $d = 0$ are equivalent. This exercise shows the forward direction, and the converse holds because $n$ mod $d = 0$ gives $n = dq$, so $d \mid n$ by definition.

---

<br>

## 6. Exercise 4.6.7: The Ceiling of an Integer Plus One Half

**Problem.** For an integer $k$, find $\lceil k + \frac{1}{2} \rceil$ and justify the answer.

**Concept used.** The definition of ceiling from [Chapter 4, Section 6](../../Lecture-Notes/Ch04_Elementary-Number-Theory-and-Methods-of-Proof/Concepts_Lecture.md). For a real number $x$ and an integer $n$, $\lceil x \rceil = n \iff n - 1 < x \le n$, so the ceiling is the smallest integer greater than or equal to $x$. Only one integer satisfies this inequality, so showing that some integer satisfies it identifies the ceiling.

**Solution.**

1. The smallest integer greater than or equal to $k + \frac{1}{2}$ appears to be $k + 1$, so take $n = k + 1$ as the candidate. Since $k$ is an integer, so is $n$.
2. Substituting $n = k + 1$ and $x = k + \frac{1}{2}$ into the defining inequality $n - 1 < x \le n$ gives $k < k + \frac{1}{2} \le k + 1$.
3. Subtracting $k$ from every part of this inequality gives $0 < \frac{1}{2} \le 1$, so the inequality in step 2 is true.
4. Therefore, by the definition of ceiling, $\lceil k + \frac{1}{2} \rceil = k + 1$.

```text
          k             k + 1/2            k + 1
   ───────●────────────────●─────────────────●───────▶
          └ ⌊k + 1/2⌋ = k                    └ ⌈k + 1/2⌉ = k + 1
```

*Figure 1. The floor and ceiling of k + 1/2, which lies between the consecutive integers k and k + 1*

**Answer.** $\lceil k + \frac{1}{2} \rceil = k + 1$, because $k + 1$ is an integer and $(k + 1) - 1 < k + \frac{1}{2} \le k + 1$.

For example, $k = 3$ gives $\lceil 3.5 \rceil = 4$.

> **Caution:** Negative integers give the same answer. For $k = -2$, $k + \frac{1}{2} = -1.5$, and since $-2 < -1.5 \le -1$, $\lceil -1.5 \rceil = -1 = k + 1$. Misreading the ceiling as rounding away from 0 gives the wrong answer $-2$. The ceiling is always the integer on the right (larger) side on the number line.

> **Note:** For comparison, $\lfloor k + \frac{1}{2} \rfloor = k$ (Example 4.6.3). In general, if $x$ is not an integer then $\lfloor x \rfloor$ and $\lceil x \rceil$ are consecutive integers with $\lceil x \rceil = \lfloor x \rfloor + 1$, and if $x$ is an integer then $\lfloor x \rfloor = \lceil x \rceil = x$.

---

<br>

## 7. Exercise 4.6.13: The Floor of Half an Even Integer

**Problem.** Show that $\lfloor n/2 \rfloor = n/2$ for every even integer $n$.

**Concept used.** The definition of even ($n = 2m$ for some integer $m$) and the definition of floor (for a real number $x$ and an integer $n$, $\lfloor x \rfloor = n \iff n \le x < n + 1$).

**Proof.**

1. Suppose $n$ is a particular but arbitrarily chosen even integer. [It must be shown that $\lfloor n/2 \rfloor = n/2$.]
2. By the definition of even, there is an integer $m$ with $n = 2m$.
3. Hence $n/2 = 2m/2 = m$.
4. $m$ is an integer and $m \le m < m + 1$, so by the definition of floor, $\lfloor m \rfloor = m$.
5. Combining steps 3 and 4 gives $\lfloor n/2 \rfloor = \lfloor m \rfloor = m = n/2$. [This is what was to be shown.]

For example, $n = 10$ gives $\lfloor 5 \rfloor = 5 = 10/2$, and $n = -6$ gives $\lfloor -3 \rfloor = -3 = -6/2$.

> **Note:** This result is the even case of Theorem 4.6.2 (the floor of $n/2$). For an odd integer $n = 2m + 1$, $n/2 = m + \frac{1}{2}$ and $m \le m + \frac{1}{2} < m + 1$, so $\lfloor n/2 \rfloor = m = \frac{n - 1}{2}$. These two formulas are used in analyzing algorithms that halve an interval, such as binary search and merge sort.

---

<br>

## 8. Exercise 4.8.6: Deciding Irrationality

**Problem.** Determine whether $6 - 7\sqrt{2}$ is irrational, and support the answer with a proof or a disproof.

**Concept used.** A real number $r$ is a **rational number** if $r = a/b$ for some integers $a, b$ with $b \ne 0$, and a real number that is not rational is an **irrational number**. By Theorem 4.8.1 in [Chapter 4, Section 8](../../Lecture-Notes/Ch04_Elementary-Number-Theory-and-Methods-of-Proof/Concepts_Lecture.md), $\sqrt{2}$ is irrational. Being irrational is the negative statement "not rational", so proof by contradiction, which supposes the negation of the conclusion and derives a contradiction, is the natural method. It is the same method as the proof of Proposition 4.8.2 (the irrationality of $1 + 3\sqrt{2}$).

**Answer.** It is irrational.

**Proof (by contradiction).**

1. Suppose not. That is, suppose $6 - 7\sqrt{2}$ is rational. [A contradiction must be derived.]
2. By the definition of rational, there are integers $a, b$ with $6 - 7\sqrt{2} = \frac{a}{b}$ and $b \ne 0$.
3. Solve this equation for $\sqrt{2}$.

$$
\begin{aligned}
7\sqrt{2} &= 6 - \frac{a}{b} = \frac{6b - a}{b} && \text{(1)} \\
\sqrt{2} &= \frac{6b - a}{7b} && \text{(2)}
\end{aligned}
$$

Step (1) adds $7\sqrt{2} - \frac{a}{b}$ to both sides of the equation in step 2 and uses a common denominator, and step (2) divides both sides by 7.

4. $6b - a$ is an integer because it is a difference of products of integers, and $7b$ is an integer because it is a product of integers. Moreover $7 \ne 0$ and $b \ne 0$, and a product of two nonzero numbers is nonzero, so $7b \ne 0$.
5. Hence (2) expresses $\sqrt{2}$ as a quotient of two integers with a nonzero denominator, so by the definition of rational, $\sqrt{2}$ is rational.
6. This contradicts Theorem 4.8.1, which states that $\sqrt{2}$ is irrational. Hence the supposition of step 1 is false, and $6 - 7\sqrt{2}$ is irrational.

> **Caution:** Obtaining $6 - 7\sqrt{2} \approx -3.8994949\ldots$ on a calculator does not prove irrationality. Every terminating decimal shown on a display is rational, and irrationality depends on the infinite property that the decimal expansion neither terminates nor repeats, which no finite number of digits can decide.

> **Note:** The same argument shows that if $p$ and $q$ are rational and $q \ne 0$, then $p + q\sqrt{2}$ is irrational. If $p + q\sqrt{2}$ were a rational number $s$, then since differences of rationals and quotients by nonzero rationals are rational, $\sqrt{2} = (s - p)/q$ would be rational. This exercise is the case $p = 6$, $q = -7$. If $q = 0$, then $p + q\sqrt{2} = p$ is rational, so the condition $q \ne 0$ cannot be dropped.

---

<br>

## 9. Exercise 4.8.28: Remainders of a Product of Primes Plus 1

**Problem.** For $N = 2 \cdot 3 \cdot 5 \cdot 7 + 1$, find the remainders of $N$ on division by 2, 3, 5, and 7, with justification.

**Concept used.** The uniqueness part of the quotient-remainder theorem (the same reasoning as in Section 5) and Proposition 4.8.3 of [Chapter 4, Section 8](../../Lecture-Notes/Ch04_Elementary-Number-Theory-and-Methods-of-Proof/Concepts_Lecture.md) (for any integer $a$ and any prime $p$, if $p \mid a$ then $p \nmid (a + 1)$). $N$ has the same form as the number in the proof that the primes are infinite (Theorem 4.8.4).

**Solution.** First, $N = 210 + 1 = 211$. Starting with the divisor 2, factor 2 out of $N$ to write $N = 2 \cdot (3 \cdot 5 \cdot 7) + 1 = 2 \cdot 105 + 1$. Since 105 is an integer and $0 \le 1 < 2$, this equation has the form of the quotient-remainder theorem, and by uniqueness the quotient is 105 and the remainder is 1. For the other three primes, factor out that prime in the same way.

| Divisor $p$ | Factored equation | Quotient | Remainder |
|:-----|:-----|:-----|:-----|
| 2 | $N = 2 \cdot (3 \cdot 5 \cdot 7) + 1 = 2 \cdot 105 + 1$ | 105 | 1 |
| 3 | $N = 3 \cdot (2 \cdot 5 \cdot 7) + 1 = 3 \cdot 70 + 1$ | 70 | 1 |
| 5 | $N = 5 \cdot (2 \cdot 3 \cdot 7) + 1 = 5 \cdot 42 + 1$ | 42 | 1 |
| 7 | $N = 7 \cdot (2 \cdot 3 \cdot 5) + 1 = 7 \cdot 30 + 1$ | 30 | 1 |

*Table 1. Quotients and remainders of N = 211 divided by 2, 3, 5, and 7*

In all four cases $p > 1$, so $0 \le 1 < p$ holds, and each equation is therefore the unique form given by the quotient-remainder theorem.

**Answer.** The remainder is 1 for each of 2, 3, 5, and 7.

> **Note:** The remainder can also be found without guessing it first. Write $N = 3q + r$ with $0 \le r < 3$. Then $r - 1 = (N - 1) - 3q = 3(2 \cdot 5 \cdot 7) - 3q = 3(70 - q)$, so $3 \mid (r - 1)$. The only multiple of 3 in the range $-1 \le r - 1 < 2$ is 0, so $r = 1$. The divisors 2, 5, and 7 are handled the same way.

> **Key Point:** This computation is the heart of the proof of Theorem 4.8.4 (the infinitude of the primes). If 2, 3, 5, and 7 were the only primes, then $N$, being an integer greater than 1, would be divisible by some prime by Theorem 4.4.4. But as Table 1 shows, division by any of these primes leaves remainder 1, which is a contradiction.

> **Caution:** This way of building $N$ does not always produce a prime. 211 is prime because none of the primes 2, 3, 5, 7, 11, 13 up to $\sqrt{211} \approx 14.5$ divides it, but $2 \cdot 3 \cdot 5 \cdot 7 \cdot 11 \cdot 13 + 1 = 30031 = 59 \cdot 509$ is composite. The proof of Theorem 4.8.4 guarantees only that $N$ is divisible by a prime that is not on the list.

---

<br>

## Summary

| Concept | Key Summary |
|:-----|:-----|
| Divisibility | $d \mid n$ means that $n = dk$ for some integer $k$ and $d \ne 0$; to show it, write the expression as $d \times (\text{an integer})$ and explain why the multiplied quantity is an integer. |
| Sums and linear combinations | If $a \mid b$ and $a \mid c$, then $a \mid (xb + yc)$ for all integers $x, y$, and $b + c$ and $2b - 3c$ are special cases. |
| Distinct letters | Using the same letter for integers obtained from different hypotheses adds a condition that is not in the hypothesis, so use distinct letters. |
| Decimal representation and 5 | Since $n = 10m + d_0$, a nonnegative integer is divisible by 5 if, and only if, its last digit is 0 or 5. |
| Uniqueness in the quotient-remainder theorem | Once one form $n = dq + r$ with $0 \le r < d$ is found, it gives the unique quotient and remainder, and if $d \mid n$ the remainder is 0. |
| Ceiling | For an integer $k$, $\lceil k + \frac{1}{2} \rceil = k + 1$ and $\lfloor k + \frac{1}{2} \rfloor = k$. |
| Floor of a half | If $n$ is even, $\lfloor n/2 \rfloor = n/2$, and if $n$ is odd, $\lfloor n/2 \rfloor = (n - 1)/2$. |
| Proving irrationality | Suppose the number is rational, express $\sqrt{2}$ as a quotient of two integers with a nonzero denominator, and derive a contradiction with Theorem 4.8.1. |
| A product of primes plus 1 | $N = p_1 p_2 \cdots p_k + 1$ leaves remainder 1 when divided by each $p_i$, which is the heart of the proof that the primes are infinite. |

---

<br>

## Self-Check Questions

1. **Deciding divisibility:** If $k$ is an integer, is $(4k+1)(4k+2)(4k+3)(4k+4)$ divisible by 4? Give a reason.

   <details>
   <summary>Answer</summary>

   Yes. Since $4k + 4 = 4(k + 1)$, the product equals $4 \cdot \big[(4k+1)(4k+2)(4k+3)(k+1)\big]$. The quantity in brackets is an integer because it is built from sums and products of integers, and $4 \ne 0$, so by the definition of divisibility 4 divides the product.

   </details>

2. **Linear combination:** Prove that for all integers $a, b, c$, if $a \mid b$ and $a \mid c$ then $a \mid (5b + 7c)$.

   <details>
   <summary>Answer</summary>

   Suppose $a, b, c$ are any integers with $a \mid b$ and $a \mid c$. By definition there are integers $r, s$ with $b = ar$ and $c = as$, and $a \ne 0$. Then $5b + 7c = 5ar + 7as = a(5r + 7s)$, and $5r + 7s$ is an integer because it is a sum of products of integers. Hence $a \mid (5b + 7c)$.

   </details>

3. **Counterexample:** Is the statement "for all integers $a, b, c$, if $a \mid (b + c)$ then $a \mid b$ or $a \mid c$" true?

   <details>
   <summary>Answer</summary>

   It is false. With $a = 2$, $b = 1$, $c = 1$, $b + c = 2 = 2 \cdot 1$, so $2 \mid (b + c)$, but since $1/2$ is not an integer, $2 \nmid b$ and $2 \nmid c$. A sum being divisible does not make each term divisible.

   </details>

4. **Remainders:** For an integer $n$, if $n$ mod $6 = 0$, what is $n$ mod 3?

   <details>
   <summary>Answer</summary>

   It is 0. If $n$ mod $6 = 0$, then $n = 6k$ for some integer $k$, so $n = 3(2k) + 0$. Since $2k$ is an integer and $0 \le 0 < 3$, the uniqueness part of the quotient-remainder theorem shows that the remainder of $n$ divided by 3 is 0.

   </details>

5. **Ceiling and floor:** For an integer $k$, find $\lceil k - \frac{1}{2} \rceil$ and $\lfloor k - \frac{1}{2} \rfloor$.

   <details>
   <summary>Answer</summary>

   Since $k - 1 < k - \frac{1}{2} \le k$, the definition of ceiling gives $\lceil k - \frac{1}{2} \rceil = k$. Since $k - 1 \le k - \frac{1}{2} < (k - 1) + 1$, the definition of floor gives $\lfloor k - \frac{1}{2} \rfloor = k - 1$.

   </details>

6. **Irrationality:** Prove that $3 + 5\sqrt{2}$ is irrational.

   <details>
   <summary>Answer</summary>

   Suppose $3 + 5\sqrt{2}$ is rational. Then $3 + 5\sqrt{2} = a/b$ for some integers $a, b$ with $b \ne 0$. Rearranging gives $\sqrt{2} = (a - 3b)/(5b)$. Since $a - 3b$ and $5b$ are integers and $5b \ne 0$, $\sqrt{2}$ would be rational, contradicting Theorem 4.8.1. Hence $3 + 5\sqrt{2}$ is irrational.

   </details>

7. **A product of primes plus 1:** Find the remainders of $M = 2 \cdot 3 \cdot 5 + 1$ divided by 2, 3, and 5, and decide whether $M$ is prime.

   <details>
   <summary>Answer</summary>

   $M = 31 = 2 \cdot 15 + 1 = 3 \cdot 10 + 1 = 5 \cdot 6 + 1$, so every remainder is 1. The only primes up to $\sqrt{31} \approx 5.6$ are 2, 3, and 5, and none of them divides 31, so 31 is prime.

   </details>
