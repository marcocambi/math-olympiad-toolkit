# Prime Numbers & Prime Factorization

## Quick Overview
Every integer greater than 1 is either a prime number or a unique product of primes. Prime factorization is the cornerstone of number theory problems in contests.

## Core Concepts
- **Prime Number:** An integer greater than 1 that has no positive divisors other than 1 and itself.
- **Fundamental Theorem of Arithmetic:** Every integer greater than 1 can be uniquely represented as a product of prime numbers.

## Python Check
A simple script using basic loops to find all prime factors of a given number:

```python
def find_prime_factors(n: int) -> list[int]:
    factors = []
    divisor = 2
    while n > 1:
        while n % divisor == 0:
            factors.append(divisor)
            n = n // divisor
        divisor += 1
    return factors

if __name__ == "__main__":
    number = 84
    print(f"Prime factors of {number}:", find_prime_factors(number))
