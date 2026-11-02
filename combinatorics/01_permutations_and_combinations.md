# Permutations and Combinations

## Quick Overview

Counting problems form the bedrock of combinatorics. The main question is always: does order matter? If yes, use permutations; if no, use combinations.

## Core Formulas

- **Factorial:** 
  $$n! = n \times (n-1) \times \dots \times 1$$

- **Combinations (Order doesn't matter):** 
  $$\binom{n}{k} = \frac{n!}{k!(n-k)!}$$

## Python Check

Funzione per il calcolo del fattoriale:

```python
def compute_factorial(n: int) -> int:
    result = 1
    for i in range(1, n + 1):
        result *= i
    return result
