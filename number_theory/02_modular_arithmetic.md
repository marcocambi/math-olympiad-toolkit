# Modular Arithmetic & Congruences

## Quick Overview
Modular arithmetic reduces infinite integer sets to a finite ring of residues, serving as the primary instrument for divisibility and contest problems.

## Core Theory
- **Congruence Definition:** a ≡ b (mod m) if m divides (a - b).
- **Fermat's Little Theorem:** If p is a prime number and p does not divide a, then a^(p-1) ≡ 1 (mod p).

## Python Check
Computational validation of Fermat's Little Theorem:

```python
def check_fermat(a: int, p: int) -> bool:
    if p <= 1 or a % p == 0:
        return False
    return pow(a, p - 1, p) == 1


if __name__ == "__main__":
    base = 3
    prime = 7
    holds = check_fermat(base, prime)
    print(f"Fermat holds for a={base}, p={prime}:", holds)