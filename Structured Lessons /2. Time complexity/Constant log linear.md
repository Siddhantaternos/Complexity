# How runtime *actually* grows

Time complexity is not an academic concept. It’s a **survival tool**.
It tells you whether your code lives long enough to matter.

At scale, correctness is assumed.
Only **growth behavior** decides whether something ships or dies.

---

## First principle (non-negotiable)

Time complexity answers **one question only**: 

> As input size `n` grows, how many **operations** does the algorithm perform?

Not seconds.
Not milliseconds.
**Operations.**

An operation is roughly:

* a comparison
* an assignment
* arithmetic
* a function call

We never count them exactly.
We track **how they grow relative to input**.

That’s it.

---

## The hierarchy you must *feel*, not memorize

```
O(1)        → stable, input irrelevant
O(log n)    → calm growth
O(n)        → honest growth
O(n log n)  → efficient but real
O(n²)       → dangerous
O(2ⁿ)       → catastrophic
O(n!)       → instant failure
```

This is not a list.
It’s a **slope comparison**.

Your intuition should react before your brain calculates.

---

# Part 1 — `constant_log_linear.py`

## Constant, Logarithmic, Linear Growth

### O(1): Constant Time

```python
def get_first(arr):
    return arr[0]
```

Why O(1)?

* One operation
* No dependency on input size

Whether `arr` has 10 elements or 10 million, the work is identical.

⚠️ Important correction:
O(1) does **not** mean “fast”.
It means **unchanging with input**.

A slow constant is still O(1).

---

### O(log n): Logarithmic Time

Logarithmic growth appears when the input **shrinks every step**.

Classic example: binary search.

Each iteration:

* discards half the data
* makes progress aggressively

Mental model:

```
n
↓
n/2
↓
n/4
↓
n/8
↓
...
```

This is why:

* binary search
* balanced trees
* divide-and-conquer

are considered scalable.

Logarithmic time feels calm because growth slows as input grows.

---

### O(n): Linear Time

```python
def print_all(arr):
    for x in arr:
        print(x)
```

Each element is touched once.

If input doubles → work doubles.

This is the **baseline of honesty** in algorithms.

Most real systems are built on linear passes.

Linear isn’t bad.
Unnecessary quadratic is.

---

