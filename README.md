<div align="center">

# Data Science Laboratory – Semester 3

**Francis Reuben R** · USN `1RUA25CSE0168` · Section G

[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)

</div>

---

Lab assignments for the **Data Science Laboratory** course (Semester 3, B.Tech CSE). Hands-on work in Python covering data collection, preprocessing, statistical analysis, and machine learning.

This repository currently publishes Experiment 1 (Data Collection), Experiment 2 (wrangling of a placement table and the Automobile dataset), Lab 03 (descriptive statistics on the student survey and gym membership tables), Lab 04 (one-sample Z-tests and t-tests), Lab 04b (probability distributions), and Lab 05 (linear regression for height-weight and food delivery time).

---

## Student

| Field | Value |
|---|---|
| Name | Francis Reuben R |
| USN | 1RUA25CSE0168 |
| Section | G |
| Programme | B.Tech Computer Science and Engineering |
| Course | Data Science Laboratory |
| Semester | 3 |

---

## Experiments

| Lab | Topic | Folder |
|---|---|---|
| 01 | Data Collection (Open-Meteo weather and air quality APIs, bookstore web scraping) | [`Semester-3/Labs-Semester-3/Lab 01`](Semester-3/Labs-Semester-3/Lab%2001) |
| 02 | Data Wrangling and Transformation | [`Semester-3/Labs-Semester-3/Exp 2`](Semester-3/Labs-Semester-3/Exp%202) |
| 02a | Student placement table (missing values, scaling, outliers, encoding) | [`Semester-3/Labs-Semester-3/Exp 2/Exp 2a`](Semester-3/Labs-Semester-3/Exp%202/Exp%202a) |
| 02b | Automobile / Auto MPG cleaning and transformation | [`Semester-3/Labs-Semester-3/Exp 2/Exp 2b`](Semester-3/Labs-Semester-3/Exp%202/Exp%202b) |
| 03 | Descriptive statistics and visualization (student survey, gym membership) | [`Semester-3/Labs-Semester-3/Lab 03`](Semester-3/Labs-Semester-3/Lab%2003) |
| 04 | Hypothesis testing: one-sample Z-test and t-test (left, right, two-tailed) | [`Semester-3/Labs-Semester-3/Lab 04`](Semester-3/Labs-Semester-3/Lab%2004) |
| 04b | Probability distributions (Bernoulli, Binomial, Poisson, Normal, Uniform) | [`Semester-3/Labs-Semester-3/Lab 04b`](Semester-3/Labs-Semester-3/Lab%2004b) |
| 05 | Linear regression: height to weight, gradient descent, and food delivery time | [`Semester-3/Labs-Semester-3/Lab 05`](Semester-3/Labs-Semester-3/Lab%2005) |

---

## Technologies Used

- **Python 3.x**
- **Pandas** – tabular data handling
- **requests** – HTTP clients for REST APIs and HTML pages
- **BeautifulSoup** – HTML parsing for web scraping
- **scikit-learn** – encoding and feature scaling
- **SciPy** – Z-score outlier checks, skewness, kurtosis, and `norm` / `t` hypothesis tests
- **Matplotlib, Seaborn** – histograms, box plots, scatter plots, heatmaps, rejection-region plots

---

## How to Use

```bash
git clone https://github.com/francisreubenr-rvu/Data-Science-Labs.git
cd Data-Science-Labs
pip install -r requirements.txt
```

Open the notebooks under `Semester-3/Labs-Semester-3/` with Jupyter.

---

## Learning Outcomes

- Collect structured data from REST APIs and paginated HTML catalogues
- Clean missing values, duplicates, and broken numeric tokens
- Encode categoricals, review outliers, and scale features
- Compute mean, median, variance, IQR, skewness, and kurtosis, and choose which to report
- Run one-sample Z-tests and t-tests, pick the tail from H1, and decide from the p-value
- Fit a linear regression on a scaled train/test split and score it with MSE, MAE, and R²
- Store collected and preprocessed records as CSV for later analysis
- Respect `robots.txt`, terms of service, and request rate limits

---

## Future Scope

Additional assignments may include two-sample tests, classification, and clustering.
