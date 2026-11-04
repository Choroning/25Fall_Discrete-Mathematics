# HW2 Assignment Explanation — Number Systems and Quantified Statements

[Repository Guide](../../README.md) | [English](Assignment-Explanation.md) | [한국어](Assignment-Explanation.ko.md)

> **Last Updated:** 2026-11-04
>
> Discrete Mathematics with Applications, Epp, Ch 2, 3

> **Learning Objectives:**
> 1. Convert integers among decimal, binary, and hexadecimal notation
> 2. Add in binary notation, and find the integer represented by an 8-bit two's complement
> 3. Determine the truth values of predicates and quantified statements, and disprove a universal statement by a counterexample
> 4. Translate statements written in everyday language into formal statements with quantifiers and predicate symbols
> 5. Write negations of universal statements and universal conditional statements
> 6. Rewrite statements expressed with necessary and sufficient conditions in the form of conditional statements

---

## Table of Contents

- [1. Exercise 2.5.2: Decimal Integer to Binary Notation](#1-exercise-252-decimal-integer-to-binary-notation)
- [2. Exercise 2.5.8: Binary to Decimal Notation](#2-exercise-258-binary-to-decimal-notation)
- [3. Exercise 2.5.15: Binary Addition](#3-exercise-2515-binary-addition)
- [4. Exercise 2.5.27: Reading an 8-Bit Two's Complement](#4-exercise-2527-reading-an-8-bit-twos-complement)
- [5. Exercise 2.5.44: Binary to Hexadecimal Notation](#5-exercise-2544-binary-to-hexadecimal-notation)
- [6. Exercise 3.1.2: Truth of Statements about Numbers](#6-exercise-312-truth-of-statements-about-numbers)
- [7. Exercise 3.1.4: Values That Make a Predicate False](#7-exercise-314-values-that-make-a-predicate-false)
- [8. Exercise 3.1.12: Disproving a Universal Statement by Counterexample](#8-exercise-3112-disproving-a-universal-statement-by-counterexample)
- [9. Exercise 3.1.17: The Form of Existential Statements](#9-exercise-3117-the-form-of-existential-statements)
- [10. Exercise 3.1.26: Combining Universal and Existential Statements](#10-exercise-3126-combining-universal-and-existential-statements)
- [11. Exercise 3.2.2: Negation of a Universal Statement](#11-exercise-322-negation-of-a-universal-statement)
- [12. Exercise 3.2.9: Negation of a Universal Conditional I](#12-exercise-329-negation-of-a-universal-conditional-i)
- [13. Exercise 3.2.10: Negation of a Universal Conditional II](#13-exercise-3210-negation-of-a-universal-conditional-ii)
- [14. Exercise 3.2.40: Sufficient Condition](#14-exercise-3240-sufficient-condition)
- [15. Exercise 3.2.41: Necessary Condition](#15-exercise-3241-necessary-condition)
- [Summary](#summary)
- [Self-Check Questions](#self-check-questions)

---

<br>

## 1. Exercise 2.5.2: Decimal Integer to Binary Notation

**Problem.** Represent the decimal integer 55 in binary notation.

**Concepts used.** **Binary notation** writes an integer as a sum of powers of 2 and lists the coefficient (0 or 1) of each power from the highest place down ([Chapter 2, Section 5](../../Lecture-Notes/Ch02_The-Logic-of-Compound-Statements/Concepts_Lecture.md)). To convert a decimal integer to binary notation, either subtract powers of 2 starting from the largest one that does not exceed the number, or divide by 2 repeatedly and read the remainders in reverse order. To indicate binary notation, attach the subscript 2 as in $110_2$.

**Solution.** The powers of 2 are $1, 2, 4, 8, 16, 32, 64, \ldots$, and $2^5 = 32 \le 55 < 64 = 2^6$, so 55 starts at the $2^5$ place. Subtract, in turn, each power that does not exceed the remaining number.

1. $55 - 32 = 23$, so the $2^5$ place is 1.
2. $23 - 16 = 7$, so the $2^4$ place is 1.
3. $8 > 7$, so the $2^3$ place is 0.
4. $7 - 4 = 3$, so the $2^2$ place is 1.
5. $3 - 2 = 1$, so the $2^1$ place is 1.
6. $1 - 1 = 0$, so the $2^0$ place is 1, and the process ends because the remainder is 0.

| Place | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
|:-----|:---:|:---:|:---:|:---:|:---:|:---:|
| Place value | 32 | 16 | 8 | 4 | 2 | 1 |
| Coefficient | 1 | 1 | 0 | 1 | 1 | 1 |

*Table 1. Coefficients of 55 written in powers of 2*

Therefore $55 = 1 \cdot 2^5 + 1 \cdot 2^4 + 0 \cdot 2^3 + 1 \cdot 2^2 + 1 \cdot 2^1 + 1 \cdot 2^0$, and $55_{10} = 110111_2$.

The same result is obtained by repeated division by 2. Divide until the quotient becomes 0, and read the remainders in reverse order, starting from the last one.

| Division | Quotient | Remainder |
|:-----|:---:|:---:|
| $55 = 2 \cdot 27 + 1$ | 27 | 1 |
| $27 = 2 \cdot 13 + 1$ | 13 | 1 |
| $13 = 2 \cdot 6 + 1$ | 6 | 1 |
| $6 = 2 \cdot 3 + 0$ | 3 | 0 |
| $3 = 2 \cdot 1 + 1$ | 1 | 1 |
| $1 = 2 \cdot 0 + 1$ | 0 | 1 |

*Table 2. Quotients and remainders of repeated division of 55 by 2*

Reading the remainders from bottom to top gives 110111, the same as before. The remainders are read in reverse because the remainder of the first division is the coefficient of the $2^0$ place and each further division moves up one place.

---

<br>

## 2. Exercise 2.5.8: Binary to Decimal Notation

**Problem.** Represent $10111_2$ in decimal notation.

**Concepts used.** From the right, the places of binary notation have the place values $2^0, 2^1, 2^2, \ldots$. Multiplying each digit by its place value and adding the products gives the value in decimal notation (Chapter 2, Section 5).

**Solution.** $10111_2$ has five places, so from the left the place values are $2^4, 2^3, 2^2, 2^1, 2^0$.

```math
10111_2 = 1 \cdot 2^4 + 0 \cdot 2^3 + 1 \cdot 2^2 + 1 \cdot 2^1 + 1 \cdot 2^0 = 16 + 0 + 4 + 2 + 1 = 23
```

Therefore $10111_2 = 23_{10}$. Converting 23 back to binary notation by the method of Exercise 2.5.2 gives $23 = 16 + 4 + 2 + 1$, that is, $10111_2$ again.

---

<br>

## 3. Exercise 2.5.15: Binary Addition

**Problem.** Compute $101101_2 + 11101_2$ in binary notation.

**Concepts used.** Binary addition works like decimal addition: add from the rightmost place, and carry to the next place whenever the sum in a place is 2 or more (Chapter 2, Section 5). The possible sums in a single place are the following.

- $0 + 0 = 0$ and $0 + 1 = 1 + 0 = 1$, with no carry.
- $1 + 1 = 10_2$, so write 0 in that place and carry 1.
- If the sum including a carry is $1 + 1 + 1 = 11_2$, write 1 in that place and carry 1.

**Solution.** Align the two numbers at the right end and compute from the rightmost place. The second number has five places, so its $2^5$ place is regarded as 0.

1. Place $2^0$: $1 + 1 = 10_2$, so write 0 and carry 1.
2. Place $2^1$: $0 + 0 + 1 = 1$, so write 1 with no carry.
3. Place $2^2$: $1 + 1 = 10_2$, so write 0 and carry 1.
4. Place $2^3$: $1 + 1 + 1 = 11_2$, so write 1 and carry 1.
5. Place $2^4$: $0 + 1 + 1 = 10_2$, so write 0 and carry 1.
6. Place $2^5$: $1 + 0 + 1 = 10_2$, so write 0 and carry 1.
7. Place $2^6$: no digits remain except the carry 1, so write 1.

| | $2^6$ | $2^5$ | $2^4$ | $2^3$ | $2^2$ | $2^1$ | $2^0$ |
|:-----|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Carry | 1 | 1 | 1 | 1 | | 1 | |
| First number | | 1 | 0 | 1 | 1 | 0 | 1 |
| Second number | | | 1 | 1 | 1 | 0 | 1 |
| Sum | 1 | 0 | 0 | 1 | 0 | 1 | 0 |

*Table 3. $`101101_2 + 11101_2`$: place-by-place computation*

Therefore $101101_2 + 11101_2 = 1001010_2$. In decimal notation, $101101_2 = 32 + 8 + 4 + 1 = 45$ and $11101_2 = 16 + 8 + 4 + 1 = 29$, so $45 + 29 = 74$, and $1001010_2 = 64 + 8 + 2 = 74$ confirms the result.

---

<br>

## 4. Exercise 2.5.27: Reading an 8-Bit Two's Complement

**Problem.** Find the decimal representation of the integer whose 8-bit **two's complement** is $11010011$.

**Concepts used.** For an integer $a$ with $-128 \le a \le 127$, the 8-bit two's complement is defined as follows (Chapter 2, Section 5).

- If $a \ge 0$, it is the 8-bit binary representation of $a$ itself.
- If $a < 0$, it is the 8-bit binary representation of $2^8 - \lvert a \rvert$.

If $0 \le a \le 127$, the leftmost bit is 0; if $a < 0$, then $2^8 - \lvert a \rvert \ge 128$, so the leftmost bit is 1. Thus the leftmost bit tells the sign. Given a two's complement whose leftmost bit is 1, flip all the bits (0 to 1 and 1 to 0) and add 1 to obtain $\lvert a \rvert$.

**Solution.**

1. The leftmost bit is 1, so the integer is negative.
2. Flipping all the bits gives $11010011 \to 00101100$.
3. Adding 1 gives $00101100 + 1 = 00101101$.
4. $00101101_2 = 32 + 8 + 4 + 1 = 45$, so $\lvert a \rvert = 45$.

Therefore the integer is $-45$. Checking with the definition directly, $2^8 - 45 = 256 - 45 = 211$, and $211 = 128 + 64 + 16 + 2 + 1 = 11010011_2$, which matches the given two's complement.

> **Note:** The method of flipping the bits and adding 1 works for the following reason. Flipping all the bits of an 8-bit number $x$ gives $11111111_2 - x = 255 - x$, and adding 1 gives $256 - x$. If $x = 2^8 - \lvert a \rvert$, then $256 - x = \lvert a \rvert$, so the procedure returns the absolute value.

---

<br>

## 5. Exercise 2.5.44: Binary to Hexadecimal Notation

**Problem.** Represent $00101110_2$ in hexadecimal notation.

**Concepts used.** **Hexadecimal notation** uses powers of 16 as place values and sixteen symbols: the digits 0 through 9 and A, B, C, D, E, F for 10 through 15 (Chapter 2, Section 5). Because $16 = 2^4$, grouping the binary digits in fours from the right makes each group correspond to one hexadecimal digit. If the leftmost group has fewer than four digits, pad it with leading zeros.

**Solution.**

1. Splitting into groups of four from the right gives $0010 \mid 1110$.
2. $0010_2 = 2$, so the first group is the hexadecimal digit 2.
3. $1110_2 = 8 + 4 + 2 = 14$, and 14 is the hexadecimal digit E.
4. Juxtaposing the two digits gives $2E_{16}$.

Therefore $00101110_2 = 2E_{16}$. In decimal notation, $00101110_2 = 32 + 8 + 4 + 2 = 46$ and $2E_{16} = 2 \cdot 16 + 14 = 46$, which confirms the result.

---

<br>

## 6. Exercise 3.1.2: Truth of Statements about Numbers

**Problem.** Decide whether each statement is true or false, and justify the answer.

- (a) Every integer is a real number.
- (b) 0 is a positive real number.
- (c) For every real number $r$, $-r$ is a negative real number.
- (d) Every real number is an integer.

**Concepts used.** A **universal statement** $`\forall x \in D,\ Q(x)`$ is true only if $Q(x)$ is true for every element of $D$, and it is false if there is at least one element that makes $Q(x)$ false, that is, a **counterexample** ([Chapter 3, Section 1](../../Lecture-Notes/Ch03_The-Logic-of-Quantified-Statements/Concepts_Lecture.md)). A real number $x$ is positive if $x > 0$ and negative if $x < 0$.

**Solution.**

- (a) **True.** Every integer is a real number represented by a point on the number line. That is, the set $\mathbf{Z}$ of all integers is a subset of the set $\mathbf{R}$ of all real numbers.
- (b) **False.** A positive number is a number greater than 0, but $0 > 0$ is false. Zero is neither positive nor negative.
- (c) **False.** A counterexample is $r = 0$: $-0 = 0$ is not negative. $r = -5$ is another counterexample, for which $-r = 5$ is positive.
- (d) **False.** A counterexample is $\frac{1}{2} = 0.5$, a real number that is not an integer.

A statement beginning with "every", as in (c) and (d), is settled as false by a single counterexample. Conversely, to show that (a) is true, giving a few examples is not enough; the general fact that all integers are real numbers must be cited.

---

<br>

## 7. Exercise 3.1.4: Values That Make a Predicate False

**Problem.** Let $Q(x, y)$ denote the predicate "if $x < y$ then $x^2 < y^2$", where both $x$ and $y$ range over the set $\mathbf{R}$ of all real numbers. (a) Explain why $Q(-2, 1)$ is false, and (b) find one other pair of values, different from the pair in (a), that makes $Q(x, y)$ false.

**Concepts used.** A **predicate** is a sentence that contains variables and becomes a statement when values from the domain are substituted for the variables (Chapter 3, Section 1). $Q(x, y)$ is a predicate of conditional form, so it is false only for values at which the hypothesis $x < y$ is true and the conclusion $x^2 < y^2$ is false.

**Solution.**

(a) Substitute $x = -2$ and $y = 1$. The hypothesis $-2 < 1$ is true. The conclusion is $(-2)^2 < 1^2$, that is, $4 < 1$, which is false. A conditional with a true hypothesis and a false conclusion is false, so $Q(-2, 1)$ is false.

(b) For example, with $x = -3$ and $y = 2$, the hypothesis $-3 < 2$ is true and the conclusion $9 < 4$ is false, so $Q(-3, 2)$ is false. To find such values systematically, analyze the condition under which $Q(x, y)$ is false, namely $x < y$ together with $x^2 \ge y^2$.

1. If $x \ge 0$, then $0 \le x < y$, so $x^2 < y^2$ and $Q(x, y)$ is true. Hence $Q(x, y)$ can be false only if $x < 0$.
2. $x^2 \ge y^2$ is the same as $\lvert y \rvert \le \lvert x \rvert = -x$, that is, $x \le y \le -x$.
3. Combined with the hypothesis $x < y$, $Q(x, y)$ is false exactly when $x < y \le -x$.

$(-2, 1)$ satisfies $-2 < 1 \le 2$, and $(-3, 2)$, $(-1, 1)$, and $(-5, -4)$ also satisfy this condition, so all of them make $Q(x, y)$ false. For instance, at $(-5, -4)$, $-5 < -4$ holds, but $25 < 16$ is false.

---

<br>

## 8. Exercise 3.1.12: Disproving a Universal Statement by Counterexample

**Problem.** Disprove the following statement with a counterexample.

```math
\forall \text{ real numbers } x, y,\quad \sqrt{x + y} = \sqrt{x} + \sqrt{y}
```

**Concepts used.** A universal statement is disproved by a single counterexample (Chapter 3, Section 1). The square root $\sqrt{t}$ is defined as a real number when $t \ge 0$, so look for a counterexample among values with $x \ge 0$ and $y \ge 0$.

**Solution.** Let $x = 1$ and $y = 1$. The left side is $\sqrt{1 + 1} = \sqrt{2} \approx 1.414$, and the right side is $\sqrt{1} + \sqrt{1} = 1 + 1 = 2$. Since $\sqrt{2} \ne 2$, the equation fails at $(x, y) = (1, 1)$. Therefore the universal statement is false. $x = 1$ and $y = 3$ is also a counterexample: the left side is $\sqrt{4} = 2$ and the right side is $1 + \sqrt{3} \approx 2.732$.

> **Note:** For $x \ge 0$ and $y \ge 0$, the equation holds only when $x = 0$ or $y = 0$. Both sides are nonnegative, so squaring both sides gives an equivalent equation, and $x + y = x + 2\sqrt{x}\sqrt{y} + y$ yields $\sqrt{x}\sqrt{y} = 0$. Hence any two positive numbers form a counterexample.

---

<br>

## 9. Exercise 3.1.17: The Form of Existential Statements

**Problem.** Rewrite each statement in the form "$`\exists`$ \_\_\_\_ $x$ such that \_\_\_\_".

- (a) Some exercises have answers.
- (b) Some real numbers are rational.

**Concepts used.** An **existential statement** $\exists x \in D \text{ such that } Q(x)$ asserts that there is at least one $x$ in $D$ for which $Q(x)$ is true (Chapter 3, Section 1). In everyday language, "some A are B" means "there is at least one A that is B", so it is translated into an existential statement whose domain is A and whose predicate is B. "Such that" means "satisfying the following condition", and it is kept to match the form used in the textbook.

**Solution.**

- (a) The domain is the set of exercises and the predicate is "has an answer". $\exists$ an exercise $x$ such that $x$ has an answer.
- (b) The domain is the set of real numbers and the predicate is "is rational". $\exists$ a real number $x$ such that $x$ is rational.

Statement (b) is true because real numbers that are rational, such as $\frac{1}{2}$, do exist.

---

<br>

## 10. Exercise 3.1.26: Combining Universal and Existential Statements

**Problem.** For the statement "All integers are rational numbers but some rational numbers are not integers", (a) write it in the form "$`\forall x`$, if \_\_\_\_ then \_\_\_\_, but $\exists$ \_\_\_\_ $x$ such that \_\_\_\_", and (b) letting $\text{Ratl}(x)$ be "$`x`$ is a rational number" and $\text{Int}(x)$ be "$`x`$ is an integer", write it using only the symbols $\text{Ratl}(x)$, $\text{Int}(x)$, $\forall$, $\exists$, $\wedge$, $\vee$, $\sim$, and $\to$.

**Concepts used.** "All A are B" is translated into the **universal conditional statement** "$`\forall x`$, if $x$ is A then $x$ is B". "Some A are not B" is translated into the existential statement "$`\exists x`$ such that $x$ is A and $x$ is not B" (Chapter 3, Section 1). In logic, "but" is the conjunction $\wedge$, the same as "and".

**Solution.**

(a) $\forall x$, if $x$ is an integer then $x$ is a rational number, but $\exists$ a rational number $x$ such that $x$ is not an integer.

(b) The first part is the universal conditional statement $`\forall x\,(\text{Int}(x) \to \text{Ratl}(x))`$. The second part says "there is an $x$ that is rational and not an integer", so it is $`\exists x\,(\text{Ratl}(x) \wedge \sim\text{Int}(x))`$. Replace "but" by $\wedge$ to join the two parts.

```math
\big(\forall x\,(\text{Int}(x) \to \text{Ratl}(x))\big) \wedge \big(\exists x\,(\text{Ratl}(x) \wedge \sim\text{Int}(x))\big)
```

The first part is true because every integer $n$ can be written as $\frac{n}{1}$, and the second part is true because $\frac{1}{2}$ is rational but not an integer. Hence the original statement is true.

> **Caution:** Writing the second part with $\to$, as in $`\exists x\,(\text{Ratl}(x) \to \sim\text{Int}(x))`$, changes the meaning. This formula is true as soon as there is any $x$ that is not rational, such as $\sqrt{2}$, because the hypothesis is then false; so it does not express "there is a number that is rational and not an integer". In an existential statement, conditions are joined by $\wedge$.

---

<br>

## 11. Exercise 3.2.2: Negation of a Universal Statement

**Problem.** Find every statement among the eight below that is a negation of "All dogs are loyal"; there may be several.

- (a) All dogs are disloyal.
- (b) No dogs are loyal.
- (c) Some dogs are disloyal.
- (d) Some dogs are loyal.
- (e) There is a disloyal animal that is not a dog.
- (f) There is a dog that is disloyal.
- (g) No animals that are not dogs are loyal.
- (h) Some animals that are not dogs are loyal.

**Concepts used.** By Theorem 3.2.1, the negation of a universal statement $`\forall x \in D,\ Q(x)`$ is logically equivalent to the existential statement $\exists x \in D \text{ such that } \sim Q(x)$ (Chapter 3, Section 2). That is, the negation of "every $x$ has the property" is "there is at least one $x$ that does not have the property".

**Solution.** The original statement is "$`\forall`$ dogs $x$, $x$ is loyal", so its negation is "$`\exists`$ a dog $x$ such that $x$ is not loyal". Write each choice formally and compare it with this negation.

| Item | Formal expression | Negation? |
|:---:|:-----|:-----|
| (a) | $\forall$ dogs $x$, $x$ is not loyal | No. If loyal and disloyal dogs are mixed, both the original statement and (a) are false. |
| (b) | $\forall$ dogs $x$, $x$ is not loyal | No. It is the same statement as (a). |
| (c) | $\exists$ a dog $x$ such that $x$ is not loyal | Yes. |
| (d) | $\exists$ a dog $x$ such that $x$ is loyal | No. If all dogs are loyal, both the original statement and (d) are true. |
| (e) | $\exists$ an animal $x$ such that $x$ is not a dog and $x$ is not loyal | No. It is a statement about animals that are not dogs. |
| (f) | $\exists$ a dog $x$ such that $x$ is not loyal | Yes. It is the same statement as (c). |
| (g) | $\forall$ animals $x$, if $x$ is not a dog then $x$ is not loyal | No. It is a statement about animals that are not dogs. |
| (h) | $\exists$ an animal $x$ such that $x$ is not a dog and $x$ is loyal | No. It is a statement about animals that are not dogs. |

*Table 4. Comparison of candidate negations of "All dogs are loyal"*

Hence the negations are **(c) and (f)**. The negation of a statement must be false when the original is true and true when the original is false. Statements (a) and (b) can be false together with the original, and (d) can be true together with the original, so they are not negations.

---

<br>

## 12. Exercise 3.2.9: Negation of a Universal Conditional I

**Problem.** Write a negation of the statement "$`\forall`$ real numbers $x$, if $x > 3$ then $x^2 > 9$".

**Concepts used.** The negation of a universal conditional statement is the following (Chapter 3, Section 2).

```math
\sim\big(\forall x \in D,\ P(x) \to Q(x)\big) \equiv \exists x \in D \text{ such that } P(x) \wedge \sim Q(x)
```

This equivalence is obtained by turning $\forall$ into $\exists$ with Theorem 3.2.1 and then applying the negation of a conditional, $\sim(p \to q) \equiv p \wedge \sim q$. The hypothesis is kept, only the conclusion is negated, and the two parts are joined by $\wedge$.

**Solution.** $P(x)$ is "$`x > 3`$" and $Q(x)$ is "$`x^2 > 9`$". For real numbers, the negation of $x^2 > 9$ is $x^2 \le 9$, so the negation is the following.

```math
\exists \text{ a real number } x \text{ such that } x > 3 \text{ and } x^2 \le 9
```

In words, "there is a real number greater than 3 whose square is at most 9".

> **Caution:** What is negated is the whole conclusion $x^2 > 9$, so its negation is $x^2 \le 9$. Writing $x \le 9$ drops the square and produces an entirely different statement. Moreover, every real number $x > 3$ satisfies $x \cdot x > 3 \cdot x > 3 \cdot 3 = 9$, so the original statement is true and therefore this negation is false. To check that a negation is written correctly, it helps to see whether the original and the negation have opposite truth values.

---

<br>

## 13. Exercise 3.2.10: Negation of a Universal Conditional II

**Problem.** Write a negation of the statement "$`\forall`$ computer programs $P$, if $P$ compiles without error messages, then $P$ is correct".

**Concepts used.** Use the same rule for negating a universal conditional statement as in Exercise 3.2.9.

**Solution.** The hypothesis is "$`P`$ compiles without error messages" and the conclusion is "$`P`$ is correct". Turn $\forall$ into $\exists$, keep the hypothesis, negate the conclusion, and join them with $\wedge$.

$\exists$ a computer program $P$ such that $P$ compiles without error messages and $P$ is not correct.

In words, "there is a computer program that compiles without error messages but is not correct". Programs that contain no syntax errors but produce wrong results because of faulty logic are common, so this negation is true and the original statement is false.

---

<br>

## 14. Exercise 3.2.40: Sufficient Condition

**Problem.** Rewrite "Being divisible by 8 is a sufficient condition for being divisible by 4" in if-then form.

**Concepts used.** "$`\forall x`$, $r(x)$ is a **sufficient condition** for $s(x)$" means "$`\forall x`$, if $r(x)$ then $s(x)$" (Chapter 3, Section 2). A sufficient condition is one whose truth alone guarantees that the other condition holds.

**Solution.** $r(n)$ is "$`n`$ is divisible by 8" and $s(n)$ is "$`n`$ is divisible by 4". Take the set of all integers as the domain.

$\forall$ integers $n$, if $n$ is divisible by 8, then $n$ is divisible by 4.

Informally, "If a number is divisible by 8, then it is divisible by 4". This statement is true: if $n = 8k$ for some integer $k$, then $n = 4(2k)$ and $2k$ is also an integer.

---

<br>

## 15. Exercise 3.2.41: Necessary Condition

**Problem.** Rewrite "Being on time each day is a necessary condition for keeping this job" in if-then form.

**Concepts used.** "$`\forall x`$, $r(x)$ is a **necessary condition** for $s(x)$" means "$`\forall x`$, if $\sim r(x)$ then $\sim s(x)$", which by the contrapositive is equivalent to "$`\forall x`$, if $s(x)$ then $r(x)$" (Chapter 3, Section 2). A necessary condition is one without which the other condition cannot hold.

**Solution.** Take the set of all people as the domain, and let $r(x)$ be "$`x`$ is on time each day" and $s(x)$ be "$`x`$ keeps this job". The negation of $r(x)$ is "$`x`$ is not on time on some day". By the definition, the statement can be written in the following two ways, which are contrapositives of each other and hence equivalent.

- $\forall$ people $x$, if $x$ is not on time on some day, then $x$ will not keep this job.
- $\forall$ people $x$, if $x$ keeps this job, then $x$ is on time each day.

> **Caution:** "If $x$ is on time each day, then $x$ keeps this job" expresses a sufficient condition, not a necessary one; it is the converse of the statement above. Being on time alone does not guarantee keeping the job, so this sentence differs in meaning from the original.

---

<br>

## Summary

| Concept | Key Summary |
|:-----|:-----|
| Binary notation | Write an integer as a sum of powers of 2 and list the coefficients from the highest place, or read the remainders of repeated division by 2 in reverse. |
| Binary to decimal | Multiply each digit by its place value $2^k$ and add. |
| Binary addition | Add from the rightmost place with carries, using $1 + 1 = 10_2$ and $1 + 1 + 1 = 11_2$. |
| 8-bit two's complement | A negative $a$ is represented by $2^8 - \lvert a \rvert$; if the leftmost bit is 1, flip the bits and add 1 to get the absolute value. |
| Hexadecimal notation | Since $16 = 2^4$, group binary digits in fours from the right and replace each group by a hexadecimal digit 0-F. |
| Truth of a universal statement | It is true only if true for every element, and false if there is a single counterexample. |
| Conditional predicate | A predicate of the form $P(x) \to Q(x)$ is false only at values where the hypothesis is true and the conclusion is false. |
| Form of an existential statement | "Some A are B" is written "$`\exists`$ an A $x$ such that $x$ is B". |
| Combining universal and existential | "All A are B" is $`\forall x\,(A(x) \to B(x))`$, and "some A are not B" is $`\exists x\,(A(x) \wedge \sim B(x))`$. |
| Negation of a universal statement | $`\sim(\forall x \in D,\ Q(x)) \equiv \exists x \in D \text{ such that } \sim Q(x)`$. |
| Negation of a universal conditional | $`\sim(\forall x,\ P(x) \to Q(x)) \equiv \exists x \text{ such that } P(x) \wedge \sim Q(x)`$. |
| Sufficient condition | "$`r`$ is a sufficient condition for $s$" means "if $r$ then $s$". |
| Necessary condition | "$`r`$ is a necessary condition for $s$" means "if $\sim r$ then $\sim s$", that is, "if $s$ then $r$". |

---

<br>

## Self-Check Questions

1. **Converting notations:** Represent the decimal integer 100 in binary notation and in hexadecimal notation.

   <details>
   <summary>Answer</summary>

   $100 = 64 + 32 + 4$, so $100 = 1100100_2$. Grouping in fours from the right gives $0110 \mid 0100$, and $0110_2 = 6$ and $0100_2 = 4$, so $100 = 64_{16}$. As a check, $6 \cdot 16 + 4 = 100$.

   </details>

2. **Two's complement:** Find the 8-bit two's complement of $-20$.

   <details>
   <summary>Answer</summary>

   $20 = 00010100_2$. Flipping the bits gives $11101011$, and adding 1 gives $11101100$. Checking with the definition, $2^8 - 20 = 236 = 128 + 64 + 32 + 8 + 4 = 11101100_2$.

   </details>

3. **Binary addition:** Compute $1011_2 + 111_2$ in binary notation and check the result in decimal notation.

   <details>
   <summary>Answer</summary>

   From the right, $1 + 1 = 10_2$ (0, carry 1), $1 + 1 + 1 = 11_2$ (1, carry 1), $0 + 1 + 1 = 10_2$ (0, carry 1), $1 + 1 = 10_2$ (0, carry 1), and writing the last carry 1 gives $10010_2$. Since $1011_2 = 11$, $111_2 = 7$, and $10010_2 = 18$, indeed $11 + 7 = 18$.

   </details>

4. **Negating a universal conditional:** Write a negation of "For every integer $n$, if $n$ is prime then $n$ is odd", and decide which of the original statement and its negation is true.

   <details>
   <summary>Answer</summary>

   The negation is "$`\exists`$ an integer $n$ such that $n$ is prime and $n$ is not odd". Since $n = 2$ is prime and even, the negation is true and the original statement is false.

   </details>

5. **Necessary and sufficient conditions:** Write "Having four sides is a necessary condition for being a square" in two forms of a conditional statement.

   <details>
   <summary>Answer</summary>

   "$`\forall`$ figures $x$, if $x$ does not have four sides, then $x$ is not a square", and its contrapositive, "$`\forall`$ figures $x$, if $x$ is a square, then $x$ has four sides".

   </details>

6. **Counterexample:** Decide whether the statement "$`\forall x \in \mathbf{R},\ x^2 \ge x`$" is true.

   <details>
   <summary>Answer</summary>

   It is false. For $x = \frac{1}{2}$, $x^2 = \frac{1}{4} < \frac{1}{2} = x$, so this is a counterexample. In fact every real number with $0 < x < 1$ is a counterexample.

   </details>
