# Module 4: Coding Practice, Mock Tests and Technical Assessments: preview

> This page is a free preview of the NeoTridhi course. [See how to get the full module](#get-the-full-module).

[Back to the course home](../README.md)

---

## What this module covers

This module is where you practise. Module 3 taught programming, data structures, DBMS, OS and networks; here you use them the way an
online test asks: under time pressure, with exact input and output formats and hidden test cases. It has 100 original coding problems
(40 easy, 40 medium, 20 hard, grouped by 22 patterns), each with a statement, examples, constraints, hints and a full Python solution
that was run against at least 3 test cases. It also has 8 full mock technical assessments of 90 minutes each, with answer keys and
explanations, and a guide to what mass recruiters and product companies usually ask in their coding rounds.

## Topics in the full module

| # | Topic | Access |
|---|---|---|
| 01 | How to read a problem and write code under time pressure | 🔒 Locked |
| 02 | Easy problems, part 1: math and strings (E01-E08) | Preview below |
| 03 | Easy problems, part 2: arrays, hashing and two pointers (E09-E17) | 🔒 Locked |
| 04 | Easy problems, part 3: window, stack, recursion, sorting, greedy, DP, matrix (E18-E25) | 🔒 Locked |
| 05 | Medium problems, part 1: math, strings, arrays and hashing (M01-M09) | 🔒 Locked |
| 06 | Medium problems, part 2: two pointers, sliding window, stacks and recursion (M10-M17) | 🔒 Locked |
| 07 | Medium problems, part 3: sorting and searching, greedy, DP and matrices (M18-M25) | 🔒 Locked |
| 08 | Hard problems, part 1: dynamic programming and grids (H01-H05) | 🔒 Locked |
| 09 | Hard problems, part 2: window, stack, backtracking, greedy and divide-and-conquer (H06-H10) | 🔒 Locked |
| 10 | Mock technical assessment 1 | 🔒 Locked |
| 11 | Mock technical assessment 2 | 🔒 Locked |
| 12 | Mock technical assessment 3 | 🔒 Locked |
| 13 | Mock technical assessment 4 | 🔒 Locked |
| 14 | Easy problems, part 4: bits, prefix sums, binary search on the answer, linked lists (E26-E33) | 🔒 Locked |
| 15 | Easy problems, part 5: intervals, heaps, graphs, union-find, string matching, DP on strings (E34-E40) | 🔒 Locked |
| 16 | Medium problems, part 4 (M26-M33) | 🔒 Locked |
| 17 | Medium problems, part 5 (M34-M40) | 🔒 Locked |
| 18 | Hard problems, part 3 (H11-H15) | 🔒 Locked |
| 19 | Hard problems, part 4 (H16-H20) | 🔒 Locked |
| 20 | Mock technical assessment 5 | 🔒 Locked |
| 21 | Mock technical assessment 6 | 🔒 Locked |
| 22 | Mock technical assessment 7 | 🔒 Locked |
| 23 | Mock technical assessment 8 | 🔒 Locked |
| 24 | Company coding round patterns | 🔒 Locked |

## Preview: Easy problems, math and strings

### The idea in plain words

Easy questions test two things: **can you read the input correctly** and **do you know the one small trick** (a formula, a modulo, a reverse).
Think of a kirana shop owner adding a bill: the maths is simple, but one wrong digit spoils everything.

### E05. Palindrome shop name

**Pattern:** Strings | **Level:** Easy

A sign painter wants shop names that read the same from both ends. Ignore case, spaces and anything that is not a letter or digit.
Print YES if the name is a palindrome under these rules, else NO. (A name with no letters or digits counts as YES.)

- **Input format.** One line: the shop name.
- **Output format.** YES or NO.
- **Constraints.** 1 <= length <= 10^5.

```text
Input:
Step on no pets!
Output:
YES
```

*Why:* 'Step on no pets!' becomes 'steponnopets', which reads the same backwards.

**Solution idea.** Build the cleaned string with a generator, then compare it with its reverse. The two-pointer version (i from left, j from right) uses O(1) extra space and is what interviewers often ask next. Time: O(n). Space: O(n).

```python
def solve(data):
    s = "".join(c.lower() for c in data if c.isalnum())
    return "YES" if s == s[::-1] else "NO"
```

Real test output:

```text
Test 1: PASS  output: YES
Test 2: PASS  output: YES
Test 3: PASS  output: NO
Test 4: PASS  output: YES
4/4 tests passed
```

### Try 3 questions (solutions open)

**1. E06. Vowels and consonants in an SMS.** Count the vowels (a, e, i, o, u, either case) and consonants (other English letters) in an SMS. Digits, spaces and symbols are not counted.
Input: one line, the SMS text. Output: two integers, vowels and consonants, separated by a space. Example: `Hello World` gives `3 7`.

<details><summary>Solution</summary>

Walk through each character once. If it is a letter, it is either a vowel or a consonant. The trap is counting spaces or digits as consonants. Time: O(n). Space: O(1).

```python
def solve(data):
    v = c = 0
    for ch in data:
        if ch.isalpha() and ch.isascii():
            if ch in "aeiouAEIOU":
                v += 1
            else:
                c += 1
    return f"{v} {c}"
```

```text
Test 1: PASS  output: 3 7
Test 2: PASS  output: 3 5
Test 3: PASS  output: 0 3
3/3 tests passed
```

</details>

**2. E07. Reverse the announcement.** A railway announcement board shows words in the wrong order. Reverse the order of the words. Words are separated by one or more spaces; print them with single spaces and no spaces at the ends.
Example: `  the train is late  ` gives `late is train the`.

<details><summary>Solution</summary>

split() with no argument handles multiple spaces for you. split(' ') would give empty strings, a classic bug. Time: O(n). Space: O(n).

```python
def solve(data):
    return " ".join(reversed(data.split()))
```

```text
Test 1: PASS  output: late is train the
Test 2: PASS  output: hello
Test 3: PASS  output: c b a
3/3 tests passed
```

</details>

**3. E08. Compress the attendance string.** Attendance for a week is stored as letters, e.g. 'PPPAAP'. Compress it: write each run of the same letter as the letter followed by the run length. 'aaabbc' becomes 'a3b2c1'.
Example: `zzzzzzzzzzzz` gives `z12`.

<details><summary>Solution</summary>

Walk with an index i; let j move forward while s[j] == s[i]; append s[i] + str(j - i); set i = j. Using a list and ''.join keeps it O(n). The 'abca' test shows that the same letter can appear in two separate runs. Time: O(n). Space: O(n).

```python
def solve(data):
    s = data.strip()
    out = []
    i = 0
    while i < len(s):
        j = i
        while j < len(s) and s[j] == s[i]:
            j += 1
        out.append(s[i] + str(j - i))
        i = j
    return "".join(out)
```

```text
Test 1: PASS  output: a3b2c1
Test 2: PASS  output: z12
Test 3: PASS  output: a1b1c1a1
3/3 tests passed
```

</details>

---

## Get the full module

The complete module, along with all 7 modules of the course, company chapters and AI mock interviews on **NeoHireAI**, is available
to subscribing colleges and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>© 2026 NeoTridhi Private Limited.</sub>
