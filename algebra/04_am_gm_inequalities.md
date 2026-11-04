# AM-GM Inequality & Contest Optimization

## Quick Overview
Inequalities are a cornerstone of advanced competition algebra. The Arithmetic Mean-Geometric Mean (AM-GM) inequality is the primary tool for solving maximum and minimum problems without relying on calculus.

## Core Theory
- **AM-GM for $n$ non-negative variables:**
  $$\frac{x_1 + x_2 + \dots + x_n}{n} \ge \sqrt[n]{x_1 x_2 \dots x_n}$$
- Equality holds if and only if $x_1 = x_2 = \dots = x_n$.

## Python Verification
A simple script to verify the AM-GM inequality with random values:

```python
import random

def verify_am_gm() -> bool:
    values = [random.uniform(1.0, 10.0) for _ in range(3)]
    am = sum(values) / len(values)
    gm = (values[0] * values[1] * values[2]) ** (1 / 3)
    return am >= gm

if __name__ == "__main__":
    print("AM >= GM holds:", verify_am_gm())
