# Linear Equations & Inequalities

## Quick Overview
Mastering linear equations and inequalities is the absolute foundation for solving multi-variable systems and bounding expressions in math contests.

## Core Concepts
- **Linear Equation:** An equation of the form $ax + b = 0$ (with $a \neq 0$), which has a unique solution $x = -\frac{b}{a}$.
- **Inequality Properties:** If $a < b$, then $a + c < b + c$. If $c > 0$, then $ac < bc$; however, if $c < 0$, the inequality sign flips ($ac > bc$).

## Python Check
A simple script to solve a linear equation and check an inequality condition:

```python
def solve_linear(a: float, b: float) -> float:
    if a == 0:
        raise ValueError("Coefficient 'a' cannot be zero for a linear equation.")
    return -b / a

def verify_inequality_flip(a: float, b: float, c: float) -> bool:
    # Checks property when multiplying by a negative number
    if c < 0:
        return (a * c) > (b * c)
    return (a * c) < (b * c)

if __name__ == "__main__":
    # Solves 2x + 6 = 0 -> x = -3
    x = solve_linear(2.0, 6.0)
    print("Solution for 2x + 6 = 0 is x =", x)
    
    # Check if 2 < 5 when multiplied by -2 (-4 > -10 should be True)
    print("Inequality flip holds:", verify_inequality_flip(2.0, 5.0, -2.0))
