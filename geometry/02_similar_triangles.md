# Similar Triangles & Proportions

## Quick Overview
Once you master basic triangle properties, similar triangles become your primary weapon for geometric problem-solving. They allow you to translate angle information into ratio equations for side lengths.

## Core Criteria
Two triangles are similar if their corresponding angles are equal and their corresponding sides are in proportion:
- **AA (Angle-Angle):** If two angles of one triangle are congruent to two angles of another triangle, the triangles are similar.
- **Ratio Property:** If $\triangle ABC \sim \triangle DEF$, then:
  $$\frac{AB}{DE} = \frac{BC}{EF} = \frac{AC}{DF} = k$$

## Python Check
A simple script to verify if two triangles satisfy the side proportion condition for similarity:

```python
def check_similar_sides(sides1: tuple[float, float, float], sides2: tuple[float, float, float]) -> bool:
    # Sort sides to align corresponding lengths
    s1 = sorted(sides1)
    s2 = sorted(sides2)
    
    ratio1 = s2[0] / s1[0]
    ratio2 = s2[1] / s1[1]
    ratio3 = s2[2] / s1[2]
    
    # Check if ratios are equal within a small tolerance
    eps = 1e-5
    return abs(ratio1 - ratio2) < eps and abs(ratio2 - ratio3) < eps

if __name__ == "__main__":
    t1 = (3.0, 4.0, 5.0)
    t2 = (6.0, 8.0, 10.0)
    print("Are triangles similar by side ratios?", check_similar_sides(t1, t2))