# 02. Polynomials and Vieta's Formulas

## 1. Division Algorithm for Polynomials
Given polynomials $P(x)$ and $D(x)$ with $\deg(D) \le \deg(P)$, there exist unique polynomials $Q(x)$ (quotient) and $R(x)$ (remainder) such that:
$$P(x) = D(x) \cdot Q(x) + R(x)$$
where either $R(x) = 0$ or $\deg(R) < \deg(D)$.

### Remainder Theorem:
The remainder of the division of a polynomial $P(x)$ by $(x - c)$ is equal to $P(c)$.
* **Factor Theorem:** $(x - c)$ is a factor of $P(x)$ if and only if $P(c) = 0$.

---

## 2. Vieta's Formulas
For a monic polynomial of degree $n$:
$$P(x) = x^n + a_{n-1}x^{n-1} + a_{n-2}x^{n-2} + \dots + a_1x + a_0 = (x - r_1)(x - r_2)\dots(x - r_n)$$
The relationship between the coefficients $a_i$ and the roots $r_1, r_2, \dots, r_n$ is given by:
* **Sum of roots:** $r_1 + r_2 + \dots + r_n = -a_{n-1}$
* **Sum of products taken two at a time:** $\sum_{i < j} r_i r_j = a_{n-2}$
* **Product of roots:** $r_1 r_2 \dots r_n = (-1)^n a_0$

### Special Case (Quadratic $ax^2 + bx + c = 0$ with roots $r_1, r_2$):
* $r_1 + r_2 = -\frac{b}{a}$
* $r_1 r_2 = \frac{c}{a}$

---

## 3. Contest Techniques & Tricks
* **Rational Root Theorem:** If a polynomial with integer coefficients has a rational root $p/q$ (in lowest terms), then $p$ divides the constant term $a_0$ and $q$ divides the leading coefficient $a_n$.
* **Symmetric Sums:** Expressing complex symmetric expressions of roots (like $r_1^2 + r_2^2 + r_3^2$) directly in terms of coefficients without finding the roots explicitly using identities like:
  $$\sum r_i^2 = \left(\sum r_i\right)^2 - 2\sum_{i < j} r_i r_j$$
