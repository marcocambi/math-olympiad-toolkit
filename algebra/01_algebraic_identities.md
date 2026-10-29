# Core Algebraic Identities

## Quick Overview
In algebra problems, factoring and expanding expressions quickly is half the battle. Knowing your identities by heart saves precious time during contests.

## Essential Formulas
- **Difference of Squares:** $a^2 - b^2 = (a - b)(a + b)$
- **Square of a Binomial:** $(a \pm b)^2 = a^2 \pm 2ab + b^2$
- **Cube Identities:** $a^3 + b^3 = (a + b)(a^2 - ab + b^2)$

## Python Check
A tiny script to verify the difference of squares programmatically:

```python
def verify_diff_of_squares(a: int, b: int) -> bool:
    left_side = a**2 - b**2
    right_side = (a - b) * (a + b)
    return left_side == right_side

if __name__ == "__main__":
    print("Identity holds:", verify_diff_of_squares(9, 4))
