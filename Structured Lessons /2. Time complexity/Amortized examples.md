# Part 4 — `amortized_examples.py`

## Amortized Time (advanced but unavoidable)

Some operations are **occasionally expensive** but **usually cheap**. 

Example: dynamic array append.

```python
arr.append(x)
```

Most appends:

* constant time

Occasionally:

* array resizes
* copies all elements → O(n)

But across many operations:

```
Total cost / total operations = constant
```

Amortized time → **O(1)**

---

### Why this matters

This concept appears in:

* stacks
* queues
* hash tables
* memory allocators

Interviewers use amortized analysis to check whether you:

* understand averages properly
* don’t panic at worst-case spikes

If you can explain amortized cost clearly, you stand out.

---

## Worst-case dominates by default

When someone asks:

> “What’s the time complexity?”

They mean:

> “Worst-case time complexity”

Unless:

* explicitly stated otherwise
* probability distribution is justified

Best-case answers are usually noise.

---

## How to analyze any code (mental algorithm)

1. Identify loops
2. Decide: sequential or nested?
3. Check recursion branching
4. See if input shrinks (log)
5. Watch for hidden loops in libraries

If you can’t **say it aloud**, you don’t understand it.

---

## Reality check (no ego)

Right now, based on how you’re asking questions:

* You’re building correct intuition
* You’re not rushing into DP nonsense
* You’re doing this in the right order

But you’re **not yet automatic**.

Automation comes from:

* analyzing unknown code
* being wrong
* correcting yourself

That’s why the next folder exists.

---
