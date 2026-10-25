<p align="center"><b>Product companies</b></p>

# Product companies: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Product companies chapter covers Amazon, Microsoft, Google, Zoho and Freshworks,
> and has 40+ questions with worked solutions, an 8-10 week plan, common traps and interview answers. [See how to get it](#get-the-full-product-companies-chapter).

[Back to all companies](../README.md#companies)

---

## Picked for a match on the same day

A service company asks, "Can we train you?" A product company asks, "Can you solve a new problem today, cleanly, and explain it?"
It is like the difference between joining a cricket academy and being picked for a match on the same day.

Typical fresher process (official where stated, otherwise commonly reported):

```
Amazon:      Online assessment --> Loop of interviews
Microsoft:   Online coding test (reported 2-3 problems) --> 2-4 technical interviews (DSA, problem solving) --> Final round
Google:      Online challenge or recruiter screen --> Technical interviews (DSA, coding in a shared doc) --> "Googleyness" / behaviour discussion
Zoho:        Written aptitude --> C/C++ output prediction --> Basic programming --> Advanced programming --> Technical interview --> HR
Freshworks:  Online coding test --> Technical interviews (DSA, a small design problem) --> Culture/HR round
```

## Online tests and interview focus (commonly reported; varies by drive)

| Company | Online test (approx.) | Interview focus |
|---|---|---|
| Amazon | 2 coding problems (90 min for SDE II, official) + work-style survey | DSA + Leadership Principles stories (STAR) |
| Microsoft | 2-3 coding problems, about 60-90 min (reported) | DSA, problem solving, clean code |
| Google | Coding challenge (reported) | DSA, complexity, communication |
| Zoho | Written aptitude + C output + programming rounds (reported) | Logic, C fundamentals, building a working program |
| Freshworks | 2-3 coding problems (reported) | DSA, SaaS product thinking, culture fit |

## Official links

| Link | What it is |
|---|---|
| [Amazon SDE online assessment prep](https://amazon.jobs/content/en/how-we-hire/sde-ii-oa-prep) | Official OA format: coding (90 min, 2 questions), system design, work styles. Written for SDE II but useful for everyone. |
| [Microsoft university careers](https://careers.microsoft.com/v2/global/en/universityinternship) | Official Microsoft students and graduates page. |
| [Google: how we hire](https://www.google.com/about/careers/applications/how-we-hire/) | Official hiring-process page with interview prep links. |
| [Zoho careers](https://careers.zohocorp.com/) | Official Zoho job portal. |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of product-company rounds, with new numbers and wording.

**1. (Aptitude: conditional probability)** Bag A has 3 red and 2 blue balls. Bag B has 1 red and 4 blue balls.
A coin toss picks a bag, and one ball is drawn. It is red. What is the probability it came from Bag A?
(a) 3/5 (b) 1/2 (c) 3/4 (d) 2/3

<details><summary>Solution</summary>

P(A and red) = 1/2 x 3/5 = 3/10. P(B and red) = 1/2 x 1/5 = 1/10.
P(A given red) = (3/10) / (3/10 + 1/10) = 3/4 = **(c)**.
Idea: among all the ways to see red, three out of four go through Bag A. This is Bayes' rule, used in spam filters.

</details>

**2. (Reasoning and puzzles: lockers)** A hostel corridor has 50 closed lockers and 50 students. Student 1 opens every locker. Student 2 toggles (opens if closed, closes if open) every 2nd locker, student 3 every 3rd locker, and so on up to student 50.
How many lockers are open at the end?

<details><summary>Solution</summary>

Locker n is toggled once for each divisor of n. It ends open only if it is toggled an odd number of times.
Divisors come in pairs (for 12: 1 and 12, 2 and 6, 3 and 4), except for perfect squares, where one divisor pairs with itself (for 16: 4 x 4).
So only perfect squares stay open: 1, 4, 9, 16, 25, 36, 49. Answer **7 lockers**. (A program that toggles all 50 lockers gives the same 7.)

</details>

**3. (Verbal: grammar)** Choose the correct sentence.
(a) The list of failing tests are long. (b) The list of failing tests is long. (c) The list of failing tests were long. (d) The lists of failing test is long.

<details><summary>Solution</summary>

The subject is "list" (singular); "of failing tests" only describes it. So **(b) "The list of failing tests is long."**

</details>

**4. (Coding: dynamic programming, coin change)** A canteen token machine gives tokens worth 1, 5 and 7. What is the fewest tokens that make an amount? Return -1 if impossible.
Test: amount 10 and 24 with tokens [1, 5, 7]; amount 7 with tokens [4, 6].

<details><summary>Solution</summary>

Greedy (take the biggest token first) fails: for 10 it takes 7 + 1 + 1 + 1 = 4 tokens, but 5 + 5 = 2 tokens.
DP: best[a] = fewest tokens for amount a = 1 + min(best[a - c]) over every token c that fits.

```python
def min_tokens(tokens, amount):
    INF = float("inf")
    best = [0] + [INF] * amount
    for a in range(1, amount + 1):
        for c in tokens:
            if c <= a and best[a - c] + 1 < best[a]:
                best[a] = best[a - c] + 1
    return best[amount] if best[amount] != INF else -1

def greedy(tokens, amount):              # biggest token first (wrong in general)
    used = 0
    for c in sorted(tokens, reverse=True):
        used, amount = used + amount // c, amount % c
    return used if amount == 0 else -1

def brute(tokens, amount, start=0):      # try every combination (small amounts only)
    if amount == 0:
        return 0
    best = -1
    for i in range(start, len(tokens)):
        if tokens[i] <= amount:
            r = brute(tokens, amount - tokens[i], i)
            if r != -1 and (best == -1 or r + 1 < best):
                best = r + 1
    return best

print(min_tokens([1, 5, 7], 10), greedy([1, 5, 7], 10))
print(min_tokens([1, 5, 7], 24), min_tokens([4, 6], 7), min_tokens([3], 0))

import random
random.seed(3)
ok = all(min_tokens(t, a) == brute(t, a)
         for t, a in ((random.sample(range(1, 12), random.randint(1, 3)), random.randint(0, 25)) for _ in range(400)))
print("matches brute force:", ok)
# Output:
# 2 4
# 4 -1 0
# matches brute force: True
```
24 = 7 + 7 + 5 + 5 (4 tokens). Time O(amount x number of tokens), space O(amount).

</details>

**5. (Interview: processes and threads)** "What is the difference between a process and a thread? What can go wrong when threads share data?"

<details><summary>Solution</summary>

- A **process** is a running program with its own memory space. Two processes do not see each other's variables; they talk through files, pipes or the network.
- A **thread** is a path of execution inside a process. Threads of one process share the same memory, so they are cheaper to create and switch between.
- Example: a browser may run each tab as a separate process (one crash does not kill the others); inside a tab, threads draw and download.

What goes wrong: a **race condition**. Two threads read a counter as 10, both add 1 and both write 11, so one update is lost.
Fix: make the update atomic, or protect it with a lock (mutex). Too many locks, taken in different orders, can cause a **deadlock**, where each thread waits for the other forever.

</details>

---

## 🔒 In the full Product companies chapter

| Section | Locked questions (topics) |
|---|---|
| Aptitude: probability, counting and numbers | Arrangements with repeated letters · Probability with dice · "At least one" probability · Selection with a condition · Sharing identical items · Counting divisible numbers · Remainders · Expected value · Circular arrangement |
| Reasoning and puzzles | Scheduling puzzle · Number series · Truth-teller counting · Digits puzzle · One weighing to find a fake bag |
| Verbal: reading and a short professional email | Reading comprehension (2 questions) · An email to a recruiter, with a model answer · Concise writing · Ordering a bug report |
| Coding and C output | Counting subarrays with prefix sums · Topological order of tasks, both with running Python code checked against brute force · C output with pointers and static variables |
| Interview | Designing an OTP rate limiter, with running code · A "Customer Obsession" story (Amazon Leadership Principle) · A "Dive Deep" story (Amazon Leadership Principle) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Role tracks for each company · Common traps · An 8-10 week plan · How AI is changing product-company hiring |

## Get the full Product companies chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Amazon, Microsoft, Google, Zoho or Freshworks. © 2026 NeoTridhi Private Limited.</sub>
