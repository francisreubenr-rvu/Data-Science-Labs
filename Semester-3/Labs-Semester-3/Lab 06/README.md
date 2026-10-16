# Lab 06: Logistic Regression

**Name:** Francis Reuben R  
**USN:** 1RUA25CSE0168  
**Section:** G  
**Experiment:** 6  
**Title:** Implementation of Logistic Regression using Python

## Objective

Predict whether a person buys life insurance from age, classify gender from height and weight with gradient descent, and predict whether an employee leaves from satisfaction, monthly hours, promotion, and salary.

## Notebooks

| File | What it does |
|---|---|
| `Ex.No.6.ipynb` | Executed notebook. Insurance model, gender gradient descent, and the HR retention exercise |
| `1RUA25CSE0168_Francis_Reuben_R_Lab6.ipynb` | Same notebook, named for upload |
| `Record_Exp6_Francis_Reuben_R.pdf` | Lab record: objective, pipeline, the three models, coefficients |

## Data

| File | Columns |
|---|---|
| `insurance_data.csv` | age, bought_insurance. 27 rows |
| `weight-height.csv` | Gender, Height (inches), Weight (pounds). 10,000 rows. All rows are kept |
| `HR_comma_sep.csv` | satisfaction_level, last_evaluation, number_project, average_montly_hours, time_spend_company, Work_accident, left, promotion_last_5years, Department, salary. 14,999 rows. The notebook loads the same table from the codebasics raw URL |

## Figures

| File | Role |
|---|---|
| `flowchart.png` | Pipeline used in the record |
| `figures/insurance_scatter.png` | Age against purchase |
| `figures/loss_curve.png` | Cross-entropy over 1,000 steps |
| `figures/confusion_matrix.png` | Gender predictions on the fitting rows |
| `figures/learning_rate.png` | Five learning rates over 300 steps |
| `figures/salary_retention.png` | Headcount by salary and whether the employee left |
| `figures/department_retention.png` | Headcount by department and whether the employee left |

## Run

```bash
pip install -r ../../../requirements.txt
jupyter notebook Ex.No.6.ipynb
```

Use the DSLAB venv at `Lab/DSLABs/dslab`. The first cell mounts Google Drive and is only needed in Colab. The insurance split is 80/20 with `random_state` 4. The HR split is 70/30 with `random_state` 42.

## Results

| Model | Result |
|---|---|
| Insurance from age | Coefficient 0.2100, intercept -8.6878, threshold at 41.4 years. Test accuracy 0.50 on 6 rows |
| Hand check of the sigmoid | 12.24% at age 32, 58.42% at age 43 |
| Gender, gradient descent | Loss 0.2326 after 1,000 steps. Accuracy 0.91 on the 10,000 fitting rows. Weight coefficient 3.482 |
| HR retention | Test accuracy 76.76%. Leave-class recall 0.241. A predict-stay baseline on the same fold is 76.18% |

Low salary leaves at 29.7%. High salary leaves at 6.6%. Satisfaction coefficient is -3.818.
