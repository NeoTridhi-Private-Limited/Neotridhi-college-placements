<p align="center"><b>Mphasis</b></p>

# Mphasis: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Mphasis chapter has 19 questions with worked solutions, a 4-week plan,
> common traps and what each round looks for. [See how to get it](#get-the-full-mphasis-chapter).

[Back to all companies](../README.md#companies)

---

## Watched in the nets, then picked

Think of a cricket academy. Some academies pick players from one trial match. Others watch you in net sessions for three months and then
pick. Mphasis now works more like the second academy: it wants to see you **learn and build** on a live project before it decides.

**Important for 2026:** Business Standard reported in January 2026 that Mphasis had **not hired engineering graduates from campuses for the
last two years**. Instead, **internships of three to six months** became its main source of new employees.
Ask your placement cell which route Mphasis is using at your college this year.

The official Mphasis "Application process" page lists these **elimination rounds**:

```
Aptitude test --> Personal interview --> Communication test --> Letter of Intent --> Training batch call --> Joining --> Permanent offer letter
```

## Mphasis online test (commonly reported; varies by drive)

Mphasis does not publish its test pattern. Prep sites commonly report an AMCAT-style online test. Treat every number below as approximate.

| Section | Commonly reported topics | Approx. size |
|---|---|---|
| Quantitative aptitude | Percentages, ratio, time and work, speed, profit and loss, series | about 25 questions |
| Logical reasoning | Coding-decoding, puzzles, blood relations, directions, data interpretation | about 25 questions |
| Verbal / English | Sentence completion, grammar, reading comprehension, synonyms and antonyms | about 25 questions |
| Computer programming | Loops, functions, recursion, arrays, stacks, queues, trees, sorting, Big O | about 20 questions |
| Spoken English (SVAR-style, reported) | Reading aloud, repeating sentences, listening | varies |
| Coding (some drives) | 1-2 automata-style problems | varies |

## Official links

| Link | What it is |
|---|---|
| [Mphasis Careers](https://careers.mphasis.com/) | Official careers home with job search and a fraud-warning banner. |
| [Campus Programs](https://careers.mphasis.com/home/hot-jobs/category/campus-programs.html) | Official page on Tier-1/Tier-2 campus hiring, MASE, internships, B-school and HR programmes. |
| [Application process](https://careers.mphasis.com/home/information-center/application-process.html) | Official eligibility (60% average), elimination rounds, Letter of Intent and onboarding. |
| [Fraud awareness](https://careers.mphasis.com/home/information-center/fraud-awareness.html) | Official page: Mphasis does not charge candidates; signs of fake offers. |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Mphasis test, with new numbers and wording.

**1. (Quantitative aptitude: ratio)** Rs 7,200 is shared among Anil, Bhanu and Chitra in the ratio 2 : 3 : 4. What is Bhanu's share? (a) Rs 1,600 (b) Rs 2,400 (c) Rs 3,200 (d) Rs 2,700

<details><summary>Solution</summary>

Total parts = 2 + 3 + 4 = 9. One part = 7200 / 9 = 800. Bhanu = 3 x 800 = **(b) Rs 2,400**.

</details>

**2. (Logical reasoning: coding-decoding)** If RICE is written as SJDF, how is DOSA written? (a) EPTB (b) CNRZ (c) EPSB (d) FQUC

<details><summary>Solution</summary>

Each letter moves one step forward: R->S, I->J, C->D, E->F. So D->E, O->P, S->T, A->B = **(a) EPTB**.

</details>

**3. (Verbal: tense)** "By next June, Ramesh ___ his degree." (a) completes (b) has completed (c) will have completed (d) completed

<details><summary>Solution</summary>

An action that will be finished before a future time takes the future perfect: **(c) will have completed**.

</details>

**4. (Computer programming: output)** What is printed? `x = 5; for i = 1 to 3: x = x * 2 - i; print x` (a) 23 (b) 26 (c) 29 (d) 32

<details><summary>Solution</summary>

i = 1: 5 x 2 - 1 = 9. i = 2: 9 x 2 - 2 = 16. i = 3: 16 x 2 - 3 = **(c) 29**. Python check:

```python
x = 5
for i in range(1, 4):
    x = x * 2 - i
print(x)
# Output: 29
```

</details>

**5. (Coding: averages)** A metro station records daily footfall: 1200, 950, 1430, 1100, 1320. Count the days with footfall **above** the average.

<details><summary>Solution</summary>

Average = (1200 + 950 + 1430 + 1100 + 1320) / 5 = 6000 / 5 = 1200. Above 1200: 1430 and 1320. 1200 itself is **not above**. Answer **2**.

```python
def days_above_average(footfall):
    avg = sum(footfall) / len(footfall)
    return sum(1 for f in footfall if f > avg)

print(days_above_average([1200, 950, 1430, 1100, 1320]))
# Output: 2
```

</details>

---

## 🔒 In the full Mphasis chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude | Average speed · Time and work · Averages with replacement · Mark-up and discount · Mixtures |
| Logical reasoning | Number series · Coded blood relations · Floor puzzle |
| Verbal | Antonyms · Error spotting · Idioms |
| Computer programming | Time complexity of sorting · Recursion, with running Python code |
| Coding | Pangram check, with running Python code |
| Also in the chapter | Role tracks and campus programmes · What each round looks for · Common traps, including fake-offer warnings · A 4-week plan · How AI is changing Mphasis hiring |

## Get the full Mphasis chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Mphasis. © 2026 NeoTridhi Private Limited.</sub>
