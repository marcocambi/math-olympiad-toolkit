# Basic Counting Principles: Sum & Product

## Quick Overview
Almost every complex counting problem in combinatorics boils down to two fundamental rules: the Rule of Sum and the Rule of Product.

## Core Rules
- **Rule of Sum:** If a task can be done in $A$ ways or in $B$ ways (and both cannot be done at the same time), then there are $A + B$ total ways to complete the task.
- **Rule of Product:** If a procedure consists of two successive stages, where the first stage has $A$ outcomes and the second has $B$ outcomes, then there are $A \times B$ total outcomes.

## Python Check
A simple script to demonstrate the Rule of Sum and Rule of Product programmatically:

```python
def rule_of_sum(ways_a: int, ways_b: int) -> int:
    return ways_a + ways_b

def rule_of_product(ways_a: int, ways_b: int) -> int:
    return ways_a * ways_b

if __name__ == "__main__":
    # Example: Choosing a shirt from 3 options OR a jacket from 2 options (Mutually exclusive)
    print("Total choices (Rule of Sum):", rule_of_sum(3, 2))
    
    # Example: Choosing an outfit consisting of 3 shirts AND 2 pants (Independent choices)
    print("Total outfits (Rule of Product):", rule_of_product(3, 2))
