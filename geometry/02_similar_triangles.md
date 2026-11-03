# Similar Triangles & Proportions

## Quick Overview
Similar triangles allow you to translate angle information into ratio equations for side lengths, serving as a core tool in geometric proofs.

## Core Criteria
- **Ratio Property:** If triangle ABC is similar to triangle DEF, then corresponding sides are proportional: 
 AB / DE = BC / EF = AC / DF = k.

## Python Check
A simple script to verify if two triangles satisfy the side proportion condition for similarity:

```python
def check_similar_sides(sides1: tuple[float, float, float], sides2: tuple[float, float, float]) -> bool:
    s1 = sorted(sides1)
    s2 = sorted(sides2)
    ratio1 = s2[0] / s1[0]
    ratio2 = s2[1] / s1[1]
    ratio3 = s2[2] / s1[2]
    eps = 1e-5
    return abs(ratio1 - ratio2) < eps and abs(ratio2 - ratio3) < eps


if __name__ == "__main__":
    t1 = (3.0, 4.0, 5.0)
    t2 = (6.0, 8.0, 10.0)
    are_similar = check_similar_sides(t1, t2)
    print("Are triangles similar by side ratios?", are_similar)