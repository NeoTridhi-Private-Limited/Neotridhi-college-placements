<p align="center"><img src="../assets/logos/hcltech.svg" alt="HCLTech" height="70"></p>

# HCLTech: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full HCLTech chapter has 40+ questions with worked solutions, a 3-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-hcltech-chapter).

[Back to all companies](../README.md#companies)

---

## Four overs per bowler

The HCLTech test is like a four-over-per-bowler rule in a T20 match: each section has its own fixed time, so you cannot spend extra time
on your favourite section. Balance matters more than brilliance in one area.

```
Application and resume --> Shortlisting --> Business / technical interview --> HR interview --> Decision and offer
```

For campus drives, an **online test** usually comes before shortlisting. The official page says technical interviews "may include out-of-the-box
queries, puzzles and problems".

## Campus online test (commonly reported; versions differ)

| Section | Approx. questions | Approx. time |
|---|---|---|
| Quantitative aptitude | 15 | 15 min |
| Logical reasoning | 15 | 15 min |
| Verbal ability | 15 | 15 min |
| Technical / computer fundamentals | 15 | 15 min |

Some drives are reported to include a short coding section (about 2 problems). **Check your drive notice.**

## Official links

| Link | What it is |
|---|---|
| [HCLTech Careers](https://careers.hcltech.com/) | Official careers home with the hiring-process section |
| [HCLTech TechBee](https://www.hcltechbee.com/) | Official site of the TechBee early-career programme |
| [Genuine job offers](https://www.hcltech.com/careers/genuine-job-offers) | Official job-scam awareness page |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the HCLTech test, with new numbers and wording.

**1. (Quantitative aptitude: successive discounts)** A shop gives a 20% discount and then a further 10% on the reduced price.
What single discount is this equal to? (a) 30% (b) 28% (c) 27% (d) 25%

<details><summary>Solution</summary>

Price after both = 100 x 0.8 x 0.9 = 72. Single discount = 100 - 72 = **(b) 28%**.
Shortcut: a + b - ab/100 = 20 + 10 - 2 = 28.

</details>

**2. (Quantitative aptitude: work with men and women)** 8 men or 12 women can finish a job in 15 days. How long will 6 men and 6 women take together?
(a) 10 days (b) 12 days (c) 14 days (d) 15 days

<details><summary>Solution</summary>

8 men = 12 women, so 1 man = 1.5 women. 6 men = 9 women; with 6 women, the team = 15 women.
Total work = 12 women x 15 days = 180 woman-days. Time = 180 / 15 = **(b) 12 days**.

</details>

**3. (Logical reasoning: balance puzzle)** You have 8 balls that look the same. One is slightly heavier. Using a simple balance, what is the minimum number of weighings that always finds the heavy ball?
(a) 1 (b) 2 (c) 3 (d) 4

<details><summary>Solution</summary>

**(b) 2.** Weighing 1: put 3 balls on each side, keep 2 aside.
- If one side is heavier, the heavy ball is among those 3. Weighing 2: put 1 vs 1 from those 3. Heavier side wins; if equal, it is the third.
- If balanced, the heavy ball is among the 2 kept aside. Weighing 2: 1 vs 1.
Why not 1? One weighing has only 3 results (left, right, equal), which cannot separate 8 possibilities.

</details>

**4. (Verbal: pronoun case)** Find the error: "Ravi and me went to the placement drive together."

<details><summary>Solution</summary>

The subject needs "I": **"Ravi and I went..."** Test: remove "Ravi and". "Me went" is wrong; "I went" is right.

</details>

**5. (Computer fundamentals: C output, division and cast)** What does this C code print?

```c
int a = 7, b = 2;
printf("%d %d %.1f", a / b, a % b, (float)a / b);
```

<details><summary>Solution</summary>

In C, int / int gives an int: 7 / 2 = 3. 7 % 2 = 1. Casting a to float first gives 7.0 / 2 = 3.5. Output: **3 1 3.5**.

```python
a, b = 7, 2
print(a // b, a % b, round(a / b, 1))   # // is integer division in Python
# Output: 3 1 3.5
```

</details>

---

## 🔒 In the full HCLTech chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude | Unitary method · Pass marks · Relative speed · Partnership · Sum of odd numbers · Averages · Two-digit numbers · Probability |
| Logical reasoning | Analogy · Letter pairs · Ranking in a queue · Syllogism · Directions with a shadow |
| Verbal ability | Antonyms · Passive voice · Prepositions · One-word substitution · Sentence completion with contrast |
| Computer fundamentals and coding | Number systems (hex and binary) · Leap year check · GCD and LCM with Euclid's method, with running Python code |
| Interview | Water jug puzzle · Compiler vs interpreter · Working with a difficult team member (HR) · Where you see yourself in five years (HR) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 3-week plan · How AI is changing HCLTech hiring |

## Get the full HCLTech chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by HCLTech. © 2026 NeoTridhi Private Limited.</sub>
