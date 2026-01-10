# ⏱️ Time Complexity

Time complexity describes how the **runtime of an algorithm grows** as input size increases.

It does not measure actual execution time.
It measures **growth behavior**.

## Common Time Complexities

| Notation | Meaning |
|--------|--------|
| O(1) | Constant time |
| O(log n) | Logarithmic |
| O(n) | Linear |
| O(n log n) | Efficient sorting |
| O(n²) | Nested loops |
| O(2ⁿ) | Exponential |
| O(n!) | Factorial |

## Rules
- Ignore constants
- Drop lower-order terms
- Nested loops multiply
- Sequential code adds

Worst-case complexity is the default in interviews.


# 🧠 Space Complexity

Space complexity measures the **extra memory** used by an algorithm.

Includes:
- Variables
- Data structures
- Recursion stack

## Common Space Complexities

| Space | Meaning |
|----|----|
| O(1) | Constant extra memory |
| O(n) | Linear memory |
| O(log n) | Recursive stack |
| O(n²) | Matrix or table |

## In-Place Algorithms
Algorithms that use constant extra space.
Example: two-pointer techniques.


# ⚖️ Time vs Space Trade-Offs

Fast algorithms often use more memory.
Memory-efficient algorithms often take more time.

Examples:
- Hash tables: faster lookups, more memory
- Sorting in-place: less memory, more logic
- Caching: faster response, higher space cost

Good engineers choose based on constraints.


# 🌍 Real-World Resource Consumption

## Power Consumption
Impacted by:
- CPU usage duration
- Cache misses
- Infinite loops

Important for:
- Mobile devices
- Data centers

## Network Consumption
Cost of transferring data.
Critical for:
- APIs
- Distributed systems
- Cloud services

Optimization:
- Reduce payload size
- Cache responses
- Batch requests

## CPU Registers & Cache
Registers are fastest memory.
Cache locality heavily affects performance.
Mostly handled by compilers, but algorithm design still matters.


# 🔍 Complexity in LeetCode Problems

- Two Sum (Brute Force): O(n²)
- Two Sum (Hash Map): O(n)
- Binary Search: O(log n)
- Nested loops → think multiplication
- Recursion → include stack space

Always explain **why**, not just the answer.
