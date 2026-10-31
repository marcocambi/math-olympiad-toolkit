# Modular Arithmetic & Congruences

## Quick Overview

Modular arithmetic is fundamental to contest number theory. Instead of dealing with arbitrarily large numbers, we focus on the remainders left when numbers are divided by a fixed integer called the modulus.

## Core Concepts

* **Congruence:** We write $a \equiv b \pmod m$ if $m$ divides the difference $a - b$. That is, $a$ and $b$ leave the same remainder when divided by $m$.
* **Properties:** Congruences can be added, subtracted, and multiplied:
  $$\text{If } a \equiv b \pmod m \text{ and } c \equiv d \pmod m \implies a \cdot c \equiv b \cdot d \pmod m$$
* **Modular Inverse:** The inverse of $a \pmod m$ exists if and only if $\gcd(a, m) = 1$.
* **Fermat's Little Theorem:** If $p$ is a prime number and $p \nmid a$, then:
  $$a^{p-1} \equiv 1 \pmod p$$

## Python Check

A simple script implementing the Extended Euclidean Algorithm to compute the modular multiplicative inverse step-by-step:

```python
def modular_inverse(a: int, m: int) -> int:
    m0, x0, x1 = m, 0, 1
    if m == 1:
        return 0
    while a > 1:
        q = a // m
        m, a = a % m, m
        x0, x1 = x1 - q * x0, x0
    if x1 < 0:
        x1 += m0
    return x1


if __name__ == "__main__":
    a = 3
    m = 11
    inv = modular_inverse(a, m)
    print("Modular inverse of", a, "mod", m, "is:", inv)
    print("Verification:", (a * inv) % m == 1)

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
