<p align="center"><img src="../assets/logos/infosys.svg" alt="Infosys" height="70"></p>

# Infosys: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Infosys chapter has 40+ questions with worked solutions, a 4-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-infosys-chapter).

[Back to all companies](../README.md#companies)

---

## Two doors into Infosys

Think of a cricket academy. Most players join through the regular selection trial: the **System Engineer** test.
A few are spotted at a tournament (**HackWithInfy**) or in a special nets session (the **Specialist Programmer / Digital Specialist Engineer
coding test**) and go straight to a higher team. Same company, different gates, different pay bands.

```
Regular route:   Registration --> Online test (aptitude + pseudocode + verbal) --> Interview (tech + HR) --> Offer
Coding route:    Registration --> Coding test (hard DSA, about 3 hours reported) --> Technical interview(s) --> HR --> SP / DSE offer
HackWithInfy:    Register via college --> Round 1 (3-hr coding) --> Round 2 (3-hr coding) --> Grand Finale --> interview chance
```

## System Engineer online test (commonly reported; varies by drive)

| Section | Approx. questions | Approx. time |
|---|---|---|
| Logical reasoning | 15 | 25 min |
| Mathematical ability | 10 | 35 min |
| Verbal ability | 20 | 20 min |
| Pseudocode | 5 | 10 min |
| Puzzle solving | 4 | 10 min |

## Official links

| Link | What it is |
|---|---|
| [Infosys Careers: students](https://www.infosys.com/careers/apply/students.html) | Official page for students and graduates |
| [HackWithInfy](https://www.infosys.com/careers/hackwithinfy.html) | Official HackWithInfy page: rounds, timeline, eligibility |
| [Infosys Springboard](https://infyspringboard.onwingspan.com/) | Official free learning platform from Infosys |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Infosys test, with new numbers and wording.

**1. (Mathematical ability: probability)** Three coins are tossed before a gully cricket match. What is the probability of getting at least two heads?
(a) 1/4 (b) 3/8 (c) 1/2 (d) 7/8

<details><summary>Solution</summary>

There are 2 x 2 x 2 = 8 equally likely outcomes.
Exactly two heads: HHT, HTH, THH = 3. Three heads: HHH = 1. Favourable = 4.
Probability = 4/8 = **1/2**. Answer: **(c)**.

</details>

**2. (Mathematical ability: remainders with powers)** Find the remainder when 3^100 is divided by 7.
(a) 1 (b) 3 (c) 4 (d) 6

<details><summary>Solution</summary>

Find the cycle of remainders of powers of 3 when divided by 7:
3^1 = 3, 3^2 = 9 -> 2, 3^3 -> 6, 3^4 -> 4, 3^5 -> 5, 3^6 -> 1. The cycle length is 6.
100 = 6 x 16 + 4, so 3^100 leaves the same remainder as 3^4: **4**. Answer: **(c)**.

</details>

**3. (Logical reasoning: letter analogy)** ACE : FHJ :: KMO : ?
(a) PRT (b) OQS (c) PQR (d) LNP

<details><summary>Solution</summary>

Each letter of ACE moves 5 places forward: A -> F, C -> H, E -> J.
Apply the same to KMO: K -> P, M -> R, O -> T = **PRT**. Answer: **(a)**.

</details>

**4. (Verbal: sentence improvement)** Improve the bold part: "**If I would have known** about the drive, I would have applied."
(a) If I would know (b) If I had known (c) If I have known (d) No improvement needed

<details><summary>Solution</summary>

For an unreal past condition, use "if + had + past participle", then "would have + past participle".
Correct: "**If I had known** about the drive, I would have applied." Answer: **(b)**.

</details>

**5. (Pseudocode: nested loops)** What is printed?

```
int count = 0;
for (int i = 1; i <= 5; i++)
    for (int j = i; j <= 5; j++)
        count = count + 1;
print(count);
```
(a) 10 (b) 15 (c) 20 (d) 25

<details><summary>Solution</summary>

The inner loop starts at j = i, so it runs (6 - i) times:
i = 1: 5 times, i = 2: 4, i = 3: 3, i = 4: 2, i = 5: 1. Total = 5 + 4 + 3 + 2 + 1 = **15**. Answer: **(b)**.
Trap: (d) 25 assumes the inner loop always starts at 1.

</details>

---

## 🔒 In the full Infosys chapter

| Section | Locked questions (topics) |
|---|---|
| Mathematical ability | Series · Ages · Work and wages · Relative speed · Mixtures and alligation · Trailing zeros in factorials · Arrangements with a restriction · Number of factors |
| Logical reasoning and puzzles | Data sufficiency · Coded blood relations · Floor arrangement · Truth and lies · Painted cube |
| Verbal ability | Prepositions · One-word substitution · Active and passive voice · Para jumbles · Reading comprehension |
| Pseudocode and SP coding | Recursion · Bitwise operators · Longest increasing subsequence in O(n log n), with running Python code |
| Interview | Stack vs queue · Polymorphism with code · Learning something new quickly (HR) · Talking about a failure (HR) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 4-week plan · How AI is changing Infosys hiring |

## Get the full Infosys chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Infosys. © 2026 NeoTridhi Private Limited.</sub>
