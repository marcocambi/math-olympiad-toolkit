# Principle of Inclusion-Exclusion (PIE)

## Quick Overview
The Principle of Inclusion-Exclusion allows us to compute the size of the union of overlapping sets by correcting double (or multiple) counts. It is essential for advanced combinatorics and number theory (e.g., Euler's totient function).

## Core Theory
- **For two sets:** 
  $$\vert{}A \cup B\vert{} = \vert{}A\vert{} + \vert{}B\vert{} - \vert{}A \cap B\vert{}$$
- **For three sets:** 
  $$\vert{}A \cup B \cup C\vert{} = \vert{}A\vert{} + \vert{}B\vert{} + \vert{}C\vert{} - (\vert{}A \cap B\vert{} + \vert{}A \cap C\vert{} + \vert{}B \cap C\vert{}) + \vert{}A \cap B \cap C\vert{}$$

## Python Verification
Script to verify PIE on two numerical sets:

```python
def verify_pie(set_a: set, set_b: set) -> bool:
    union_size = len(set_a.union(set_b))
    calculated_size = len(set_a) + len(set_b) - len(set_a.intersection(set_b))
    return union_size == calculated_size

if __name__ == "__main__":
    A = {1, 2, 3, 4}
    B = {3, 4, 5, 6}
    print("PIE formula holds:", verify_pie(A, B))
