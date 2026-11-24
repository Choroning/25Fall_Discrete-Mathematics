# HW7 과제 안내문 — 함수와 기수

[레포지토리 안내](../../../README.ko.md) | [English](Assignment.md) | [한국어](Assignment.ko.md)

> **최종 수정일:** 2026-11-24

10주차에 나온 이산구조및연습 과제 7이다. 교재 Discrete Mathematics with Applications(Epp)의 7.1절(일반 집합 위에서 정의된 함수), 7.2절(일대일 함수, 위로의 함수, 역함수), 7.3절(함수의 합성), 7.4절(기수와 계산 가능성)에서 고른 연습 문제 11개로 이루어지며, 문제 번호는 교재의 연습 문제 번호이다.

---

<br>

## 1. 연습 문제 7.1.9: 양의 약수의 합 함수

함수 $S: \mathbf{Z}^{+} \to \mathbf{Z}^{+}$를 다음과 같이 정의한다. 각 양의 정수 $n$에 대해 $S(n)$은 $n$의 양의 약수 전체의 합이다. 다음 값을 구하라.

- (a) $S(1)$
- (b) $S(15)$
- (c) $S(17)$
- (d) $S(5)$
- (e) $S(18)$
- (f) $S(21)$

---

<br>

## 2. 연습 문제 7.1.15: 곱 함수의 상등

$F$와 $G$를 실수 전체의 집합에서 그 자신으로의 함수라 하자. 곱 함수 $F \cdot G: \mathbf{R} \to \mathbf{R}$와 $G \cdot F: \mathbf{R} \to \mathbf{R}$를 모든 $x \in \mathbf{R}$에 대해 다음과 같이 정의한다.

```math
(F \cdot G)(x) = F(x) \cdot G(x), \qquad (G \cdot F)(x) = G(x) \cdot F(x)
```

$F \cdot G = G \cdot F$인가? 이유를 설명하라.

---

<br>

## 3. 연습 문제 7.1.21: 역수의 로그

$b$가 $b \neq 1$인 양의 실수이고 $x$가 실수일 때 $b^{-x}$는 $b^{-x} = \frac{1}{b^x}$로 정의된다. 이 정의와 로그의 정의를 이용하여, $b \neq 1$인 모든 양의 실수 $u$와 $b$에 대해 다음 등식이 성립함을 증명하라.

```math
\log_b\left(\frac{1}{u}\right) = -\log_b(u)
```

---

<br>

## 4. 연습 문제 7.2.10: 2배 함수의 일대일성과 위로의 성질

- (a) $f: \mathbf{Z} \to \mathbf{Z}$를 모든 정수 $n$에 대해 규칙 $f(n) = 2n$으로 정의한다.
  - (i) $f$는 일대일 함수인가? 증명하거나 반례를 제시하라.
  - (ii) $f$는 위로의 함수인가? 증명하거나 반례를 제시하라.
- (b) $2\mathbf{Z}$를 짝수 전체의 집합, 곧 $2\mathbf{Z} = \lbrace n \in \mathbf{Z} \mid \text{어떤 정수 } k\text{에 대해 } n = 2k \rbrace$라 하자. $h: \mathbf{Z} \to 2\mathbf{Z}$를 각 정수 $n$에 대해 규칙 $h(n) = 2n$으로 정의한다. $h$는 위로의 함수인가? 증명하거나 반례를 제시하라.

---

<br>

## 5. 연습 문제 7.2.16: 분수 함수의 일대일성 판정

모든 실수 $x$에 대해 정의된 다음 함수 $f$가 일대일 함수인지 판정하고, 답의 근거를 쓰라.

```math
f(x) = \frac{x}{x^2 + 1}
```

---

<br>

## 6. 연습 문제 7.2.41: 위로의 함수와 역상의 상

$F: X \to Y$가 위로의 함수라 하자. $Y$의 모든 부분집합 $B$에 대해 $F(F^{-1}(B)) = B$임을 증명하라.

---

<br>

## 7. 연습 문제 7.3.7: 제곱 함수와 mod 5 함수의 합성

$L: \mathbf{Z} \to \mathbf{Z}$와 $M: \mathbf{Z} \to \mathbf{Z}$를 각 정수 $a$에 대해 규칙 $L(a) = a^2$, $M(a) = a \bmod 5$로 정의한다.

- (a) $(L \circ M)(12)$, $(M \circ L)(12)$, $(L \circ M)(9)$, $(M \circ L)(9)$를 구하라.
- (b) $L \circ M = M \circ L$인가?

---

<br>

## 8. 연습 문제 7.3.10: 2배 함수와 바닥 함수의 합성

$F: \mathbf{Z} \to \mathbf{Z}$와 $G: \mathbf{Z} \to \mathbf{Z}$를 모든 정수 $n$에 대해 규칙 $F(n) = 2n$, $G(n) = \lfloor n/2 \rfloor$로 정의한다.

- (a) $(G \circ F)(8)$, $(F \circ G)(8)$, $(G \circ F)(3)$, $(F \circ G)(3)$을 구하라.
- (b) $G \circ F = F \circ G$인가? 설명하라.

---

<br>

## 9. 연습 문제 7.3.17: 함수와 그 역함수의 합성

정리 7.3.2(b)를 증명하라. 곧 $f: X \to Y$가 역함수 $f^{-1}: Y \to X$를 갖는 일대일 함수이자 위로의 함수이면, $Y$ 위의 항등 함수 $I_Y$에 대해 $f \circ f^{-1} = I_Y$임을 증명하라.

---

<br>

## 10. 연습 문제 7.4.3: 정수 전체와 3의 배수 전체의 기수

$3\mathbf{Z} = \lbrace n \in \mathbf{Z} \mid \text{어떤 정수 } k\text{에 대해 } n = 3k \rbrace$라 하자. $\mathbf{Z}$와 $3\mathbf{Z}$의 기수가 같음을 증명하라.

---

<br>

## 11. 연습 문제 7.4.10: 두 열린 구간의 기수

$S$를 0과 1 사이에 있는 실수 전체의 집합, 곧 $S = \lbrace x \in \mathbf{R} \mid 0 < x < 1 \rbrace$이라 하고, $U = \lbrace x \in \mathbf{R} \mid 0 < x < 2 \rbrace$라 하자. $S$와 $U$의 기수가 같음을 증명하라.

---

<br>

문제를 풀어 본 뒤 [과제 해설](../Assignment-Explanation.ko.md)에서 정답과 풀이를 볼 수 있다.
