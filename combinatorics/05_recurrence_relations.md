# Recurrence Relations

## Quick Overview
A recurrence relation defines each term of a sequence as a function of the preceding terms. Solving recurrences is a fundamental skill in combinatorics and algorithmic complexity.

## Core Theory
- **Linear Homogeneous Recurrence:** A relation of the form $a_n = c_1 a_{n-1} + c_2 a_{n-2} + \dots + c_k a_{n-k}$.
- **Characteristic Equation:** Used to find explicit closed-form solutions for linear recurrences (e.g., Fibonacci sequence: $F_n = F_{n-1} + F_{n-2}$).

## Python Verification
A Python script to compute terms of a linear recurrence (Fibonacci) iteratively:

```python
def compute_fibonacci(n: int) -> int:
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    
    a, b = 0, 1
    for _ in range(2, n + 1):
        a, b = b, a + b
    return b

if __name__ == "__main__":
    print("10th Fibonacci number:", compute_fibonacci(10))
