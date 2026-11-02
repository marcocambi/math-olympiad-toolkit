# The Pigeonhole Principle

## Quick Overview
The Pigeonhole Principle is one of the most elegant and deceptively simple tools in combinatorics. It allows us to prove that a certain configuration or overlap exists without having to construct it explicitly.

## Core Concept
- **Basic Form:** If $n$ items are put into $m$ containers, and $n > m$, then at least one container must contain more than one item.
- **Generalized Form:** If $n$ items are put into $m$ containers, at least one container must contain at least $\lceil n/m \rceil$ items.

## Python Check
A simple script to demonstrate the pigeonhole principle by grouping numbers based on their remainders:

```python
def check_pigeonhole(numbers: list[int], m: int) -> tuple[int, list[int]]:
    buckets = {}
    for num in numbers:
        rem = num % m
        if rem not in buckets:
            buckets[rem] = []
        buckets[rem].append(num)
    
    for rem, group in buckets.items():
        if len(group) > 1:
            return rem, group
    return None, []

if __name__ == "__main__":
    nums = [12, 17, 22, 27, 3]
    rem, group = check_pigeonhole(nums, 5)
    print(f"Remainder {rem} has multiple elements: {group}")
