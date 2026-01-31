# ⚙️ Algorithm Complexity | Structured Learning Notes

This repository is a **practical, execution focused guide to mastering algorithm complexity**, designed to develop **interview ready intuition**, not memorized definitions. The goal is to understand **how time and space grow as input scales**, and reason confidently about performance trade offs in real code.

It’s meant to be **visited repeatedly**: to check progress, refresh intuition, and identify the *next concept to master*.

---

## What You’ll Learn

* What complexity *actually measures* (beyond Big-O symbols)
* How to analyze **time and space** from real code
* How recursion, loops, and data structures affect growth
* How to reason about **trade-offs** in interviews and production systems

---

## Learning Roadmap (Top → Bottom)

```
01. Intuition & Meaning
    ↓
02. Time Complexity
    ↓
03. Space Complexity
    ↓
04. Code → Complexity Mapping
    ↓
05. Trade-offs & Interview Reasoning
```

Each step builds on the previous one **don’t skip**.

---

## Repository Structure

```
Complexity/
│
├── 01_intuition/                   # What complexity means & why it matters
│   ├── why_complexity_matters.md
│   └── growth_visuals.md
│
├── 02_time_complexity/             # How runtime grows
│   ├── constant_log_linear.py
│   ├── nested_loops.py
│   ├── recursion_examples.py
│   └── amortized_examples.py
│
├── 03_space_complexity/            # How memory grows
│   ├── input_vs_auxiliary.py
│   ├── recursion_stack.py
│   └── in_place_vs_extra_space.py
│
├── 04_code_to_complexity/          # Analyze unknown code
│   ├── analyze_given_code.md
│   ├── brute_vs_optimized.py
│   └── complexity_annotations.py
│
├── 05_tradeoffs/                   # Decision-making & interviews
│   ├── time_vs_space.md
│   └── real_interview_questions.md
│
└── README.md
```

---

## How to Use This Repository

* Start with **01_intuition**
* Don’t move forward until you can **explain the topic in your own words**
* Every example should answer: **“What grows when input grows?”**
* Use this alongside problem solving platforms (LeetCode, DSA practice)

---

## Visual Guide to Complexity

```
Operations
^
|                   /  -> O(2^n)   < Horrible >
|                  /
|                 /
|                /  -> O(n^2)   < Horrible >
|               /
|              /
|             /         
|            /
|           /  -> O(n log n) < Bad >
|          /
|         /
|        /
|       /
|      /   -> O(n)  < Fair >
|     /
|    /
|   /   -> O(log n)  < Good >
|  /
| /   -> O(1)  < Best >
+--------------------------------------------------> Elements
```

---

## Progress Check (Self-Evaluation)

* Recognize Big-O → **Early**
* Explain complexity in words → **Learning**
* Predict complexity from code → **Interview-ready**

Advanced topics (strings, arrays, patterns) should be tackled **only after** building solid complexity intuition.

---

## Purpose

This repository exists to build a **mental framework** that makes future topics DSA, SQL performance, system design faster and easier to learn.

Master complexity once. Everything else compounds.

---
