```markdown
# Polynomials & Vieta's Formulas

## Quick Overview
Polynomial manipulation and the relationship between coefficients and roots are vital for algebra problems in math contests.

## Core Formulas
- **Division Algorithm:** `P(x) = D(x) * Q(x) + R(x)`, where `deg(R) < deg(D)`
- **Vieta's Formulas (Quadratic `ax^2 + bx + c = 0`):**
  - Sum of roots: `r1 + r2 = -b / a`
  - Product of roots: `r1 * r2 = c / a`

## Python Check
A simple script to verify Vieta's formulas for a quadratic polynomial:

```python
def verify_vietas_quadratic(a: float, b: float, c: float, r1: float, r2: float) -> bool:
    sum_formula = -b / a
    prod_formula = c / a
    
    actual_sum = r1 + r2
    actual_prod = r1 * r2
    
    eps = 1e-5
    return abs(sum_formula - actual_sum) < eps and abs(prod_formula - actual_prod) < eps

if __name__ == "__main__":
    print("Vieta's formulas hold:", verify_vietas_quadratic(1.0, -5.0, 6.0, 2.0, 3.0))
    
    eps = 1e-5
    return abs(sum_formula - actual_sum) < eps and abs(prod_formula - actual_prod) < eps

if __name__ == "__main__":
    # For x^2 - 5x + 6 = 0, roots are 2 and 3
    print("Vieta's formulas hold:", verify_vietas_quadratic(1.0, -5.0, 6.0, 2.0, 3.0))