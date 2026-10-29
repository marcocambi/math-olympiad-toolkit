# Divisibility & GCD Basics

## Quick Overview
Number theory contests almost always start with divisibility. Before using complex modular arithmetic, you need a solid grasp of how factors and the Greatest Common Divisor (GCD) work.

## Core Concepts
- **Divisibility:** We write $a \mid b$ ($a$ divides $b$) if there exists an integer $k$ such that $b = k \cdot a$.
- **GCD:** The greatest common divisor is the largest integer that divides both numbers without a remainder.

## Python Check
A very simple script using basic loops to find common divisors and the greatest common divisor step-by-step:

```python
def find_gcd_simple(a: int, b: int) -> int:
    smaller = a if a < b else b
    gcd = 1
    
    for i in range(1, smaller + 1):
        if a % i == 0 and b % i == 0:
            gcd = i
            
    return gcd

if __name__ == "__main__":
    num1 = 84
    num2 = 30
    print("GCD of", num1, "and", num2, "is:", find_gcd_simple(num1, num2))
