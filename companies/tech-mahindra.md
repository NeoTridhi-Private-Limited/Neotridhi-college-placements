<p align="center"><img src="../assets/logos/tech-mahindra.svg" alt="Tech Mahindra" height="70"></p>

# Tech Mahindra: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Tech Mahindra chapter has 40+ questions with worked solutions, a 3-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-tech-mahindra-chapter).

[Back to all companies](../README.md#companies)

---

## Like a driving licence test

The Tech Mahindra process is like a driving licence test: a written test (aptitude and technical), a practical (coding), a talk with the
officer (interview) and a check of how you behave on the road (psychometric). You need all of them.

```
Register --> Online test (aptitude + technical + coding + English) --> Psychometric --> (some drives: spoken English / writing) --> Technical interview --> HR --> Offer
```

## Online test (two formats reported; your drive may use either)

| Format A (reported) | Approx. | Format B (reported) | Approx. |
|---|---|---|---|
| Aptitude (quant, logical, verbal) | 75 Q / 42 min | Aptitude + essay writing | about 60 min |
| Technical MCQs + 1 coding | 26 Q / 65 min | Programming and CS MCQs + 2 coding problems + psychometric | about 90 min |
| Communication (English) | about 18 Q / 20 min | AI-proctored spoken English | separate stage |
| Psychometric | untimed | | |

**Check the official drive notice** for the version you will get.

## Official links

| Link | What it is |
|---|---|
| [Tech Mahindra Careers](https://www.techmahindra.com/careers/) | Official careers home |
| [Tech Mahindra job portal](https://careers.techmahindra.com/) | Official job listings ("Join Us") |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Tech Mahindra test, with new numbers and wording.

**1. (Quantitative aptitude: percentages)** The price of sugar falls by 20%. How much MORE sugar can a family buy for the same money?
(a) 20% (b) 25% (c) 16.67% (d) 22%

<details><summary>Solution</summary>

New price = 0.8 of old. Same money buys 1 / 0.8 = 1.25 times as much: **(b) 25% more**.
Shortcut: fall of r% gives r / (100 - r) x 100 = 20/80 x 100 = 25%.

</details>

**2. (Quantitative aptitude: probability with dice)** Two dice are rolled. What is the probability that the sum is a prime number?
(a) 1/3 (b) 5/12 (c) 7/18 (d) 1/2

<details><summary>Solution</summary>

Prime sums possible: 2, 3, 5, 7, 11. Ways: 2 -> 1, 3 -> 2, 5 -> 4, 7 -> 6, 11 -> 2. Total = 15 of 36.
15/36 = **(b) 5/12**.

</details>

**3. (Logical reasoning: data sufficiency)** Is the whole number n divisible by 6?
I. n is divisible by 3. II. n is even.
(a) I alone (b) II alone (c) Both together (d) Not enough even together

<details><summary>Solution</summary>

6 = 2 x 3. I alone: 9 is divisible by 3 but not by 6. II alone: 4 is even but not divisible by 6. Together: divisible by 2 and 3, so by 6.
Answer **(c) Both together**.

</details>

**4. (English: error spotting)** Find the error: "The informations you shared in the mail were very useful."

<details><summary>Solution</summary>

"Information" is uncountable: no -s, singular verb. **"The information you shared in the mail was very useful."**

</details>

**5. (Coding: strings)** Check whether one string is a rotation of another. Tests: ("upipay", "payupi") -> True; ("upipay", "upiyap") -> False.

<details><summary>Solution</summary>

Trick: if b is a rotation of a, then b appears inside a + a, and the lengths match.

```python
def is_rotation(a, b):
    return len(a) == len(b) and b in a + a

print(is_rotation("upipay", "payupi"))
print(is_rotation("upipay", "upiyap"))
print(is_rotation("", ""))
# Output:
# True
# False
# True
```
"upipayupipay" contains "payupi", so the first is True.

</details>

---

## 🔒 In the full Tech Mahindra chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude | Simple interest from two amounts · Mixtures · Meeting time · Counting even numbers · Profit and loss · Ages · Averages · Compound interest doubling |
| Logical reasoning | Coding-decoding with numbers · Coded blood relations · Linear seating · Odd one out · Statement and assumption |
| English and essay | Synonyms · Phrasal verbs · Comparatives · Sentence order · Essay outline |
| Technical MCQs and coding | The call stack · Pseudocode loop with a step · Frequency sort, with running Python code |
| Interview | Bandwidth vs latency · Four pillars of OOP · A failure and what you learnt (HR) · Working under pressure (HR) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 3-week plan · How AI is changing Tech Mahindra hiring |

## Get the full Tech Mahindra chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Tech Mahindra. © 2026 NeoTridhi Private Limited.</sub>
