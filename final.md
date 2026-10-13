---
layout: post
title: MCQ Reflection
permalink: /mcq/
Author: Laya Balaji
comments: true
---

## Introduction

This reflection covers AP CSA Practice Exam 1 (MCQ), which I took at the start of the school year as a baseline. I scored **32/42 (about 76%)**. Going through my 10 missed questions, I noticed that most of my mistakes weren't from not knowing the concept. They came from tracing code too quickly: stopping a loop one iteration early, forgetting how integer division and casting work, or reading a condition backwards. This page breaks down what I missed, which units those mistakes come from, and my plan to improve as we move through the course.

---

## MCQ Reflection

| # | Topic | Reflection |
|---|---|---|
| 1 | Values after assignments | I chose `20 200` but the answer was `10 200`. The line `x = y;` changes `x` to 10 before `y = temp * x;` runs, so `y` becomes 20 × 10 = 200 and `x` stays 10. I forgot that `x` had already been reassigned. |
| 8 | Division with int casting | I chose `0.4, 0.4` but the answer was `0.4, 0.0`. In `(int) w / x`, the cast applies only to `w`, so it's 2 / 5.0 = 0.4. In `(int) (w / x)`, the division happens first (0.4), then the cast truncates it to 0, which becomes 0.0 when stored in a `double`. Parentheses decide what the cast applies to. |
| 12 | Modify private variable in Pair class | I chose a `public int setY` method that just returns `num`, but that never changes `y`. A mutator has to assign to the instance variable, like `public void setY(int num) { y = num; }`. Returning a value doesn't modify anything. |
| 15 | Substrings within while loop | I chose `ookout out` but the answer was `ookout okout out`. After the first print, `str.substring(1)` gives `"okout"`, where `"o"` is at index 0, so it prints `"okout"` too. I skipped the iteration where `indexOf` returned 0. |
| 20 | Division and modulus in loop | I chose 13 but the answer was 12. The loop goes 100 → 50 → 25 → 12, and 25 is still divisible by 5 so it runs one more time. Integer division truncates (`25 / 2 = 12`); it never rounds up. |
| 25 | Static variable in Shoe class | The answer was 2. `count` is `static`, so all objects share one copy, but only the two-parameter constructor increments it. The no-argument constructor never touches `count`, so I need to check which constructors actually contain `count++`. |
| 27 | Course and club investigation | I chose Data set 2 but the answer was Data set 3. Data set 2 only covers photography club members and has no info on whether they took a CS course. Data set 3 lists every student's courses and clubs, so it's the only one that can compare CS students to non-CS students. |
| 29 | Recursive printNums method | I chose `40 -20 10` but the answer was `-80 40 -20 10`. −80 is still less than 50, so that call also prints. Only 160 stops the recursion. Since the recursive call comes before the print, values print in reverse order. |
| 35 | Method that traverses numbers | I chose the reverse of the correct answer. The method returns `false` as soon as any number is greater than the previous one, so it returns `true` only if the list is sorted from greatest to least. I need to read what triggers each return statement carefully. |
| 37 | Value returned by enigma | I chose "column `x`" but the answer was "row `x`." `values[x]` is a whole row of the 2D array, since the first index is the row. The method counts how many times `target` appears in that row. |

### Patterns in My Mistakes

- **Stopping a trace too early (Q15, Q20, Q29):** In three questions, I missed the final iteration or recursive call. I should keep tracing until the condition is actually false.
- **Integer division and casting (Q8, Q20):** I need to remember that `int` division truncates and that a cast only applies to what's directly next to it.
- **Reading logic backwards (Q35, Q37):** I understood the code but mixed up rows and columns, or least-to-greatest and greatest-to-least.

### Misses by Unit

Each missed question is grouped by the College Board unit it was tagged with. Exam weightings are from College Board's AP CSA Course at a Glance.

| Unit | Questions Missed | # Missed | AP Exam Weighting |
|---|---|:---:|:---:|
| Unit 1: Using Objects and Methods | Q1, Q8 | 2 | 15–25% |
| Unit 2: Selection and Iteration | Q15, Q20 | 2 | 25–35% |
| Unit 3: Class Creation | Q12, Q25 | 2 | 10–18% |
| Unit 4: Data Collections | Q27, Q29, Q35, Q37 | 4 | 30–40% |

**What this tells me:** Unit 4 had the most misses, but we haven't covered it in class yet, so some of those were expected. The misses I care about most right now are in Units 1 and 2. That material comes first in the course, and it's the foundation for everything after it. Unit 2 is also one of the most heavily weighted units on the exam, so fixing my loop tracing early will pay off all year.

---

# AP CSA Study Plan

## Plan for the Year

- **Units 1–2 (now):** Fix my High Priority mistakes in casting and loop tracing while we're covering this material in class.
- **Unit 3:** Focus on the Medium Priority class topics (mutators and `static` variables) when we reach them.
- **Unit 4:** Revisit recursion, ArrayList, and 2D array mistakes once we learn them, then retake similar questions to check that I've improved.
- **After every practice MCQ:** Add my score to the tracker below and update this reflection with any new mistake patterns.

---

## High Priority

- **2.7 while Loops** — Trace loops with a table of variable values after every iteration. Always check the condition one more time before stopping.
- **4.16 Recursion** — Practice finding the base case and determining whether output happens before or after the recursive call.
- **1.5 Casting and Range of Variables** — Review how `(int)` truncates, how parentheses change what gets cast, and when `int` values are widened to `double`.
- **4.10 Implementing ArrayList Algorithms** — Practice describing what a method does by testing it on small sorted and unsorted inputs.

---

## Medium Priority

- **4.12 2D Array Traversals** — Remember `arr[row][col]`, and that `arr[x]` refers to an entire row.
- **3.5 Methods: How to Write Them** — Review accessor vs. mutator methods. A setter has to assign to the instance variable.
- **3.7 Class Variables and Methods** — Remember that a `static` variable is shared by every object of the class.
- **1.15 String Manipulation** — Practice `substring` and `indexOf`, especially when `indexOf` returns 0 or −1.

---

## Low Priority

- **1.4 Assignment Statements and Input** — Track every variable's value line by line, especially when swapping.
- **4.2 Introduction to Using Data Sets** — Check whether a data set actually contains every piece of information the question needs.

---

## Progress Tracker

I'll fill this in after each practice MCQ so I can see whether my score and my mistake patterns are improving over the year.

| Practice Test | Date | Score | Most Common Mistake |
|---|---|:---:|---|
| Practice Exam 1 MCQ | Oct 9 | 32/42 (76%) | Stopping a trace too early |
| | | | |
| | | | |

---

## Future Goals

- Raise my practice exam score from 32/42 to at least 36/42 on the next full MCQ
- Trace every loop and recursive call on paper until the condition is actually false, instead of stopping early
- Write out integer division and casting step by step, checking what each cast applies to
- Reread "returns true if" and row vs. column questions before choosing an answer, so I don't pick the reverse
- Review every missed question after each practice test and add it to this reflection