# Permutations & Combinations

## Quick Overview
Counting problems form the bedrock of combinatorics. The main question is always: *does order matter?* If yes, use permutations; if no, use combinations.

## Core Formulas
- **Factorial:** $n! = n \times (n-1) \times \dots \times 1$
- **Combinations (Order doesn't matter):** 
  $$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$

## Python Check
A simple loop-based function to calculate factorials without advanced built-in shortcuts:

```python
def compute_factorial(n: int) -> int:
    result = 1
    for i in range(1, n + 1):
        result = result * i
    return result

if __name__ == "__main__":
    print("Factorial of 5 is:", compute_factorial(5))
