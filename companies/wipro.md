<p align="center"><img src="../assets/logos/wipro.svg" alt="Wipro" height="70"></p>

# Wipro: placement preparation at a glance

> **Pattern as of October 2026 from public sources. Always check the official page before your test.**
> This page is a free preview of the NeoTridhi course. The full Wipro chapter has 40+ questions with worked solutions, a 3-week plan,
> common traps and interview answers. [See how to get it](#get-the-full-wipro-chapter).

[Back to all companies](../README.md#companies)

---

## Three courses, one sitting

The Wipro test is like a three-course thali: one plate of aptitude, one bowl of writing (an essay), and one dish of coding.
You must finish all three in one sitting. Missing one course (for example, a weak essay) can cost you the whole meal.
Most freshers come in through **Elite**; selected premier institutes also see the harder **Turbo** track.

```
Register (campus cell or Wipro careers) --> Online assessment --> Business discussion / technical interview --> HR --> Offer
                                            aptitude + essay + coding
```

## Elite online assessment (commonly reported; varies by drive)

| Section | Approx. content | Approx. time |
|---|---|---|
| Aptitude | Quantitative, logical reasoning, verbal ability | about 48-60 min |
| Written communication | One essay (a topic is given) | about 20 min |
| Online programming | 2 coding problems (any allowed language) | about 60 min |

Wipro does not publish one fixed pattern for all drives. **Check the official drive notice.**

## Official links

| Link | What it is |
|---|---|
| [Wipro Careers](https://careers.wipro.com/) | Official careers home |
| [Wipro Early Careers](https://careers.wipro.com/content/Early-Careers/?locale=en_US) | Official descriptions of Elite, Turbo, STAR, WILP, internships and MBA programmes |
| [Wipro Fraud Awareness](https://careers.wipro.com/content/Fraud-Awareness/?locale=en_US) | Official warning about fake job offers. Wipro never asks for money |

---

## Try 5 questions (solutions open)

All questions are original, written in the style of the Wipro Elite test, with new numbers and wording.

**1. (Quantitative: average speed)** A bus goes from Nellore to Tirupati at 40 km/h and comes back on the same road at 60 km/h. What is the average speed for the whole trip?
(a) 48 km/h (b) 50 km/h (c) 52 km/h (d) 45 km/h

<details><summary>Solution</summary>

For equal distances, average speed = 2xy / (x + y) = 2 x 40 x 60 / (40 + 60) = 4,800 / 100 = **48 km/h**. Answer: **(a)**.
Why not 50? The bus spends more time at the slower speed. Check with a distance of 120 km: 3 hours + 2 hours = 5 hours for 240 km = 48 km/h.

</details>

**2. (Quantitative: discount and profit)** An electronics shop marks a fan 40% above its cost price and then gives a 15% discount. What is the profit percentage?
(a) 19% (b) 25% (c) 21% (d) 15%

<details><summary>Solution</summary>

Let cost price = 100. Marked price = 140. Selling price = 140 x 0.85 = 119.
Profit = 19 on 100 = **19%**. Answer: **(a)**.
Trap: (b) 25% just subtracts 15 from 40. Discount is on the marked price, not on the cost.

</details>

**3. (Logical reasoning: ranking in a queue)** In a queue at a railway ticket counter, Ramesh is 9th from the front and Sita is 14th from the back. Ramesh is ahead of Sita, and there are exactly 4 people between them. How many people are in the queue?
(a) 23 (b) 26 (c) 27 (d) 28

<details><summary>Solution</summary>

Count from the front: 8 people before Ramesh, then Ramesh (9th), then 4 people, then Sita (position 9 + 4 + 1 = 14th from the front).
Sita is 14th from the back, so 13 people stand behind her. Total = 14 + 13 = **27**. Answer: **(c)**.
Formula: total = Ramesh's position + people between + Sita's position from the back = 9 + 4 + 14 = 27.

</details>

**4. (Verbal: error spotting)** Find the part with the error: "One of my friends (a) / are going (b) / to Hyderabad (c) / for the drive (d)."

<details><summary>Solution</summary>

The subject is "One" (singular), not "friends". So the verb must be singular: "is going".
Error in part **(b)**. Correct: "One of my friends **is** going to Hyderabad for the drive."

</details>

**5. (Coding: strings)** Check whether a sentence is a palindrome when you ignore case, spaces and punctuation. Print `True` or `False`.
Examples: `Malayalam` gives True; `Was it a car or a cat I saw?` gives True.

<details><summary>Solution</summary>

Keep only letters and digits, in lower case. Then compare from both ends with two pointers, moving inwards.

```python
def is_clean_palindrome(s):
    letters = [ch.lower() for ch in s if ch.isalnum()]
    i, j = 0, len(letters) - 1
    while i < j:
        if letters[i] != letters[j]:
            return False
        i += 1
        j -= 1
    return True

print(is_clean_palindrome("Malayalam"))
print(is_clean_palindrome("Was it a car or a cat I saw?"))
print(is_clean_palindrome("Wipro"))
# Output:
# True
# True
# False
```

Time O(n), extra space O(n) for the cleaned list. Trap: forgetting `.lower()`, so `M` and `m` do not match.

</details>

---

## 🔒 In the full Wipro chapter

| Section | Locked questions (topics) |
|---|---|
| Quantitative ability | Percentages · Simple interest · Averages · Ratio and proportion · Clocks · Calendars (odd days) · Compound interest · Committees with a condition |
| Logical reasoning | Odd one out · Coding-decoding with sentences · Number series · Directions with shadows · Linear seating |
| Verbal ability and written communication | Synonyms · Tenses · Para jumbles (email order) · A timed essay with a model answer and checklist · Editing a paragraph |
| Coding | Sum of even digits · Spiral order of a matrix · Merging overlapping bookings, with running Python code |
| Interview | Compiler vs interpreter · Normalisation (1NF, 2NF, 3NF) · Adapting to a big change (HR) · A mistake and how you fixed it (HR) |
| Also in the chapter | 10 more sample questions with answers · Questions in the style of the public exams · Common traps · A 3-week plan · How AI is changing Wipro hiring |

## Get the full Wipro chapter

The complete chapter, along with all 7 modules of the course and AI mock interviews on **NeoHireAI**, is available to subscribing colleges
and students. Contact **NeoTridhi** at [neotridhi.tech](https://neotridhi.tech/).

---
<sub>Company names and logos are trademarks of their respective owners. They are used here only to identify the companies whose public
recruitment processes this course prepares for. NeoTridhi is not affiliated with or endorsed by Wipro. © 2026 NeoTridhi Private Limited.</sub>
