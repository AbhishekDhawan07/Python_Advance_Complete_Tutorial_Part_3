# 🐍 Python_Advance_Complete_Tutorial_Part_3

> **A comprehensive, hands-on collection of advanced Python tutorials** — Part 3 focuses entirely on **Recursion & Backtracking**, tackling classic problems that build deep intuition for recursive thinking, string manipulation, combinatorics, and problem decomposition.

---

## 📁 Repository Structure

```
Python_Advance_Complete_Tutorial_Part_3/
├── README.md
├── Tower of Hanoi.py
├── Palindrome Check using Recursion (Two-Pointer Technique).py
├── Remove Character.py
├── Subset Generation(for strings).py
├── Subsequence Generation using Recursion (Include–Exclude Method).py
├── Subsequence Generation using Recursion.py
├── Return Permutations of a string.py
├── Insertion-Based Permutation Algorithm.py
└── Return All Words.py
```

---

## 📌 Table of Contents

1. [About This Repository](#-about-this-repository)
2. [Files Overview](#-files-overview)
3. [Detailed File Breakdown](#-detailed-file-breakdown)
   - [Tower of Hanoi](#1-tower-of-hanoipy)
   - [Palindrome Check using Recursion (Two-Pointer Technique)](#2-palindrome-check-using-recursion-two-pointer-techniquepy)
   - [Remove Character](#3-remove-characterpy)
   - [Subset Generation (for strings)](#4-subset-generationfor-stringspy)
   - [Subsequence Generation using Recursion (Include–Exclude Method)](#5-subsequence-generation-using-recursion-includeexclude-methodpy)
   - [Subsequence Generation using Recursion](#6-subsequence-generation-using-recursionpy)
   - [Return Permutations of a String](#7-return-permutations-of-a-stringpy)
   - [Insertion-Based Permutation Algorithm](#8-insertion-based-permutation-algorithmpy)
   - [Return All Words](#9-return-all-wordspy)
4. [Concepts at a Glance](#-concepts-at-a-glance)
5. [Prerequisites](#-prerequisites)
6. [How to Run](#-how-to-run)
7. [Learning Approach](#-learning-approach)
8. [Who Is This For?](#-who-is-this-for)
9. [Contributing](#-contributing)
10. [License](#-license)

---

## 📖 About This Repository

`Python_Advance_Complete_Tutorial_Part_3` is part of a multi-series Python tutorial repository designed to take learners beyond the basics. Each part targets a specific domain of advanced Python programming.

**Part 3** is dedicated entirely to **Recursion and Backtracking** — the foundation of elegant problem solving in computer science. Every file in this repository isolates one classic recursive problem, implementing it cleanly in Python with a focus on understanding the **call stack**, **base cases**, **recursive leap of faith**, and **backtracking mechanics**.

Unlike other parts, this repository contains **no subfolders** — all `.py` files live directly at the root, making each topic immediately accessible.

---

## 🗂️ Files Overview

| # | File Name | Core Concept | Technique |
|---|-----------|--------------|-----------|
| 1 | `Tower of Hanoi.py` | Classic 3-peg disk transfer puzzle | Recursion |
| 2 | `Palindrome Check using Recursion (Two-Pointer Technique).py` | Check if a string reads the same forwards and backwards using two-pointer recursion | Recursion |
| 3 | `Remove Character.py` | Recursively remove all occurrences of a character from a string | Recursion |
| 4 | `Subset Generation(for strings).py` | Generate all subsets (power set) of a string's characters | Recursion + Backtracking |
| 5 | `Subsequence Generation using Recursion (Include–Exclude Method).py` | Generate all subsequences using explicit include/exclude branching | Recursion + Include–Exclude |
| 6 | `Subsequence Generation using Recursion.py` | Generate all subsequences using the processed/unprocessed string pattern | Recursion |
| 7 | `Return Permutations of a string.py` | Collect and return all permutations as a list | Recursion + Backtracking |
| 8 | `Insertion-Based Permutation Algorithm.py` | Generate permutations by inserting each character at every possible position | Recursion + Insertion |
| 9 | `Return All Words.py` | Generate all possible letter combinations from a phone keypad number and return them | Recursion + Mapping |

---

## 🔍 Detailed File Breakdown

### 1. `Tower of Hanoi.py`

> Moves `n` disks from a source peg to a destination peg using an auxiliary peg, following the rule that no larger disk may rest on a smaller one.

**Key Concepts:**
- Base case: moving 1 disk directly
- Recursive case: move `n-1` disks to auxiliary, move the largest to destination, move `n-1` back
- Demonstrates how recursion elegantly solves problems that appear complex iteratively

**Time Complexity:** O(2ⁿ)  
**Space Complexity:** O(n) — recursion stack depth

---

### 2. `Palindrome Check using Recursion (Two-Pointer Technique).py`

> Recursively checks whether a given string is a palindrome using a two-pointer approach — comparing characters from both ends moving inward.

**Key Concepts:**
- Base case: a string of length 0 or 1 is always a palindrome
- Recursive case: check if the first and last characters match, then recurse on the inner substring
- Mirrors the iterative two-pointer technique but expressed purely through recursion
- Demonstrates recursion as a natural replacement for loop-based logic

**Time Complexity:** O(n)  
**Space Complexity:** O(n) — recursion stack

---

### 3. `Remove Character.py`

> Recursively removes all occurrences of a specified character from a string and returns the cleaned result.

**Key Concepts:**
- Base case: empty string returns empty string
- Recursive case: if the current character matches the target, skip it; otherwise keep it and recurse on the rest
- A clean example of recursion for string filtering without using built-in `replace()`
- Reinforces the processed/unprocessed mental model at a simple level before harder problems

**Example:**  
Input: `"hello"`, remove `'l'` → Output: `"heo"`

**Time Complexity:** O(n)  
**Space Complexity:** O(n) — recursion stack

---

### 4. `Subset Generation(for strings).py`

> Recursively generates **all subsets** (the power set) of a string's characters — every possible combination of characters regardless of order.

**Key Concepts:**
- At each character, two choices exist: include it in the current subset or exclude it
- The total number of subsets for a string of length `n` is `2ⁿ`
- Distinct from subsequences in that subsets focus on combinations, not ordered selections
- Introduces the include/exclude branching pattern that underpins subsequence and backtracking problems

**Example:**  
Input: `"abc"` → Output: `['', 'c', 'b', 'bc', 'a', 'ac', 'ab', 'abc']`

**Time Complexity:** O(2ⁿ)  
**Space Complexity:** O(2ⁿ) — storing all subsets

---

### 5. `Subsequence Generation using Recursion (Include–Exclude Method).py`

> Generates all subsequences of a string using **explicit include/exclude branching** — making the two recursive paths visually and structurally clear.

**Key Concepts:**
- Each recursive call explicitly splits into two branches: one that includes the current character, one that excludes it
- The include/exclude method makes the decision tree transparent and easy to reason about
- Base case: when the string is exhausted, the built-up subsequence is recorded or printed
- Ideal for building intuition before moving to more compact recursive forms

**Example:**  
Input: `"ab"` → Output: `['', 'b', 'a', 'ab']`

**Time Complexity:** O(2ⁿ)  
**Space Complexity:** O(2ⁿ) — storing all subsequences

---

### 6. `Subsequence Generation using Recursion.py`

> Generates all subsequences using the **processed/unprocessed string pattern** — a more compact and elegant recursive formulation.

**Key Concepts:**
- Maintains a `processed` string (built so far) and an `unprocessed` string (remaining characters)
- At each step, the first character of `unprocessed` is either added to `processed` or skipped
- Base case: when `unprocessed` is empty, `processed` is a complete subsequence
- Contrast with File 5 to see how two different recursive structures solve the same problem

**Example:**  
Input: `"abc"` → Prints all 8 subsequences: `""`, `"c"`, `"b"`, `"bc"`, `"a"`, `"ac"`, `"ab"`, `"abc"`

**Time Complexity:** O(2ⁿ)

---

### 7. `Return Permutations of a string.py`

> Recursively generates all permutations of a string and **returns them as a list**.

**Key Concepts:**
- Uses the processed/unprocessed pattern: at each step, every character in `unprocessed` is a candidate for the next position
- Base case: when `unprocessed` is empty, `processed` is a complete permutation — add to result list
- Demonstrates how to convert a "print" recursion into a "return" recursion using list accumulation
- Useful when permutations need to be stored, filtered, or processed further

**Example:**  
Input: `"abc"` → Output: `['abc', 'acb', 'bac', 'bca', 'cab', 'cba']`

**Time Complexity:** O(n × n!)  
**Space Complexity:** O(n!) — storing all permutations

---

### 8. `Insertion-Based Permutation Algorithm.py`

> Generates all permutations by **inserting each new character at every possible position** within already-generated permutations — a fundamentally different approach to File 7.

**Key Concepts:**
- Start with the last character as the only permutation
- For each preceding character, insert it at every possible index (0 to current length) in each existing permutation
- Builds permutations bottom-up rather than top-down
- Excellent contrast with the processed/unprocessed method — same result, different mental model

**Example:**  
Input: `"abc"` → Inserts `'a'` into all positions of each permutation of `"bc"` → Output: `['abc', 'bac', 'bca', 'acb', 'cab', 'cba']`

**Time Complexity:** O(n × n!)  
**Space Complexity:** O(n!) — storing all permutations

---

### 9. `Return All Words.py`

> Given a numeric string (like a phone number), generates **all possible letter combinations** using the standard phone keypad mapping and **returns them as a list**.

**Key Concepts:**
- Maps each digit to its corresponding letters (e.g., `2 → ABC`, `3 → DEF`, ..., `9 → WXYZ`)
- Recursively picks one letter per digit and recurses on the remaining digits
- Base case: when all digits are consumed, the built word is added to the result list
- Classic application of recursion with a lookup mapping

**Keypad Mapping:**
```
2 → ABC    3 → DEF    4 → GHI
5 → JKL    6 → MNO    7 → PQRS
8 → TUV    9 → WXYZ
```

**Example:**  
Input: `"23"` → Output: `['AD', 'AE', 'AF', 'BD', 'BE', 'BF', 'CD', 'CE', 'CF']`

**Time Complexity:** O(4ⁿ) where n = length of input  
**Space Complexity:** O(n) — recursion depth

---

## 🧩 Concepts at a Glance

| Concept | Files Demonstrating It |
|---------|------------------------|
| Basic Recursion & Base Cases | `Tower of Hanoi.py`, `Palindrome Check using Recursion (Two-Pointer Technique).py` |
| String Filtering via Recursion | `Remove Character.py` |
| Include / Exclude Pattern | `Subset Generation(for strings).py`, `Subsequence Generation using Recursion (Include–Exclude Method).py` |
| Processed / Unprocessed Pattern | `Subsequence Generation using Recursion.py`, `Return Permutations of a string.py` |
| Insertion-Based Recursion | `Insertion-Based Permutation Algorithm.py` |
| Recursion with Lookup / Mapping | `Return All Words.py` |
| Print vs Return Recursion | Files 5 vs 6 (subsequences), Files 7 vs 8 (permutations) |

---

## ✅ Prerequisites

- **Python 3.7+**
- A basic understanding of functions, strings, and lists in Python
- No third-party libraries required — all files use **Python standard library only**

---

## ▶️ How to Run

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/Python_Advance_Complete_Tutorial_Part_3.git
   cd Python_Advance_Complete_Tutorial_Part_3
   ```

2. **Run any file directly:**

   ```bash
   python "Tower of Hanoi.py"
   python "Palindrome Check using Recursion (Two-Pointer Technique).py"
   python "Remove Character.py"
   python "Subset Generation(for strings).py"
   python "Return All Words.py"
   # ... and so on
   ```

3. **Modify the input** at the bottom of each file to experiment with different test cases.

> 💡 **Tip:** Open files in any editor (VS Code, PyCharm, or even IDLE) and step through them with a debugger to visualize the call stack — it makes the recursion click instantly.

---

## 🧠 Learning Approach

This repository follows a **deliberate progression** through recursion concepts:

```
Simple Recursion          →   Tower of Hanoi, Palindrome Check (Two-Pointer)
        ↓
String Filtering          →   Remove Character
        ↓
Include / Exclude         →   Subset Generation → Subsequence Generation (Include–Exclude)
        ↓
Processed / Unprocessed   →   Subsequence Generation → Return Permutations
        ↓
Insertion-Based           →   Insertion-Based Permutation Algorithm
        ↓
Recursion + Mapping       →   Return All Words
```

Each file builds on the mental model established by the previous one. It is recommended to study them **in order**.

---

## 🎯 Who Is This For?

- **Students** learning recursion and backtracking for the first time
- **Developers** preparing for coding interviews (LeetCode / HackerRank style problems)
- **Python learners** who want to move beyond loops and understand the call stack
- **Anyone** revisiting CS fundamentals with clean, readable Python code

---

## 🤝 Contributing

Contributions are welcome and greatly appreciated! Whether it's a new recursive problem, an alternative approach to an existing one, or a clearer explanation — every improvement helps the community.

### How to Contribute

1. **Fork the repository**

   Click the **Fork** button at the top-right of the repository page.

2. **Clone your fork locally**

   ```bash
   git clone https://github.com/your-username/Python_Advance_Complete_Tutorial_Part_3.git
   cd Python_Advance_Complete_Tutorial_Part_3
   ```

3. **Create a new branch** for your changes

   ```bash
   git checkout -b feature/add-sudoku-solver
   ```

4. **Add or edit your `.py` file**

5. **Commit with a clear message**

   ```bash
   git add .
   git commit -m "Add Sudoku Solver using backtracking"
   ```

6. **Push to your fork**

   ```bash
   git push origin feature/add-sudoku-solver
   ```

7. **Open a Pull Request** on the original repository

---

### 📋 Contribution Guidelines

- **Name files descriptively** — the filename alone should convey the problem (e.g., `N-Queens Problem.py`)
- **Include a docstring** at the top of the file explaining what the problem does
- **Provide at least one test call** at the bottom of the file with a printed result
- **Follow the existing code style** — clean, commented, readable Python
- **Do not use external libraries** — keep everything in the Python standard library

---

### 💡 Ideas for Contributions

- N-Queens Problem
- Rat in a Maze
- Sudoku Solver
- Subset Sum Problem
- Generate Balanced Parentheses
- Flood Fill Algorithm
- Knight's Tour Problem

---

### 🐛 Reporting Issues

Found a bug or an incorrect output? Please [open an issue](https://github.com/your-username/Python_Advance_Complete_Tutorial_Part_3/issues) with:

- The **filename** where the issue occurs
- A **clear description** of what is wrong
- The **input used** and the **expected vs actual output**

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute for educational purposes.

---

> 💡 **Challenge yourself:** After studying each file, close it and try to rewrite it from scratch. Recursion is a skill that only clicks through repeated practice — not just reading!
