# Part 3 — `recursion_examples.py`

## Recursion: Linear vs Branching (the silent killer) 

### Linear recursion

```python
def sum_n(n):
    if n == 0:
        return 0
    return n + sum_n(n - 1)
```

Each call reduces input by 1.

Calls = `n`
Time = **O(n)**

Recursion does not automatically mean exponential.

---

### Branching recursion (this is where people lie)

```python
def fib(n):
    if n <= 1:
        return n
    return fib(n-1) + fib(n-2)
```

Each call spawns **two more calls**.

Textual call explosion:

```
fib(5)
├─ fib(4)
│  ├─ fib(3)
│  │  ├─ fib(2)
│  │  └─ fib(1)
│  └─ fib(2)
└─ fib(3)
```

Work repeats.
Growth explodes.

Time complexity → **O(2ⁿ)**

This is not inefficient.
It is **unacceptable**.

Memoization collapses this back to linear — that’s optimization through structure, not hacks.

---

### Key recursion rule

Ask **one question**:

> Does each call create more than one meaningful subproblem?

If yes → exponential risk.
If no → linear or logarithmic.

---

