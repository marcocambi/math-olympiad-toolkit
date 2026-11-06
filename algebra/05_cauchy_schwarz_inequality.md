# Cauchy-Schwarz Inequality

## Quick Overview
The Cauchy-Schwarz inequality is one of the most important and versatile inequalities in mathematics. In competition algebra, it is frequently used to prove bounds and solve multi-variable optimization problems.

## Core Theory
- **Algebraic Form (Sum form):** 
  For any real numbers $a_1, a_2, \dots, a_n$ and $b_1, b_2, \dots, b_n$:
  $$(a_1^2 + a_2^2 + \dots + a_n^2)(b_1^2 + b_2^2 + \dots + b_n^2) \ge (a_1 b_1 + a_2 b_2 + \dots + a_n b_n)^2$$
- **Equality Condition:** Equality holds if and only if the sequences $a_i$ and $b_i$ are proportional ($a_i = k \cdot b_i$ for all $i$).

## Python Verification
A Python script to verify Cauchy-Schwarz for two vectors:

```python
def verify_cauchy_schwarz(a: list[float], b: list[float]) -> bool:
    if len(a) != len(b):
        raise ValueError("Vectors must have the same length.")
    
    sum_a_sq = sum(x ** 2 for x in a)
    sum_b_sq = sum(y ** 2 for y in b)
    dot_product = sum(x * y for x, y in zip(a, b))
    
    left_side = sum_a_sq * sum_b_sq
    right_side = dot_product ** 2
    
    return left_side >= right_side - 1e-5

if __name__ == "__main__":
    v1 = [1.0, 2.0, 3.0]
    v2 = [4.0, 5.0, 6.0]
    print("Cauchy-Schwarz holds:", verify_cauchy_schwarz(v1, v2))
