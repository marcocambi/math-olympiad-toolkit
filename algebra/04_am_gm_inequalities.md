# AM-GM Inequality & Contest Optimization

## Quick Overview
Le disuguaglianze sono il pilastro dell'algebra olimpica avanzata. La disuguaglianza tra media aritmetica e geometrica (AM-GM) è lo strumento principale per risolvere problemi di massimo e minimo senza ricorrere alle derivate.

## Core Theory
- **AM-GM per $n$ variabili non negative:**
  $$\frac{x_1 + x_2 + \dots + x_n}{n} \ge \sqrt[n]{x_1 x_2 \dots x_n}$$
- L'uguaglianza vale se e solo se $x_1 = x_2 = \dots = x_n$.

## Python Verification
Un semplice script per verificare la disuguaglianza AM-GM con valori casuali:

```python
import random

def verify_am_gm() -> bool:
    values = [random.uniform(1.0, 10.0) for _ in range(3)]
    am = sum(values) / len(values)
    gm = (values[0] * values[1] * values[2]) ** (1 / 3)
    return am >= gm

if __name__ == "__main__":
    print("AM >= GM holds:", verify_am_gm())
