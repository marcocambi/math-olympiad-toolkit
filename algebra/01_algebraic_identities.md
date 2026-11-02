# Core Algebraic Identities

## Quick Overview
In algebra problems, factoring and expanding expressions quickly is the key. Knowing your identities by heart saves time during contests.

## Core Formulas
- **Difference of Squares:** a^2 - b^2 = (a - b) * (a + b)
- **Square of a Binomial:** (a ± b)^2 = a^2 ± 2ab + b^2

## Python Check
A simple script to verify the difference of squares:

```python
def verify_diff_of_squares(a: int, b: int) -> bool:
    left = (a * a) - (b * b)
    right = (a - b) * (a + b)
    return left == right


if __name__ == "__main__":
    a_val = 9
    b_val = 4
    result = verify_diff_of_squares(a_val, b_val)
    print("Identity holds:", result)
