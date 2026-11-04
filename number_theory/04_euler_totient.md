# Euler's Totient Function & Theorem

## Quick Overview
Euler's totient function $\phi(n)$ counts how many integers between $1$ and $n$ are coprime to $n$. It is a key tool for handling high modular powers in national contests.

## Core Theory
- **Definition:** $\phi(n) = n \prod_{p \vert{} n} \left(1 - \frac{1}{p}\right)$ where $p$ are the distinct prime factors of $n$.
- **Euler-Fermat Theorem:** If $\text{gcd}(a, n) = 1$, then:
  $$a^{\phi(n)} \equiv 1 \pmod n$$

## Python Verification
Script to compute the totient function and verify the theorem:

```python
def gcd(a: int, b: int) -> int:
    while b:
        a, b = b, a % b
    return a

def euler_totient(n: int) -> int:
    count = 0
    for i in range(1, n + 1):
        if gcd(i, n) == 1:
            count += 1
    return count

if __name__ == "__main__":
    n = 9
    print(f"Phi({n}) =", euler_totient(n))
