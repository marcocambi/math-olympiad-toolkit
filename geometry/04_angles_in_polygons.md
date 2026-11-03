# Angles in Polygons

## Quick Overview
Understanding the sum of interior and exterior angles of polygons is a fundamental geometric tool used extensively in contest geometry and angle-chasing problems.

## Core Formulas
- **Sum of Interior Angles:** For an $n$-sided convex polygon:
  $$\text{Sum} = (n - 2) \times 180^\circ$$
- **Sum of Exterior Angles:** The sum of the exterior angles of any convex polygon is always $360^\circ$.

## Python Check
A simple script to calculate the interior angle sum and each interior angle of a regular polygon:

```python
def polygon_angles(n: int) -> tuple[float, float]:
    if n < 3:
        raise ValueError("A polygon must have at least 3 sides.")
    
    total_interior_sum = (n - 2) * 180
    each_interior_angle = total_interior_sum / n
    return total_interior_sum, each_interior_angle

if __name__ == "__main__":
    sides = 5  # Pentagon
    total_sum, each_angle = polygon_angles(sides)
    print(f"For a regular {sides}-sided polygon:")
    print(f"Total interior sum: {total_sum}°")
    print(f"Each interior angle: {each_angle}°")
