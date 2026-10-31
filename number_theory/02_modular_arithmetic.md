# 02. Modular Arithmetic and Congruences

## 1. Definition and Basic Properties
Let $m$ be a positive integer (the modulus). Two integers $a$ and $b$ are said to be congruent modulo $m$ if $m$ divides their difference:
$$a \equiv b \pmod m \iff m \mid (a - b)$$

### Algebraic Properties:
If $a \equiv b \pmod m$ and $c \equiv d \pmod m$, then:
* **Addition:** $a + c \equiv b + d \pmod m$
* **Multiplication:** $a \cdot c \equiv b \cdot d \pmod m$
* **Powers:** $a^k \equiv b^k \pmod m$ for any integer $k \ge 0$

---

## 2. Modular Inverse
The modular inverse of $a$ modulo $m$ is an integer $a^{-1}$ such that:
$$a \cdot a^{-1} \equiv 1 \pmod m$$
* **Existence:** The inverse exists if and only if $\gcd(a, m) = 1$ (coprime).
* **Computation:** Solved via Bézout's Identity using the Extended Euclidean Algorithm.

---

## 3. Fundamental Theorems
* **Fermat's Little Theorem:** 
  If $p$ is a prime number and $p \nmid a$, then:
  $$a^{p-1} \equiv 1 \pmod p$$
  *(General form: $a^p \equiv a \pmod p$ for any integer $a$)*

* **Chinese Remainder Theorem (CRT):**
  A system of congruences of the form:
  $$\begin{cases} x \equiv a_1 \pmod{m_1} \\ x \equiv a_2 \pmod{m_2} \end{cases}$$
  has a unique solution modulo $\text{lcm}(m_1, m_2)$ if and only if $\gcd(m_1, m_2) \mid (a_1 - a_2)$.

---

## 4. Contest Techniques & Tricks
* **Residue Analysis:** Working modulo $3, 4, 8$, or $p$ (prime) is frequently used to prove that a Diophantine equation has no solutions (e.g., perfect squares modulo $4$ can only be $0$ or $1$).
* **Last Digits:** 
  * Decimal trailing digits $\implies$ work modulo $10^k$ (often split into $\pmod{2^k}$ and $\pmod{5^k}$).
