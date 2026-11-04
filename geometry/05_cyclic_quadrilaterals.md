# Cyclic Quadrilaterals & Power of a Point

## Quick Overview
Cyclic quadrilaterals (quadrilaterals whose vertices all lie on a single circle) and the power of a point are hot topics for national geometry finals.

## Core Theory
- **Opposite Angles:** In a cyclic quadrilateral, opposite angles are supplementary ($\alpha + \gamma = 180^\circ$).
- **Intersecting Chords Theorem (Power of a Point):** If two chords $AB$ and $CD$ intersect at an internal point $P$, then:
  $$PA \cdot PB = PC \cdot PD$$

## Python Verification
Script to verify the product of segments for intersecting chords:

```python
def verify_chord_theorem(pa: float, pb: float, pc: float, pd: float) -> bool:
    eps = 1e-5
    return abs((pa * pb) - (pc * pd)) < eps

if __name__ == "__main__":
    print("Chord theorem holds:", verify_chord_theorem(2.0, 6.0, 3.0, 4.0))
