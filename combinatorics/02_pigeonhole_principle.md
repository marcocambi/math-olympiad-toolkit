# The Pigeonhole Principle

## Quick Overview
If you have more pigeons than pigeonholes, at least one pigeonhole must contain more than one pigeon. It is a powerful tool to prove existence without constructing explicit configurations.

## Core Concept
- **Generalized Form:** If n items are put into m containers, at least one container must contain at least ceil(n / m) items.

## Python Check
A simple script to demonstrate the generalized pigeonhole principle:

```python
import math

def check_pigeonhole(items: int, boxes: int) -> int:
    if boxes <= 0:
        raise ValueError("Boxes must be greater than zero.")
    return math.ceil(items / boxes)


if __name__ == "__main__":
    items_cnt = 10
    boxes_cnt = 3
    min_items = check_pigeonhole(items_cnt, boxes_cnt)
    print(f"Min items in one box ({items_cnt} items, {boxes_cnt} boxes):", min_items)
