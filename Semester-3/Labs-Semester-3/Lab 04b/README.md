# Lab 04b – Probability Distributions

**Name:** Francis Reuben R  
**USN:** 1RUA25CSE0168  
**Section:** G  
**Experiment:** 4(b)  
**Title:** Bernoulli, Binomial, Poisson, Normal, and Uniform Distributions

## Objective

Choose the distribution from the wording of a scenario (counted vs measured), compute the probability by hand, check it with `scipy.stats`, and plot a PMF or a PDF with labelled axes.

## Notebooks

| File | What it does |
|---|---|
| `Lab-4-b.ipynb` | Taught notebook: penalty kick (Bernoulli), faulty bulbs (Binomial), hospital emergencies (Poisson), packet weight (Normal), random numbers on [10, 20] (Uniform) |
| `Lab-4-b-Assignment.ipynb` | Assignment (50 marks): library gate, attendance estimate, MCQ quiz, help-desk emails, night-shift server errors, phone battery, coffee fill, campus shuttle |
| `1RUA25CSE0168_Francis_Reuben_R_Lab4b.ipynb` | Same assignment notebook, named for upload |
| `Record_Exp4b_Francis_Reuben_R.pdf` | Lab record: objective, pipeline, taught results, assignment results |

## Run

```bash
pip install -r ../../../requirements.txt
jupyter notebook Lab-4-b.ipynb
jupyter notebook Lab-4-b-Assignment.ipynb
```

Run `Lab-4-b.ipynb` first. Neither notebook uses a CSV. The assignment setup cell is unchanged.

## Taught results

| Question | Distribution | Hand result | scipy |
|---|---|---|---|
| Q1 penalty | Bernoulli, p = 0.8 | P(score) = 0.8000, var = 0.1600 | match |
| Q2 bulbs | Binomial, n = 15, p = 0.1 | P(X=2) = 0.2669, mean = 1.5, var = 1.35 | match |
| Q3 emergencies | Poisson, lambda = 4 | P(X=0) = 0.0183, P(X=4) = 0.1954 | match |
| Q4 packet weight | Normal, mean 500 g, sd 5 g | P(495 to 505 g) = 0.6827 | match |
| Q5 random numbers | Uniform on [10, 20] | mean = 15, var = 8.3333 | match |

## Assignment results

| Q | Distribution | Result |
|---|---|---|
| Q1 library gate | Bernoulli, p = 0.92 | P(X=1) = 0.9200, var = 0.0736 |
| Q2 attendance | Bernoulli, p = 1740/2000 = 0.87 | var = 0.1131; largest Bernoulli var is 0.25 at p = 0.5; 2,000 simulations gave proportion 0.8675 |
| Q3 quiz | Binomial, n = 12, p = 0.25 | C(12,5) = 792, P(X=5) = 0.1032, mean = 3, var = 2.25 |
| Q5 emails | Poisson, lambda = 3 | P(X=0) = 0.0498, P(X=2) = 0.2241 by the given e^(-3); scipy prints 0.2240. Smallest k with CDF at least 0.95 is k = 6 |
| Q6 night shift | Poisson, lambda = 12 | P(X=0) = 6.1442e-06, P(X>18) = 0.0374 via `poisson.sf` |
| Q7 battery | Normal, mean 18 h, sd 1.5 h | Z(15) = -2; 95% rule interval is 15 to 21 hours |
| Q8 coffee fill | Normal, mean 200 ml | sigma = 10/1.96 = 5.1020 ml by hand; scipy `norm.ppf` gives 5.1021 ml. 1st percentile = 188.1307 ml. P(X<190) = 0.0250 |
| Q9 shuttle | Uniform on [0, 15] | mean = 7.5 min, var = 18.75 |

The issued assignment file has no question text for Q4 or Q10, and Q3(c), Q6(c), Q7(c), Q8(c) and Q9(b) stop mid-sentence. The notebook answers every part that is present.
