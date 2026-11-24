# HW6 과제 안내문 — 집합론과 부울 대수

[레포지토리 안내](../../../README.ko.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **최종 수정일:** 2026-11-24

9주차에 나온 이산구조및연습 과제 6이다. 교재 Discrete Mathematics with Applications(Epp)의 6.1절(집합론: 정의와 원소 증명법), 6.2절(집합의 성질), 6.3절(반증과 대수적 증명), 6.4절(부울 대수, 러셀의 역설, 정지 문제)에서 고른 연습 문제 12개로 이루어지며, 문제 번호는 교재의 연습 문제 번호이다.

---

<br>

## 1. 연습 문제 6.1.15: 조건을 만족하는 벤 다이어그램

다음 각 경우에 주어진 조건을 모두 만족하는 집합 $A$, $B$, $C$의 벤 다이어그램을 그리라.

- (a) $A \cap B = \emptyset$, $A \subseteq C$, $C \cap B \ne \emptyset$
- (b) $A \subseteq B$, $C \subseteq B$, $A \cap C \ne \emptyset$
- (c) $A \cap B \ne \emptyset$, $B \cap C \ne \emptyset$, $A \cap C = \emptyset$, $A \not\subseteq B$, $C \not\subseteq B$

---

<br>

## 2. 연습 문제 6.1.24: 구간의 합집합과 교집합

음이 아닌 정수 $i$마다 $W_i = \lbrace x \in \mathbf{R} \mid x > i \rbrace = (i, \infty)$라 하자.

- (a) $\bigcup_{i=0}^{4} W_i$를 구하라.
- (b) $\bigcap_{i=0}^{4} W_i$를 구하라.
- (c) $W_0, W_1, W_2, \ldots$는 쌍마다 서로소인가? 이유를 설명하라.
- (d) $\bigcup_{i=0}^{n} W_i$를 구하라.
- (e) $\bigcap_{i=0}^{n} W_i$를 구하라.
- (f) $\bigcup_{i=0}^{\infty} W_i$를 구하라.
- (g) $\bigcap_{i=0}^{\infty} W_i$를 구하라.

---

<br>

## 3. 연습 문제 6.1.33: 공집합의 반복된 멱집합

다음을 구하라.

- (a) $\mathcal{P}(\emptyset)$
- (b) $\mathcal{P}(\mathcal{P}(\emptyset))$
- (c) $\mathcal{P}(\mathcal{P}(\mathcal{P}(\emptyset)))$

---

<br>

## 4. 연습 문제 6.2.7: 드모르간의 법칙의 원소 논증

모든 집합은 전체집합 $U$의 부분집합이라고 가정한다. 원소 논증으로 다음 명제를 증명하라.

- 모든 집합 $A$, $B$에 대해 $(A \cap B)^c = A^c \cup B^c$이다.

---

<br>

## 5. 연습 문제 6.2.20: 두 부분집합의 합집합

모든 집합은 전체집합 $U$의 부분집합이라고 가정한다. 원소 논증으로 다음 명제를 증명하라.

- 모든 집합 $A$, $B$, $C$에 대해, $A \subseteq C$이고 $B \subseteq C$이면 $A \cup B \subseteq C$이다.

---

<br>

## 6. 연습 문제 6.2.30: 집합과 그 여집합의 교집합

귀류법으로 다음 명제를 증명하라.

- 전체집합 $U$의 모든 부분집합 $A$에 대해 $A \cap A^c = \emptyset$이다.

---

<br>

## 7. 연습 문제 6.3.8: 여집합이 포함될 때의 합집합

모든 집합은 전체집합 $U$의 부분집합이라고 가정한다. 다음 명제가 참이면 증명하고, 거짓이면 반례를 제시하라.

- 모든 집합 $A$, $B$에 대해, $A^c \subseteq B$이면 $A \cup B = U$이다.

---

<br>

## 8. 연습 문제 6.3.24: 한 원소를 포함하는 부분집합과 포함하지 않는 부분집합

$A = \lbrace t, u, v, w \rbrace$라 하고, $S_1$을 $w$를 포함하지 않는 $A$의 부분집합 전체의 집합, $S_2$를 $w$를 포함하는 $A$의 부분집합 전체의 집합이라 하자.

- (a) $S_1$을 구하라.
- (b) $S_2$를 구하라.
- (c) $S_1$과 $S_2$는 서로소인가?
- (d) $S_1$과 $S_2$의 크기를 비교하라.
- (e) $S_1 \cup S_2$의 원소는 몇 개인가?
- (f) $S_1 \cup S_2$와 $\mathcal{P}(A)$는 어떤 관계인가?

---

<br>

## 9. 연습 문제 6.3.31: 차집합이 들어 있는 합집합의 대수적 증명

다음 명제의 대수적 증명을 쓰라. 모든 단계에 정리 6.2.2의 성질을 근거로 밝히라.

- 모든 집합 $A$, $B$에 대해 $A \cup (B - A) = A \cup B$이다.

---

<br>

## 10. 연습 문제 6.4.1: 곱의 멱등 법칙

$B$가 연산 $+$와 $\cdot$을 가진 부울 대수라 하자. 부울 대수의 공리만 써서 다음 증명의 빈칸 (a)~(e)에 들어갈 근거를 채우라.

**곱의 멱등 법칙:** $B$의 모든 $a$에 대해 $a \cdot a = a$이다.

**증명.** $a$를 $B$의 임의의 원소라 하자. 그러면 다음이 성립한다.

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

## 11. 연습 문제 6.4.3: 흡수 법칙

$B$가 연산 $+$와 $\cdot$을 가진 부울 대수라 하자. 부울 대수의 공리만 써서 다음 증명의 빈칸 (a)~(f)에 들어갈 근거를 채우라. 연습 문제 6.4.1은 곱의 멱등 법칙 $a \cdot a = a$이고, 연습 문제 6.4.2는 합의 전체 한계 법칙 $a + 1 = 1$이다.

**$+$에 대한 $\cdot$의 흡수 법칙:** $B$의 모든 $a$, $b$에 대해 $(a + b) \cdot a = a$이다.

**증명.** $a$와 $b$를 $B$의 임의의 원소라 하자. 그러면 다음이 성립한다.

```math
\begin{aligned}
(a + b) \cdot a &= a \cdot (a + b) && \text{(a)} \\
&= a \cdot a + a \cdot b && \text{(b)} \\
&= a + a \cdot b && \text{연습 문제 6.4.1에 의해} \\
&= a \cdot 1 + a \cdot b && \text{(c)} \\
&= a \cdot (1 + b) && \text{(d)} \\
&= a \cdot (b + 1) && \text{(e)} \\
&= a \cdot 1 && \text{연습 문제 6.4.2에 의해} \\
&= a && \text{(f)}
\end{aligned}
```

---

<br>

## 12. 연습 문제 6.4.6: 0의 유일성

$B$가 연산 $+$와 $\cdot$을 가진 부울 대수라 하자. 부울 대수의 공리와, 교재 본문이나 앞 번호의 연습 문제에서 증명한 명제만 써서 다음 명제를 증명하라.

- $B$에서 $+$에 대한 항등원인 원소는 하나뿐이다.

---

<br>

문제를 풀어 본 뒤 [과제 해설](../Assignment-Explanation.ko.md)에서 정답과 풀이를 볼 수 있다.
