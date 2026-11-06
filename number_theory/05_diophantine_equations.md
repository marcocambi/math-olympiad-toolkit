# Diophantine Equations

## Quick Overview
A Diophantine equation is a polynomial equation where integer solutions are sought. Linear Diophantine equations form the basis of modular inverses and remainder problems in number theory.

## Core Theory
- **Linear Diophantine Equation:** An equation of the form $ax + by = c$.
- **Solvability Condition:** Has solutions if and only if $\text{gcd}(a, b)$ divides $c$.
- **Extended Euclidean Algorithm:** Used to find particular integer solutions $(x_0, y_0)$.

## Python Verification
A Python script to check if a linear Diophantine equation has integer solutions:

```python
def gcd(a: int, b: int) -> int:
    while b:
        a, b = b, a % b
    return a

def check_diophantine_solvable(a: int, b: int, c: int) -> bool:
    return c % gcd(a, b) == 0

if __name__ == "__main__":
    print("Is 6x + 9y = 15 solvable?", check_diophantine_solvable(6, 9, 15))
    print("Is 6x + 9y = 7 solvable?", check_diophantine_solvable(6, 9, 7))
