<p align="center"><b>Persistent Systems</b></p>

# Persistent Systems: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Persistent Systems chapter has 19 questions with worked solutions, a 4-week plan,
> common traps and what each round looks for. [See how to get it](#get-the-full-persistent-systems-chapter).

[Back to all companies](../README.md#companies)

---

## A GATE-style paper with a coding practical

Most service-company tests are like a general-category railway exam: wide but easy. The Persistent test is closer to a GATE-style paper with a
coding practical: fewer English and maths questions, more operating systems, DBMS, networks and data structures. Your CS basics carry you.

**Important for 2026:** Business Standard reported in April 2026 that CEO Sandeep Kalra said Persistent was **not looking to hire many fresh
engineering graduates** and would focus on **lateral (experienced) hires** in areas where it wants to invest. So fresher seats may be few.

Commonly reported hiring rounds (approximate):

```
Objective round (CS + English + logical) --> Coding round (2 problems) --> [Advanced coding for top scorers] --> Technical interview 1 --> Technical interview 2 --> HR
```

## Persistent online test (commonly reported; varies by drive)

Not official. One widely read prep site reports the pattern below. Treat all numbers as approximate.

| Section | Commonly reported topics | Approx. size and time |
|---|---|---|
| Computer science | OS, DBMS, SQL, networks, computer architecture, data structures and algorithms | about 20 questions, 20 min |
| English | Synonyms, antonyms, jumbled sentences, voice, comprehension | about 12 questions, 15 min |
| Logical ability | Deductive and inductive reasoning, seating, blood relations, coding-decoding, series | about 12 questions, 15 min |
| Coding | 2 problems; C, C++, Java, Python and others reported | about 45 min |
| Advanced coding (only for strong performers, reported) | Trees, graphs, heaps, greedy, dynamic programming, backtracking | 2 problems, about 60 min |

## Official links

| Link | What it is |
|---|---|
| [Persistent Early Careers and Campus Program](https://www.persistent.com/careers/early-careers-campus-program/) | Official page: campus programme for technology and business roles, Train and Hire, Career Compass, Hyperscaler Enablement, 250+ universities. |

Find Persistent's main careers portal and its recruitment-fraud page from the Early Careers page. **Never pay anyone for a job.**

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Persistent test, with new numbers and wording.

**1. (Computer science: SQL)** Table `orders(id, city, amount)`. Which query lists the cities with **more than 2** orders? (a) `SELECT city FROM orders WHERE COUNT(*) > 2 GROUP BY city;` (b) `SELECT city FROM orders GROUP BY city HAVING COUNT(*) > 2;` (c) `SELECT city FROM orders HAVING city > 2;` (d) `SELECT DISTINCT city FROM orders WHERE id > 2;`

<details><summary>Solution</summary>

**(b).** WHERE filters single rows **before** grouping and cannot use COUNT(*). HAVING filters groups after GROUP BY. Run here on sample data:

```python
import sqlite3
con = sqlite3.connect(":memory:")
con.execute("CREATE TABLE orders(id INTEGER, city TEXT, amount INTEGER)")
con.executemany("INSERT INTO orders VALUES (?, ?, ?)", [
    (1, "Pune", 500), (2, "Nagpur", 300), (3, "Pune", 700), (4, "Nashik", 200),
    (5, "Pune", 400), (6, "Nagpur", 900), (7, "Nagpur", 150)])
q = "SELECT city FROM orders GROUP BY city HAVING COUNT(*) > 2 ORDER BY city"
print([row[0] for row in con.execute(q)])
# Output: ['Nagpur', 'Pune']
```

</details>

**2. (Computer science: networks)** How many **usable** host addresses does a /26 IPv4 subnet have? (a) 64 (b) 62 (c) 30 (d) 126

<details><summary>Solution</summary>

/26 leaves 32 - 26 = 6 host bits: 2^6 = 64 addresses. Remove the network and broadcast addresses: 64 - 2 = **(b) 62**.

</details>

**3. (English: voice)** Change to active voice: "The bug was fixed by Swathi before the release." (a) Swathi fixed the bug before the release. (b) Swathi has fixed the bug before the release. (c) Swathi was fixing the bug before the release. (d) The bug fixed Swathi before the release.

<details><summary>Solution</summary>

**(a) Swathi fixed the bug before the release.** The tense stays simple past.

</details>

**4. (Logical ability: deduction)** "If the server is down, the app shows an error." Today the app did **not** show an error. What must be true? (a) The server is down. (b) The server is not down. (c) The app is broken. (d) Cannot say.

<details><summary>Solution</summary>

If "down" always gives an error, then "no error" means "not down". **(b)**. (This is the rule "if P then Q; not Q, so not P".)

</details>

**5. (Coding: strings)** Find the longest common prefix of roll numbers. Tests: ["21NEC045", "21NEC048", "21NEC1"] and ["CSE01", "ECE01"].

<details><summary>Solution</summary>

Shrink the first string until every other string starts with it.

```python
def common_prefix(words):
    if not words:
        return ""
    prefix = words[0]
    for w in words[1:]:
        while not w.startswith(prefix):
            prefix = prefix[:-1]
    return prefix

print(common_prefix(["21NEC045", "21NEC048", "21NEC1"]))
print(repr(common_prefix(["CSE01", "ECE01"])))
# Output: 21NEC
# ''
```

</details>

---

## 🔒 In the full Persistent Systems chapter

| Section | Locked questions (topics) |
|---|---|
| Computer science | Paging · Binary search tree traversal, with running Python code · Worst-case sorting · Correlated subquery in SQL · FIFO page replacement · Postfix evaluation with a stack · Network devices |
| English | Vocabulary in context · Prepositions · Jumbled sentences |
| Logical ability | Letter series · Seating arrangement · Coding-decoding |
| Coding | Shortest path in a grid with BFS, with running Python code |
| Also in the chapter | Official pre-hiring programmes (Train and Hire, Career Compass and more) · Role tracks · What each round looks for · Common traps · A 4-week plan · How AI is changing Persistent hiring |

## Get the full Persistent Systems chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Persistent Systems. © 2026 NeoTridhi Private Limited.</sub>
