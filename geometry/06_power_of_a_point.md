# Power of a Point & Radical Axis

## Quick Overview
The power of a point theorem relates lengths of line segments associated with a point and a circle, serving as a powerful tool for proving collinearity and concyclicity in advanced geometry.

## Core Theory
- **Theorem Statement:** If a line through a point $P$ intersects a circle at points $A$ and $B$, the product of the lengths $PA \cdot PB$ is constant regardless of the line's angle, depending only on the distance from $P$ to the circle's center.
- **Tangent-Secant Theorem:** If a tangent from $P$ touches the circle at $T$ and a secant intersects at $A$ and $B$, then $PT^2 = PA \cdot PB$.

## Python Verification
A Python script to verify the power of a point relationship for intersecting secants:

```python
def verify_power_of_point(pa: float, pb: float, pc: float, pd: float) -> bool:
    eps = 1e-5
    return abs((pa * pb) - (pc * pd)) < eps

if __name__ == "__main__":
    print("Power of a point holds:", verify_power_of_point(3.0, 8.0, 4.0, 6.0))
