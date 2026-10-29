# Triangle Basics: Angles & Sides

## Quick Overview
Before jumping into advanced theorems, everything in triangle geometry builds on basic angle chasing and side inequalities. If you miss these fundamentals, harder proofs fall apart.

## Core Rules
- **Angle Sum:** The interior angles of any triangle always add up to $180^\circ$.
- **Triangle Inequality:** For any triangle with sides $a, b, c$:
  $$a + b > c$$
  The sum of any two sides must strictly exceed the third.

## Python Check
A simple script using basic conditional checks to see if three side lengths can form a valid triangle:

```python
def is_valid_triangle(a: float, b: float, c: float) -> bool:
    cond1 = (a + b > c)
    cond2 = (a + c > b)
    cond3 = (b + c > a)
    return cond1 and cond2 and cond3

if __name__ == "__main__":
    print("Can form triangle?", is_valid_triangle(3.0, 4.0, 5.0))
