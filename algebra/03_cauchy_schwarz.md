# Cauchy-Schwarz Inequality

## Quick Overview
The Cauchy-Schwarz inequality is one of the most powerful tools in contest algebra for proving bounds and optimizing expressions.

## Core Formula
- **Algebraic Form:** For any real numbers $a_1, a_2, \dots, a_n$ and $b_1, b_2, \dots, b_n$:
  $$\left(\sum_{i=1}^{n} a_i b_i\right)^2 \leq \left(\sum_{i=1}^{n} a_i^2\right) \left(\sum_{i=1}^{n} b_i^2\right)$$
  Equality holds if and only if the sequences $a$ and $b$ are proportional.

## Python Check
A simple script to verify the Cauchy-Schwarz inequality for vectors of size 3:

```python
def verify_cauchy_schwarz(a: tuple[float, float, float], b: tuple[float, float, float]) -> bool:
    dot_product = sum(ai * bi for ai, bi in zip(a, b))
    sum_a_sq = sum(ai ** 2 for ai in a)
    sum_b_sq = sum(bi ** 2 for bi in b)
    
    lhs = dot_product ** 2
    rhs = sum_a_sq * sum_b_sq
    
    eps = 1e-5
    return lhs <= rhs + eps

if __name__ == "__main__":
    v1 = (1.0, 2.0, 3.0)
    v2 = (4.0, 5.0, 6.0)
    print("Cauchy-Schwarz holds:", verify_cauchy_schwarz(v1, v2))
