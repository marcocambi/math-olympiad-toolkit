```markdown
# The Pythagorean Theorem

## Quick Overview
The Pythagorean theorem relates the lengths of the sides of a right-angled triangle. It is one of the most frequently used tools for calculating lengths and distances in geometry problems.

## Core Formula
- **Pythagorean Relation:** In any right-angled triangle with legs $a$ and $b$ and hypotenuse $c$:
  $$a^2 + b^2 = c^2$$

## Python Check
A simple script to verify if three side lengths form a valid right-angled triangle:

```python
def verify_pythagorean(a: float, b: float, c: float) -> bool:
    # Ensure c is treated as the hypotenuse (the longest side)
    sides = sorted([a, b, c])
    leg1, leg2, hyp = sides[0], sides[1], sides[2]
    
    eps = 1e-5
    return abs((leg1**2 + leg2**2) - hyp**2) < eps

if __name__ == "__main__":
    print("Is (3, 4, 5) a right triangle?", verify_pythagorean(3.0, 4.0, 5.0))
