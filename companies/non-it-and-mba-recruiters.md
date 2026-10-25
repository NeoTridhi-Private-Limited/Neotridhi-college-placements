<p align="center"><b>Non-IT and MBA recruiters</b></p>

# Non-IT and MBA recruiters: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Non-IT and MBA recruiters chapter covers banks and financial services, consulting, FMCG and analytics,
> and has 40+ questions with worked solutions, a 6-week plan, common traps and interview answers. [See how to get it](#get-the-full-non-it-and-mba-recruiters-chapter).

[Back to all companies](../README.md#companies)

---

## Money, customers and data

An IT test asks, "Can you build it?" These recruiters ask, "Can you think about money, customers and data?"
A kirana shop owner deciding how much stock to buy before Diwali is doing a mini case interview in his head.

```
Public sector banks (IBPS PO, SBI PO):  Prelims --> Mains (with a descriptive English part) --> Interview
RBI (Grade B officer):                  Phase I --> Phase II --> Interview
Private banks and financial services:   Aptitude test --> GD --> Interviews (sales, credit, operations roles)
Consulting:                             Online assessment or resume shortlist --> Case interviews --> Fit/behaviour interviews
FMCG (management trainee programmes):   Online test --> GD / case --> Panel interviews --> Final round
Analytics:                              Aptitude + statistics + SQL/Excel test --> Case or puzzle round --> Interviews
```

## Exams and selection rounds (widely reported; varies by cycle)

| Exam / sector | Widely reported pattern (approximate) | Official source to check |
|---|---|---|
| IBPS PO Prelims | English, Quantitative Aptitude, Reasoning; about 100 questions in about 60 minutes with sectional timing | IBPS Information Handout for the current cycle |
| IBPS PO Mains | Reasoning and Computer Aptitude, Data Analysis and Interpretation, General/Economy/Banking Awareness, English, plus a descriptive test | IBPS Information Handout |
| SBI PO | Similar three-stage structure; details in the SBI notification | SBI careers page |
| Wrong answers | Official IBPS handouts state a penalty of one-fourth of the marks for a wrong answer in objective tests | Read the handout for your exam |
| Consulting case interviews | 30-45 minute business problem discussions | Firm's official case-prep pages |
| FMCG management trainee | Aptitude + GD + case + panel interviews | Company careers page |
| Analytics firms | Aptitude, statistics, SQL/Excel, puzzles, case | Company careers page |

## Official links

| Link | What it is |
|---|---|
| [IBPS](https://www.ibps.in/) | Official site for IBPS PO, Clerk, SO and RRB exams: notifications and Information Handouts (with sample questions). |
| [SBI Careers](https://sbi.bank.in/web/careers) | Official SBI recruitment page (sbi.co.in/web/careers redirects here). |
| [Bain: case interview prep](https://www.bain.com/careers/hiring-process/case-interview/) | Official Bain case-prep hub with practice cases. |
| [BCG: case interview preparation](https://careers.bcg.com/global/en/case-interview-preparation) | Official BCG case-prep page. |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of these recruiters' tests and interviews, with new numbers and wording.
All banks, branches, rates and figures are **hypothetical**.

**1. (Quantitative aptitude: percentages)** Anitha's salary is 25% more than Bharath's. By what percentage is Bharath's salary less than Anitha's?
(a) 25% (b) 20% (c) 22.5% (d) 18% (e) 15%

<details><summary>Solution</summary>

Let Bharath = 100. Anitha = 125. Difference = 25, compared with Anitha's 125: 25/125 x 100 = **(b) 20%**.
Shortcut: if A is r% more than B, then B is r/(100 + r) x 100 % less than A: 25/125 = 20%.

</details>

**2. (Reasoning: inequality)** Statements: M >= N > O, P < O <= Q.
Conclusions: I. M > Q  II. P < N
(a) only I follows (b) only II follows (c) either I or II follows (d) neither follows (e) both follow.

<details><summary>Solution</summary>

I: M > O and Q >= O. Both are above O, but M and Q are never compared. Does not follow.
II: P < O < N, so P < N. Follows. Answer **(b) only II follows**.

</details>

**3. (Bank English: error spotting, fixed pairs)** Find the part with the error.
"Hardly had the RBI announced (a) / the policy than (b) / the markets started (c) / reacting sharply. (d) / No error (e)"

<details><summary>Solution</summary>

"Hardly" (and "scarcely") pair with **when**, not "than". "No sooner" pairs with "than". Correct: "...announced the policy when the markets started reacting sharply." Answer **(b)**.

</details>

**4. (Analytics: Excel)** A sheet of loan applications (amounts in Rs lakh) is in A1:D9:

| | A: Branch | B: Product | C: Amount | D: Status |
|---|---|---|---|---|
| 2 | Guntur | Home | 25 | Approved |
| 3 | Nellore | Home | 30 | Approved |
| 4 | Guntur | Car | 8 | Approved |
| 5 | Guntur | Home | 18 | Rejected |
| 6 | Guntur | Home | 40 | Approved |
| 7 | Nellore | Car | 6 | Rejected |
| 8 | Guntur | Personal | 3 | Approved |
| 9 | Guntur | Home | 12 | Approved |

Write one formula for the total APPROVED HOME loan amount in GUNTUR, and one for how many such loans there are. What are the results?

<details><summary>Solution</summary>

```
=SUMIFS(C2:C9, A2:A9, "Guntur", B2:B9, "Home", D2:D9, "Approved")
=COUNTIFS(A2:A9, "Guntur", B2:B9, "Home", D2:D9, "Approved")
```
SUMIFS takes the sum range first, then pairs of (criteria range, criteria). Rows 2, 6 and 9 match, so the results are **77** (Rs lakh) and **3**.
(Excel is not run here; we checked the same filter in Python.)

```python
rows = [("Guntur", "Home", 25, "Approved"), ("Nellore", "Home", 30, "Approved"),
        ("Guntur", "Car", 8, "Approved"), ("Guntur", "Home", 18, "Rejected"),
        ("Guntur", "Home", 40, "Approved"), ("Nellore", "Car", 6, "Rejected"),
        ("Guntur", "Personal", 3, "Approved"), ("Guntur", "Home", 12, "Approved")]
match = [amt for b, p, amt, s in rows if (b, p, s) == ("Guntur", "Home", "Approved")]
print(sum(match), len(match))
# Output:
# 77 3
```
Trap: forgetting the Status condition adds the rejected Rs 18 lakh and gives 95.

</details>

**5. (Interview: banking concept)** "What is an NPA? How is the gross NPA ratio different from the net NPA ratio?"

<details><summary>Solution</summary>

- An **NPA (non-performing asset)** is a loan that has stopped "performing", meaning the borrower has stopped paying. Under RBI's prudential norms, a term loan generally becomes an NPA when interest or an instalment stays overdue for more than 90 days. (Check the latest RBI master circular for the exact rules for each loan type.)
- **Gross NPA ratio** = gross NPAs / gross advances (all loans given).
- **Net NPA ratio** = (gross NPAs - provisions) / (gross advances - provisions). Provisions are money the bank has already set aside for expected losses.

Hypothetical example: gross advances Rs 50,000 crore, gross NPAs Rs 2,000 crore, provisions Rs 1,200 crore.
Gross NPA ratio = 2,000 / 50,000 = 4%. Net NPA ratio = 800 / 48,800 = about 1.64%.

Why it matters: an NPA earns no interest, and provisions reduce profit, so high NPAs limit how much the bank can lend.

</details>

---

## 🔒 In the full Non-IT and MBA recruiters chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative aptitude and data interpretation | Simplification · Approximation · Quadratic equations · Number series · Simple interest in two parts · Probability · A data-interpretation table (3 questions) |
| Reasoning | Inequality with "either-or" · Syllogism · Syllogism with possibility · Floor arrangement puzzle · Months puzzle |
| Bank English | Subject-verb agreement · Double fillers · Vocabulary filler · Para jumbles (2 questions) |
| Analytics: SQL, Python and a guesstimate | SQL with GROUP BY and HAVING, with a run result · EMI calculation, with running Python code · A market-sizing guesstimate |
| Interview | A fully worked profit-tree case · Why an MBA (HR) · Why banking, and not an IT job (HR) |
| Also in the chapter | 10 more sample questions with answers · An official consulting practice case, worked step by step · Questions in the style of the public exams · Role tracks by sector · Common traps · A 6-week plan · How AI is changing these recruiters' hiring |

## Get the full Non-IT and MBA recruiters chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by any of the recruiters or exam bodies named here. © 2026 NeoTridhi Private Limited.</sub>
