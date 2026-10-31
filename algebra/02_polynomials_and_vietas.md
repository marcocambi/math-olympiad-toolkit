# Polynomials & Vieta's Formulas

## Quick Overview

Polynomial manipulation and the relationship between coefficients and roots are vital for algebra problems in math contests. Mastering polynomial division and Vieta's formulas drastically cuts down solving time.

## Core Concepts

* **Division Algorithm:** For polynomials $P(x)$ and $D(x)$ with $\deg(D) \le \deg(P)$, there exist unique polynomials $Q(x)$ and $R(x)$ such that:
  $$P(x) = D(x) \cdot Q(x) + R(x)$$
  where either $R(x) = 0$ or $\deg(R) < \deg(D)$.
* **Remainder & Factor Theorem:** The remainder of $P(x)$ divided by $(x - c)$ is $P(c)$. Consequently, $(x - c)$ is a factor if and only if $P(c) = 0$.
* **Vieta's Formulas:** For a monic polynomial $P(x) = x^n + a_{n-1}x^{n-1} + \dots + a_0 = (x - r_1)(x - r_2)\dots(x - r_n)$:
  * Sum of roots: $\sum r_i = -a_{n-1}$
  * Product of roots: $\prod r_i = (-1)^n a_0$
* **Quadratic Case ($ax^2 + bx + c = 0$):**
  * $r_1 + r_2 = -\frac{b}{a}$
  * $r_1 r_2 = \frac{c}{a}$

## Contest Techniques

* **Rational Root Theorem:** Any rational root $p/q$ (in lowest terms) of a polynomial with integer coefficients must satisfy $p \mid a_0$ and $q \mid a_n$.

## Python Check

A simple script to verify Vieta's formulas for a quadratic polynomial:

```python
def verify_vietas_quadratic(a: float, b: float, c: float, r1: float, r2: float) -> bool:
    sum_roots_formula = -b / a
    product_roots_formula = c / a
    
    actual_sum = r1 + r2
    actual_product = r1 * r2
    
    print(f"Sum check: {sum_roots_formula} == {actual_sum}")
    print(f"Product check: {product_roots_formula} == {actual_product}")
    
    return abs(sum_roots_formula - actual_sum) < 1e-9 and abs(product_roots_formula - actual_product) < 1e-9


if __name__ == "__main__":
    # For x^2 - 5x + 6 = 0, roots are 2 and 3
    a, b, c = 1.0, -5.0, 6.0
    r1, r2 = 2.0, 3.0
    is_valid = verify_vietas_quadratic(a, b, c, r1, r2)
    print("Vieta's formulas hold:", is_valid)
