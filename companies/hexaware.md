<p align="center"><b>Hexaware</b></p>

# Hexaware: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Hexaware chapter has 19 questions with worked solutions, a 4-week plan,
> common traps and what each round looks for. [See how to get it](#get-the-full-hexaware-chapter).

[Back to all companies](../README.md#companies)

---

## One trip, two possible tickets

Think of a two-level bus ticket: ordinary and AC. Prep sites report that Hexaware campus drives work like this. Everyone writes the same
test. If you also do well in an extra coding round, you may be offered the higher track (reported as **PGET**). If not, you can still get the
regular track (reported as **GET**). One trip, two possible tickets.

Hexaware's official careers page does not list the stages. Commonly reported stages (approximate; they change by drive):

```
Register / campus shortlist --> Online test (aptitude + technical) --> Communication test --> Coding test (for the higher track) --> Technical interview --> HR interview --> Offer
```

## Hexaware online test (commonly reported; varies by drive)

Not official. Prep sites report the following; treat all numbers as approximate.

| Section | Commonly reported topics | Approx. size |
|---|---|---|
| Quantitative aptitude | Number system, percentages, profit and loss, ratio, work, speed, interest, probability | about 20 questions |
| Logical reasoning | Series, coding-decoding, blood relations, seating, syllogisms, data interpretation | about 20 questions |
| Verbal ability | Sentence correction, synonyms, antonyms, fill in the blanks, reading comprehension | about 20 questions |
| Technical MCQs | C/C++/Java basics, OOP, DBMS, OS, networks, data structures | varies |
| Coding | Arrays, strings, sorting, searching, simple recursion | 2-3 problems |

## Official links

| Link | What it is |
|---|---|
| [Why Join Hexaware](https://hexaware.com/about-us/join-hexaware/) | Official careers landing page: culture, benefits, links to the jobs portal. |
| [Hexaware Jobs Portal](https://jobs.hexaware.com/) | Official job listings ("Careers at Hexaware Technologies"). |
| [Programs and Learning (HexaVarsity)](https://hexaware.com/about-us/programs-learning/) | Official page describing Mavericks (graduate programme), HFLX (management trainees) and other learning programmes. |
| [Beware of Fake Job Offer](https://hexaware.com/beware-of-fake-job-offer/) | Official warning: Hexaware never asks for money; offers do not come from free email services; report to careers@hexaware.com. |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Hexaware test, with new numbers and wording.

**1. (Quantitative aptitude: probability)** A die is rolled twice. What is the probability that the **product** of the two numbers is even? (a) 1/2 (b) 3/4 (c) 1/4 (d) 2/3

<details><summary>Solution</summary>

The product is odd only when both numbers are odd: (3/6) x (3/6) = 1/4. So even = 1 - 1/4 = **(b) 3/4**. (Count check: 27 of the 36 pairs give an even product.)

</details>

**2. (Logical reasoning: calendar)** 1 January 2026 was a Thursday. What day was 1 March 2026? (a) Saturday (b) Sunday (c) Monday (d) Friday

<details><summary>Solution</summary>

Days after 1 Jan up to 1 Mar = 31 (January) + 28 (February, 2026 is not a leap year) = 59. 59 = 7 x 8 + 3. Thursday + 3 = **(b) Sunday**.

</details>

**3. (Verbal: articles)** "He is ___ honest man and ___ useful member of the team." (a) a, an (b) an, a (c) an, an (d) a, a

<details><summary>Solution</summary>

"Honest" starts with a vowel **sound** (the h is silent): "an". "Useful" starts with a "yoo" sound (a consonant sound): "a". **(b) an, a**.

</details>

**4. (Technical: SQL)** Which command removes a table completely, including its structure? (a) DELETE (b) TRUNCATE (c) DROP (d) REMOVE

<details><summary>Solution</summary>

**(c) DROP.** DELETE removes chosen rows; TRUNCATE removes all rows but keeps the table; DROP removes the table itself.

</details>

**5. (Coding: longest run)** A hostel's power-cut log for 9 days is 1, 1, 0, 1, 1, 1, 0, 0, 1 (1 = power cut that day). Find the longest run of consecutive power-cut days.

<details><summary>Solution</summary>

Keep a running count; reset it at every 0.

```python
def longest_run(log):
    best = cur = 0
    for day in log:
        cur = cur + 1 if day == 1 else 0
        best = max(best, cur)
    return best

print(longest_run([1, 1, 0, 1, 1, 1, 0, 0, 1]))
print(longest_run([0, 0, 0]))
# Output: 3
# 0
```

</details>

---

## 🔒 In the full Hexaware chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude | Time and work · Divisibility · Trains in opposite directions · Partnership · Data interpretation |
| Logical reasoning | Analogy · Odd one out · Ranking |
| Verbal | Synonyms · Question tags |
| Technical | OOP concepts · Process states · C output with post-increment |
| Coding | Pair sum, with running Python code |
| Also in the chapter | Role tracks (GET, PGET and official programmes) · What each round looks for · Common traps · A 4-week plan · How AI is changing Hexaware hiring |

## Get the full Hexaware chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Hexaware. © 2026 NeoTridhi Private Limited.</sub>
