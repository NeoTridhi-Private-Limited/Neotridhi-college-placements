# Module 3: Technical Training: preview

> This page is a free preview of the NeoTridhi course. [See how to get the full module](#get-the-full-module).

[Back to the course home](../README.md)

---

## What this module covers

This module builds the technical base that campus tests and technical interviews check: programming in Python (with C and Java shown
side by side), OOP, complexity, data structures, algorithms, DBMS and SQL, plus interview-ready notes on operating systems, computer
networks and Git. A second part adds a 150-question technical MCQ bank, a Java and C++ quick reference, cloud and DevOps basics,
cybersecurity basics and 20 SQL practice problems. Every program was run with Python 3.13 before the notes were written, so the
outputs shown are the real outputs. In all there are 19 topics and 338 practice questions with worked answers.

## Topics in the full module

| # | Topic | Access |
|---|---|---|
| 01 | Programming fundamentals | 🔒 Locked |
| 02 | Object-oriented programming | 🔒 Locked |
| 03 | Time and space complexity | 🔒 Locked |
| 04 | Linear data structures | Preview below |
| 05 | Trees, heaps and graphs | 🔒 Locked |
| 06 | Searching, sorting and techniques | 🔒 Locked |
| 07 | Recursion, greedy and DP | 🔒 Locked |
| 08 | DBMS concepts | 🔒 Locked |
| 09 | SQL from zero to interview | 🔒 Locked |
| 10 | Operating systems basics | 🔒 Locked |
| 11 | Computer networks basics | 🔒 Locked |
| 12 | Git basics | 🔒 Locked |
| 13 | Technical MCQ bank, part 1 | 🔒 Locked |
| 14 | Technical MCQ bank, part 2 | 🔒 Locked |
| 15 | Technical MCQ bank, part 3 | 🔒 Locked |
| 16 | Java and C++ quick reference | 🔒 Locked |
| 17 | Cloud and DevOps basics | 🔒 Locked |
| 18 | Cybersecurity basics | 🔒 Locked |
| 19 | SQL practice problems | 🔒 Locked |

## Preview: Linear data structures

### The idea in plain words

A **data structure** is a way of arranging data so that the jobs you do most often are fast.

| Structure | Real-life picture | Fast at | Slow at |
|---|---|---|---|
| **Array / list** | Numbered seats in a bus | Jump to seat 23 directly | Squeezing a new person into seat 5 (everyone shifts) |
| **Linked list** | A treasure hunt: each clue tells where the next one is | Adding a clue in the middle (if you are already there) | Finding clue number 23 (follow all clues) |
| **Stack** (LIFO: last in, first out) | A pile of plates in the mess | Taking the top plate | Getting the bottom plate |
| **Queue** (FIFO: first in, first out) | The line at a railway ticket counter | Serving the front, joining at the back | Anything in the middle |
| **Hash table / dictionary** | The college locker room: roll number tells you the locker directly | Find by key in about one step | Keeping things in sorted order |

### Example 3 (medium): stack for balanced brackets

Push every opening bracket. On a closing bracket, the top must be its partner. At the end the stack must be empty.

```python
def balanced(expr):
    pairs = {')': '(', ']': '[', '}': '{'}
    st = []
    for ch in expr:
        if ch in "([{":
            st.append(ch)
        elif ch in pairs:
            if not st or st.pop() != pairs[ch]:
                return False
    return not st
```

Trace for `([)]`: push `(`, push `[`, see `)`, pop gives `[`, which is not `(`, so **False**.

```
3. balanced: [('{[()]}', True), ('([)]', False), ('((', False), ('a*(b+c)', True)]
   next greater of [4, 5, 2, 25, 7]: [5, 25, 25, -1, -1]
   postfix '2 3 4 * +' = 14 | '5 1 2 + 4 * + 3 -' = 14
```

**Next greater element** uses a *monotonic stack*: keep indexes whose answer is not yet known; when a bigger number comes, it is the answer for all smaller ones on top. Each index is pushed and popped once, so **O(n)**, not O(n^2).

### Example 5 (medium-hard): hashing, two-sum in O(n)

```python
def two_sum(nums, target):
    seen = {}                          # value -> index
    for i, x in enumerate(nums):
        if target - x in seen:         # O(1) average lookup
            return (seen[target - x], i)
        seen[x] = i
```

```
5. freq: {'CSE': 3, 'ECE': 2, 'MBA': 1} | Counter most common: [('CSE', 3)]
   two_sum([2, 7, 11, 15], 9): (0, 1) | target 26: (2, 3)
   first non-repeating in 'swiss': w | in 'aabb': None
   anagram groups: [['eat', 'tea', 'ate'], ['tan', 'nat'], ['bat']]
   toy buckets (size 7): {'CSE': 2, 'ECE': 2, 'MBA': 5, 'MCA': 6}
```

### Try 3 questions (solutions open)

**1.** An array holds 1..6 with one number missing: `[1, 2, 4, 5, 6]`. Find it in O(n) time and O(1) space.

<details><summary>Solution</summary>

**3**. Expected sum 6 x 7 / 2 = 21; actual 18; missing 21 - 18 = 3. (XOR also works and never overflows in C/Java.)

</details>

**2.** Check whether "erbottlewat" is a rotation of "waterbottle" with a single substring check.

<details><summary>Solution</summary>

**True**. If B is a rotation of A (same length), B is a substring of A + A.

</details>

**3.** Scanning `[4, 9, 2, 7, 9, 4]` from left to right, which element is the first to be seen a second time?

<details><summary>Solution</summary>

**9**. Keep a set of seen values; 9 is the first value found already in the set (at index 4). Note that 4 appears first in the list, but its repeat comes later (index 5).

</details>

---

## Get the full module

The complete module, along with all 7 modules of the course, company chapters and AI mock interviews on **NeoHireAI**, is available
to subscribing colleges and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>© 2026 NeoTridhi Private Limited.</sub>
