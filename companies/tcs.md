<p align="center"><img src="../assets/logos/tcs.svg" alt="TCS" height="70"></p>

# TCS: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full TCS chapter has 40+ questions with worked solutions, a 4-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-tcs-chapter).

[Back to all companies](../README.md#companies)

---

## One test, three windows

Think of the NQT like a railway ticket counter with three windows. Everyone stands in the same queue and writes the same test.
Your score decides the window: **Ninja** (general window), **Digital** (faster window) or **Prime** (the Tatkal window, for the top scorers).
You do not pick a track. Your performance picks it for you.

```
Register on TCS NextStep  -->  TCS NQT (online, proctored)  -->  Interview(s)  -->  Offer letter  -->  Joining + training
                               Foundation + Advanced            Technical + Managerial + HR
                                                                (often in one sitting)
```

## TCS NQT test pattern (official TCS iON NQT - IT page)

| Part | Sections | Questions | Time |
|---|---|---|---|
| Part A: Foundation | Numerical Ability, Verbal Ability, Reasoning Ability | 65 | 75 min |
| Part B: Advanced | Advanced Quantitative and Reasoning Ability, Advanced Coding | 16 | 115 min |
| Psychometric | Personality and motivation (not counted in the 81 questions) | varies | 30 min |
| **Total** | | **81** | **220 min** (including psychometric) |

No negative marking. Tests are in English. Your NQT score is valid for 2 years, and you may retake to improve it.

## Official links

| Link | What it is |
|---|---|
| [TCS iON National Qualifier Test](https://www.tcsion.com/hub/national-qualifier-test/) | Official NQT home: who can take it, score validity, retakes, sample test button |
| [TCS iON NQT - IT](https://www.tcsion.com/hub/national-qualifier-test/it-career-readiness-pack/) | Official structure of the IT version |
| [TCS NextStep](https://nextstep.tcs.com/) | Official TCS fresher registration portal |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the TCS NQT, with new numbers and wording.

**1. (Numerical ability: profit and loss)** A shopkeeper buys 20 kg of sugar at Rs 40 per kg. He sells 15 kg at Rs 48 per kg and the remaining 5 kg (a little damp) at Rs 36 per kg. Find his profit percentage.
(a) 10% (b) 12% (c) 12.5% (d) 15%

<details><summary>Solution</summary>

Cost price = 20 x 40 = Rs 800.
Selling price = 15 x 48 + 5 x 36 = 720 + 180 = Rs 900.
Profit = 900 - 800 = Rs 100. Profit % = 100 / 800 x 100 = **12.5%**. Answer: **(c)**.

</details>

**2. (Advanced quant: probability)** A bag has 4 red, 5 green and 3 blue balls. Two balls are taken out together at random. What is the probability that both are of the same colour?
(a) 19/66 (b) 1/3 (c) 19/132 (d) 5/22

<details><summary>Solution</summary>

Total ways to pick 2 from 12 = 12C2 = 66.
Both red = 4C2 = 6. Both green = 5C2 = 10. Both blue = 3C2 = 3. Favourable = 6 + 10 + 3 = 19.
Probability = **19/66**. Answer: **(a)**.

</details>

**3. (Reasoning: coding-decoding)** In a code language, TRAIN is written as OJBSU. How is METRO written in that code?
(a) PSUFN (b) NFUSP (c) PSUEN (d) OSUFN

<details><summary>Solution</summary>

Find the rule: write TRAIN backwards: N I A R T. Move each letter one step forward: O J B S U. That matches.
METRO backwards: O R T E M. One step forward: P S U F N = **PSUFN**. Answer: **(a)**.
(b) forgets to reverse; (c) and (d) have one wrong letter each.

</details>

**4. (Verbal: subject-verb agreement)** Find the part with the error: "Neither the manager (a) / nor the team members (b) / was ready (c) / for the audit (d)."

<details><summary>Solution</summary>

With "neither ... nor", the verb agrees with the subject **nearer** to it. The nearer subject is "the team members" (plural), so the verb should be "were".
Error in part **(c)**. Correct: "Neither the manager nor the team members **were** ready for the audit."

</details>

**5. (Advanced coding: run-length compression)** Compress a string by writing each character followed by how many times it repeats in a row.
Example: `ppqqqrsssst` gives `p2q3r1s4t1`.

<details><summary>Solution</summary>

Walk through the string, counting while the character stays the same. When it changes, write the character and its count. After the loop, write the last group.

```python
def compress(s):
    if not s:
        return ""
    out = []
    count = 1
    for i in range(1, len(s)):
        if s[i] == s[i - 1]:
            count += 1
        else:
            out.append(s[i - 1] + str(count))
            count = 1
    out.append(s[-1] + str(count))   # do not forget the last group
    return "".join(out)

print(compress("ppqqqrsssst"))
print(compress("z"))
# Output:
# p2q3r1s4t1
# z1
```

Common bug: forgetting the last group (you would print `p2q3r1s4` and lose `t1`).

</details>

---

## 🔒 In the full TCS chapter

| Section | Locked questions (topics) |
|---|---|
| Numerical ability and advanced quant | Percentages · Trains and platforms · Unit digit of powers · Averages · Pipes and cisterns · Compound vs simple interest · Arrangements with a condition · HCF with remainders |
| Reasoning ability | Number series · Blood relations · Circular seating · Syllogism · Directions |
| Verbal ability | Synonyms · Antonyms · Sentence completion · Para jumbles · Reading comprehension |
| Advanced coding | Cricket over summary (strings) · Second largest distinct value · Subarrays with a given sum using prefix sums, with running Python code |
| Interview | Array vs linked list · WHERE vs HAVING in SQL · Disagreeing with a teammate (managerial) · Working to a tight deadline (managerial) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 4-week plan · How AI is changing TCS hiring |

## Get the full TCS chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by TCS. © 2026 NeoTridhi Private Limited.</sub>
