# Divisibility & GCD Basics

## Quick Overview
Number theory contests almost always start with divisibility. Before using complex modular arithmetic, you need a solid grasp of how factors and the Greatest Common Divisor (GCD) work.

## Core Concepts
- **Divisibility:** We write $a \mid b$ ($a$ divides $b$) if there exists an integer $k$ such that $b = k \cdot a$.
- **Euclidean Algorithm:** To find $\gcd(a, b)$, repeatedly apply division with remainder:
  $$\gcd(a, b) = \gcd(b, a \pmod b)$$
  until the remainder is 0.

## Python Check
Using Python's built-in math module to check GCD quickly:

```python
import math

def compute_gcd(a: int, b: int) -> int:
    return math.gcd(a, b)

if __name__ == "__main__":
    print("GCD of 84 and 30 is:", compute_gcd(84, 30))
