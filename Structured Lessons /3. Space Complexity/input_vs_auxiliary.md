Part 1 — input_vs_auxiliary.py
Separating input from extra memory
Example 1: No extra space
def sum_array(arr):
    total = 0
    for x in arr:
        total += x
    return total


Input space → O(n) (ignored)

Auxiliary space → O(1)

Only one variable (total) is created.

This is constant auxiliary space, even though input is large.

Example 2: Extra array created
def double_array(arr):
    res = []
    for x in arr:
        res.append(x * 2)
    return res


Input space → O(n)

Auxiliary space → O(n)

You created a new array that grows with input.

This distinction matters constantly in interviews.

Rule of thumb

Ask yourself:

Did I allocate memory proportional to input?

If yes → O(n)
If no → O(1)

Simple. Brutal. Effective.
