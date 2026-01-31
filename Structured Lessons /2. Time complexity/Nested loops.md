# Part 2 — `nested_loops.py`

## Sequential vs Nested Growth (where people screw up)

### Sequential loops → addition

```python
for i in range(n):
    pass

for j in range(n):
    pass
```

Operations:

```
O(n) + O(n) = O(2n) → O(n)
```

Constants die. Growth survives.

---

### Nested loops → multiplication

```python
for i in range(n):
    for j in range(n):
        pass
```

Operations:

```
n × n = n² → O(n²)
```

This explodes faster than people expect.

Textual intuition:

```
n = 1,000   → 1,000,000 ops
n = 10,000  → 100,000,000 ops
```

Quadratic growth doesn’t look dangerous early.
It kills you late.

---

### Uneven nesting

```python
for i in range(n):
    for j in range(10):
        pass
```

Inner loop is constant.

```
O(n × 10) → O(n)
```

Not every nested loop is quadratic.
Only **input-dependent nesting** multiplies.

---

