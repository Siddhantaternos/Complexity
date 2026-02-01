# `04_code_to_complexity/` — Extracting complexity from *unknown code*

Knowing definitions is useless if you can’t analyze **code you’ve never seen before**.

Interviewers don’t care whether you know Big-O symbols.
They care whether you can **read unfamiliar logic and predict consequences**.

This folder exists to build that muscle.

---

## The core skill (this is the real goal)

When you see code, you should be able to answer — calmly and confidently:

> How does time grow?
> How does space grow?
> Why?

Not guessing.
Not vibes.
Reasoning.

---

## The only correct analysis order (never break this)

Always analyze in this exact sequence:

```
1) Control flow (loops / recursion)
2) Input dependency
3) Nesting vs sequencing
4) Hidden work
5) Data structure behavior
```

If you skip steps, you hallucinate complexity.

---

# Part 1 — `analyze_given_code.md`

## A deterministic method (no guessing)

### Step 1: Identify the dominant input

Ask:

* What variable represents input size?
* What actually grows?

Example:

```python
def solve(arr, k):
```

Here, `arr` → input size `n`
Ignore constants like `k` unless stated otherwise.

---

### Step 2: Count loops and recursion

Example:

```python
for i in range(n):
    process(i)
```

Time → O(n)

Now this:

```python
for i in range(n):
    for j in range(n):
        process(i, j)
```

Time → O(n²)

Do not think. Just apply the rule.

---

### Step 3: Sequential vs nested (again, because people mess this up)

```python
for i in range(n):
    pass

for j in range(n):
    pass
```

O(n + n) → O(n)

But:

```python
for i in range(n):
    for j in range(m):
        pass
```

O(n × m)

If `m = n` → O(n²)
If `m` is constant → O(n)

---

### Step 4: Look for shrinking input (log behavior)

```python
while n > 1:
    n = n // 2
```

Each iteration halves input.

Time → O(log n)

This overrides intuition.
No halving → no logarithm.

---

### Step 5: Analyze recursion properly

Ask two questions:

1. How many recursive calls per invocation?
2. How fast does input shrink?

If:

* one call → linear or log
* two calls → exponential risk

Never guess. Draw it.

---

## Textual recursion tree (do this mentally)

For:

```python
f(n) = f(n-1) + f(n-1)
```

Tree shape:

```
        n
      /   \
   n-1     n-1
   / \     / \
```

Explosion → O(2ⁿ)

For:

```python
f(n) = f(n/2)
```

Tree shape:

```
n
|
n/2
|
n/4
```

Depth → log n

---

# Part 2 — `brute_vs_optimized.py`

## Same problem, different growth

This section teaches **contrast**, not code.

### Brute force

```python
for i in range(n):
    for j in range(n):
        if arr[i] == arr[j]:
            return True
```

Time → O(n²)
Space → O(1)

---

### Optimized with extra space

```python
seen = set()
for x in arr:
    if x in seen:
        return True
    seen.add(x)
```

Time → O(n)
Space → O(n)

This is the **core engineering trade-off**.

Interviewers want to hear:

* what improved
* what worsened
* why the trade makes sense

---

## The real lesson here

Optimization is never free.

Every improvement costs:

* memory
* complexity
* readability
* maintainability

Good engineers choose consciously.

---

# Part 3 — `complexity_annotations.py`

## Annotating code line-by-line (advanced habit)

You should be able to annotate like this:

```python
for i in range(n):          # O(n)
    for j in range(i):      # O(n)
        print(i, j)         # O(1)
```

Total → O(n²)

Annotations force honesty.
If you can’t annotate, you don’t understand.

---

## Hidden complexity traps (read carefully)

### Library calls

```python
sorted(arr)
```

Time → O(n log n)
Space → O(n)

Never assume library calls are free.

---

### Python slicing

```python
new_arr = arr[:]
```

Time → O(n)
Space → O(n)

Looks harmless. Isn’t.

---

### String concatenation

```python
s = ""
for c in chars:
    s += c
```

Time → O(n²)
Space → O(n)

One of the most common silent failures.

---

## Interview behavior (this matters)

When unsure, say:

> “Let me walk through it step by step.”

Silence while thinking is fine.
Guessing confidently is not.

---

## Reality check (brutal but fair)

At this point:

* You know definitions
* You understand growth
* You’re learning extraction

This is where most people quit — because it’s uncomfortable.

If you push through this folder, you stop being average.

---
