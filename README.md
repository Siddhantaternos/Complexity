# ⚙️ Algorithm Complexity | Structured Learning Notes

This repository is a **structured, execution-focused guide to mastering algorithm complexity**, built to develop **interview-ready intuition**, not memorized definitions. The goal is to understand **how time and space grow as input scales**, and to reason confidently about performance trade-offs in real code.

This repo is designed to be **visited repeatedly**: to check progress, refresh intuition, and identify the *next concept to master*.

---

## What this repository teaches

* What complexity *actually measures* (beyond Big-O symbols)
* How to analyze **time and space** from real code
* How recursion, loops, and data structures affect growth
* How to reason about **trade-offs** in interviews and real systems

---

## Learning Roadmap (follow top → bottom)

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

You should not skip steps. Each layer depends on the previous one.

---

## Repository Structure

```
Complexity/
│
├── 01_intuition/                                           # What complexity means & why it matters
│   ├── why_complexity_matters.md
│   └── growth_visuals.md
│
├── 02_time_complexity/                                     # How runtime grows
│   ├── constant_log_linear.py
│   ├── nested_loops.py
│   ├── recursion_examples.py
│   └── amortized_examples.py
│
├── 03_space_complexity/                                    # How memory grows
│   ├── input_vs_auxiliary.py
│   ├── recursion_stack.py
│   └── in_place_vs_extra_space.py
│
├── 04_code_to_complexity/                                  # Analyze unknown code
│   ├── analyze_given_code.md
│   ├── brute_vs_optimized.py
│   └── complexity_annotations.py
│
├── 05_tradeoffs/                                           # Decision-making & interviews
│   ├── time_vs_space.md
│   └── real_interview_questions.md
│
└── README.md
```

---

## How to use this repo

* Start from **01_intuition**
* Do not move forward until you can **explain the topic in words**
* Every example should answer:
  **“What grows when input grows?”**
* Use this repo alongside problem-solving (LeetCode, DSA)


![Big O Time Complexity Chart]("C:\Users\Siddhant\Desktop\Big_O_Cheatsheet.png")


---

## Progress check (self-evaluation)

* If you recognize Big-O → you are early
* If you can explain complexity → you are learning
* If you can predict it from code → you are interview-ready

Strings, arrays, and advanced patterns should only be explored **after** solid complexity intuition.

---

## Purpose

This repository exists to build a **mental framework** that makes future topics (DSA, SQL performance, system design) easier and faster to learn.

Master this once. Everything else compounds.

---
