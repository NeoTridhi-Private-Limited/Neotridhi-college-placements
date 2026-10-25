<p align="center"><img src="../assets/logos/cognizant.svg" alt="Cognizant" height="70"></p>

# Cognizant: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Cognizant chapter has 40+ questions with worked solutions, a 3-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-cognizant-chapter).

[Back to all companies](../README.md#companies)

---

## One depot, buses of different speeds

GenC is like a bus depot with buses of different speeds. Everyone enters the same depot (the GenC process). Your scores in the coding part
decide whether you board the regular bus (**GenC**), the express (**GenC Next**) or a specialist bus (**GenC Pro**, for specific skills).
Track names appear differently in different years: older material calls one track **GenC Elevate**. Follow the name in your own invitation.

```
Application (campus drive or off-campus) --> Initial screening --> Assessment(s) --> Interview(s) --> Result
```

The official GenC page says the assessments "evaluate your communication skills, aptitude and/or technical skills", and that there are "No service bonds".

## GenC assessment stages (commonly reported; varies by drive)

| Stage | Approx. content | Notes |
|---|---|---|
| Aptitude | Quant (number system, time and work), logical (coding-decoding, seating), verbal | Reported to run on AMCAT-style platforms in some drives |
| Communication | Reading, listening, speaking, grammar | Often AI-scored |
| Technical / coding | SQL queries, coding problems; harder DSA for GenC Next | Number of problems varies |
| Technical interview | Language basics, SQL, project | Plus HR questions |

## Official links

| Link | What it is |
|---|---|
| [GenC program](https://careers.cognizant.com/india-en/pathways-to-cognizant/genc-program/) | Official GenC page: steps, assessments, no service bonds, Digital Honors |
| [Cognizant Careers India](https://careers.cognizant.com/india-en/) | Official careers home for India |
| [How we hire](https://careers.cognizant.com/india-en/pathways-to-cognizant/how-we-hire/) | Official hiring overview |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Cognizant GenC tests, with new numbers and wording.

**1. (Quantitative aptitude: percentages)** Rani's stipend is raised by 20% and later cut by 20%. What is the net change?
(a) no change (b) 4% decrease (c) 4% increase (d) 2% decrease

<details><summary>Solution</summary>

1.20 x 0.80 = 0.96, so **(b) 4% decrease**. Trap: +20% and -20% do not cancel because the second 20% is on a bigger amount.

</details>

**2. (Quantitative aptitude: mixtures)** A kirana owner mixes rice costing Rs 40/kg with rice costing Rs 55/kg to get a mix worth Rs 45/kg.
In what ratio should he mix them? (a) 1 : 2 (b) 2 : 1 (c) 3 : 1 (d) 2 : 3

<details><summary>Solution</summary>

Alligation: cheaper : dearer = (55 - 45) : (45 - 40) = 10 : 5 = **(b) 2 : 1**.
Check: (2 x 40 + 1 x 55) / 3 = 135 / 3 = 45.

</details>

**3. (Logical reasoning: blood relations)** Pointing to a boy, Neha says, "His mother is the only daughter of my mother." How is Neha related to the boy?
(a) sister (b) aunt (c) mother (d) cousin

<details><summary>Solution</summary>

"The only daughter of my mother" is Neha herself (Neha is a girl, and she is the only daughter). So the boy's mother is Neha: **(c) mother**.
Trap: drawing an aunt into the family tree. Always check whether the description points back to the speaker.

</details>

**4. (Verbal: subject-verb agreement)** "Neither of the two answers ___ correct."
(a) are (b) were (c) is (d) have been

<details><summary>Solution</summary>

"Neither of" takes a singular verb in formal English: **(c) is**.

</details>

**5. (SQL: GROUP BY, HAVING, ORDER BY)** Table `orders`:

| order_id | customer | city | amount |
|---|---|---|---|
| 1 | Ramya | Chennai | 450 |
| 2 | Suresh | Hyderabad | 1200 |
| 3 | Ramya | Chennai | 700 |
| 4 | Imran | Pune | 300 |
| 5 | Kavya | Hyderabad | 250 |
| 6 | Teja | Pune | 500 |
| 7 | Anil | Chennai | 100 |

Write a query to show each city's total order amount, only for cities whose total is more than 1000, biggest first.

<details><summary>Solution</summary>

```sql
SELECT city, SUM(amount) AS total
FROM orders
GROUP BY city
HAVING SUM(amount) > 1000
ORDER BY total DESC;
```
Result (run in SQLite):

| city | total |
|---|---|
| Hyderabad | 1450 |
| Chennai | 1250 |

Pune's total is 800, so HAVING removes it. Remember: WHERE filters rows before grouping; HAVING filters groups after.

</details>

---

## 🔒 In the full Cognizant chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude | Number of factors · Unit digit of powers · Time and work · Profit and loss · Average speed · Boats and streams · Arrangements with vowels together · Trailing zeros in 100! |
| Logical reasoning | Coding-decoding with alternate shifts · Circular seating · Wrong number in a series · Syllogism · Data sufficiency |
| Verbal and communication | Synonyms · Error spotting · Tenses · Business email subject line · Idioms |
| SQL and coding | LEFT JOIN to find missing rows · Missing number in an array · Longest substring without repeats (GenC Next), with running Python code |
| Interview | Primary key vs unique key · Normalisation (1NF, 2NF, 3NF) · Training in a technology you did not choose (HR) · Learning outside the syllabus (HR) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 3-week plan · How AI is changing Cognizant hiring |

## Get the full Cognizant chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Cognizant. © 2026 NeoTridhi Private Limited.</sub>
