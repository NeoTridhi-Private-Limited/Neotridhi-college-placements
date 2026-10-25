<p align="center"><img src="../assets/logos/capgemini.svg" alt="Capgemini" height="70"></p>

# Capgemini: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Capgemini chapter has 40+ questions with worked solutions, a 3-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-capgemini-chapter).

[Back to all companies](../README.md#companies)

---

## Puzzle games and recipes

A game-based test is like a mobile puzzle game: quick rounds, patterns, switches, grids. It checks how you think, not what you memorised.
Pseudocode is like a recipe written in plain steps; you must "cook it in your head" and say what comes out.
Prep sites report that one application and one test decide the track: **Analyst** or **Senior Analyst**.

```
Online aptitude test --> Coding or technical assessment --> Group discussion (select roles only) --> Technical interview --> HR interview
```

## Capgemini assessment (commonly reported; varies by drive)

| Part | Approx. content | Notes |
|---|---|---|
| Pseudocode | Output of loops, recursion, bitwise operators, swaps | MCQs |
| English communication | Grammar, vocabulary, reading | MCQs |
| Game-based aptitude | Deductive logic grids, inductive patterns, "switch" puzzles, motion/grid games | About 45 min reported |
| Behavioural competency | Situation-based choices | No "right" pattern to memorise; be consistent |
| Coding (Senior Analyst) | 1-2 problems | Reported mainly for the higher track |
| Interviews | Technical + HR / behavioural | STAR answers help |

## Official links

| Link | What it is |
|---|---|
| [Recruitment process](https://www.capgemini.com/in-en/careers/join-capgemini/recruitment-process/) | Official stages for campus hiring |
| [Students and graduates](https://www.capgemini.com/in-en/careers/career-paths/students-and-graduates/) | Official page for freshers |
| [Fraud alert](https://www.capgemini.com/in-en/fraud-alert/) | Official warning: recruiters use capgemini.com, sogeti.com or frog.co emails; never pay anyone |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Capgemini assessment, with new numbers and wording.

**1. (Quantitative aptitude: LCM)** Three temple bells ring every 12, 18 and 30 minutes. They ring together at 9:00 am. When do they next ring together?
(a) 10:30 am (b) 11:00 am (c) 12:00 noon (d) 1:30 pm

<details><summary>Solution</summary>

LCM(12, 18, 30): 12 = 2^2 x 3, 18 = 2 x 3^2, 30 = 2 x 3 x 5. LCM = 2^2 x 3^2 x 5 = 180 minutes = 3 hours.
9:00 am + 3 h = **(c) 12:00 noon**.

</details>

**2. (Quantitative aptitude: clocks)** What is the angle between the hour and minute hands at 3:40?
(a) 120 degrees (b) 125 degrees (c) 130 degrees (d) 140 degrees

<details><summary>Solution</summary>

Angle = |30H - 5.5M| = |30 x 3 - 5.5 x 40| = |90 - 220| = **(c) 130 degrees**.
Why 5.5: the minute hand moves 6 degrees a minute, the hour hand 0.5 degrees a minute.

</details>

**3. (Game-style reasoning: switch challenge)** A switch code tells which input position goes to each output position.
Code 2413 means: output 1 = input 2, output 2 = input 4, output 3 = input 1, output 4 = input 3.
The symbols P Q R S pass through switch 2413 and then through switch 4123. What comes out?

<details><summary>Solution</summary>

After 2413: (input 2, input 4, input 1, input 3) = Q S P R.
Now apply 4123 to Q S P R: (4th, 1st, 2nd, 3rd) = R Q S P.
Answer **R Q S P**.

</details>

**4. (English: articles)** "He is ___ honest man and ___ university professor."
(a) a, a (b) an, an (c) an, a (d) a, an

<details><summary>Solution</summary>

Articles follow the SOUND. "Honest" starts with a vowel sound (the h is silent): **an** honest. "University" starts with a "yoo" sound: **a** university. Answer **(c)**.

</details>

**5. (Pseudocode: integer division, mod, shift)** What is printed? (`/` between integers is integer division, `mod` is the remainder, `>>` shifts bits right.)

```
integer a = 25, b = 4, c
c = a / b
c = c * b + a mod b
a = a >> 1
print c + a
```
(a) 37 (b) 38 (c) 25 (d) 36

<details><summary>Solution</summary>

c = 25 / 4 = 6 (integer division). c = 6 x 4 + 25 mod 4 = 24 + 1 = 25 (this always rebuilds a).
a >> 1 = 25 shifted right by 1 = 12 (same as integer division by 2). Print 25 + 12 = **(a) 37**.

</details>

---

## 🔒 In the full Capgemini chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude | Ratios · Percentages · Speed · Compound vs simple interest · Time and work · Calendars · Probability · Averages |
| Game-style reasoning | Deductive logic grid (4 x 4) · Inductive odd one out · Grid movement · Deductive matching · Letter-number series |
| English communication | Prepositions · Error spotting · Vocabulary · Sentence improvement · Reading for inference |
| Pseudocode and coding | Recursion: value and number of calls · Nested loops with break · Moving zeros to the end (Senior Analyst), with running Python code |
| Interview and behavioural | Overloading vs overriding · Stack vs queue · A bug the night before a demo (behavioural) · Why Capgemini (HR) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 3-week plan · How AI is changing Capgemini hiring |

## Get the full Capgemini chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Capgemini. © 2026 NeoTridhi Private Limited.</sub>
