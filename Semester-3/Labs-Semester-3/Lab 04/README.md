# Lab 04 – Hypothesis Testing (Z-Test and t-Test)

**Name:** Francis Reuben R  
**USN:** 1RUA25CSE0168  
**Section:** G  
**Experiment:** 4  
**Title:** Hypothesis Testing with Z-Test and t-Test

## Objective

Run one-sample Z-tests and t-tests at α = 0.05 for left-tailed, right-tailed, and two-tailed alternatives. For each test, state H0 and H1, compute the statistic, critical value, and p-value, then decide whether to reject H0.

## Notebooks

| File | What it does |
|---|---|
| `Lab-4.ipynb` | Taught notebook: six worked examples (battery life, coaching scores, bottle filling, chocolate weight, teaching method, plant height) plus three practice questions |
| `Lab4_ZtTest_Assignment.ipynb` | Submitted assignment (100 marks): Z and t tests on a 40-student table (sleep, screen time, exam score, attendance, study hours, commute) |

## Figures

| File | Role |
|---|---|
| `hypothesis_testing_decision.png` | Two-tailed rejection regions, α, and the p-value decision rule |
| `type_i_type_ii_errors.png` | Type I (α) and Type II (β) error table |

## Run

```bash
pip install -r ../../../requirements.txt
jupyter notebook Lab-4.ipynb
jupyter notebook Lab4_ZtTest_Assignment.ipynb
```

Run `Lab-4.ipynb` first. The assignment notebook uses the starter dataset in the notebook (no CSV). Restart and run all before opening the assignment.

## Assignment results (α = 0.05)

| Q | Test | Tail | Decision |
|---|---|---|---|
| Q1 sleep hours | Z | Left | Reject H0 |
| Q2 screen time | Z | Right | Reject H0 |
| Q3 exam score | Z | Two | Fail to reject H0 |
| Q4 attendance (Section B) | t | Left | Fail to reject H0 |
| Q5 study hours (Section A) | t | Right | Reject H0 |
| Q6 commute (Section C) | t | Two | Reject H0 |

Classroom submission was the `.ipynb` only (LMS). This folder is the course repo copy.
