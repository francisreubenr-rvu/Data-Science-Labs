# Lab 07: KNN Classification

**Name:** Francis Reuben R  
**USN:** 1RUA25CSE0168  
**Section:** G  
**Experiment:** 7  
**Title:** Implementation of KNN Classification using Python

## Objective

Classify iris species from sepal and petal measurements with K nearest neighbours, rebuild that vote from Euclidean distance, and classify 1,797 handwritten digits.

## Notebooks

| File | What it does |
|---|---|
| `Ex.No.7.ipynb` | Executed notebook. Distance check, hand example, iris KNN, from-scratch vote, and the digits exercise |
| `1RUA25CSE0168_Francis_Reuben_R_Lab7.ipynb` | Same notebook, named for upload |
| `Record_Exp7_Francis_Reuben_R.pdf` | Lab record: objective, pipeline, iris model, scratch vote, digits |

## Data

Iris and the digits come from scikit-learn (`load_iris`, `load_digits`). No CSV is stored. Iris has 150 rows and four measurements, 50 of each species. Digits has 1,797 images of 8 by 8 pixels.

## Figures

| File | Role |
|---|---|
| `flowchart.png` | Pipeline used in the record |
| `figures/sepal_scatter.png` | Setosa against versicolor on the sepal axes |
| `figures/petal_scatter.png` | Setosa against versicolor on the petal axes |
| `figures/petal_three_species.png` | All three species on the petal axes |
| `figures/iris_confusion_matrix.png` | Iris test set, K = 10 |
| `figures/iris_roc.png` | One-vs-rest ROC for that model |
| `figures/iris_k_accuracy.png` | Iris test accuracy for K = 1 to 30 |
| `figures/scratch_confusion_matrix.png` | From-scratch vote on sepal length and width, K = 5 |
| `figures/scratch_k_accuracy.png` | That vote for K = 1 to 20 |
| `figures/digits_samples.png` | First ten digit images |
| `figures/digits_k_accuracy.png` | Digits test accuracy for K = 1 to 30 |
| `figures/digits_confusion_matrix.png` | Digits test set at K = 1 |

## Run

```bash
pip install -r ../../../requirements.txt
jupyter notebook Ex.No.7.ipynb
```

Use the DSLAB venv at `Lab/DSLABs/dslab`. The iris split is 80/20 with `random_state` 1. The scratch split is 70/30 with `random_state` 42, on sepal length and sepal width only. The digits split is 80/20 with `random_state` 10.

## Results

| Model | Result |
|---|---|
| Hand example, K = 3 | Versicolor. Nearest are C 0.36, F 0.36, D 0.89 |
| Iris, four measurements, K = 10 | Test accuracy 0.9667 (29 of 30). One versicolor called virginica (row 77, vote 6 to 4). AUC 1.000 for each class |
| Iris K sweep | K = 1 to 6 and K = 8 score 30 of 30. K = 7 and K = 9 to 30 score 29 of 30 |
| Scratch vote, sepal only, K = 5 | 36 of 45. sklearn on the same rows scores 35 of 45. The gap is one distance tie at 0.1414 |
| Digits, K = 1 | 356 of 360. K = 3 ties that score. Lowest F1 is digit 8 at 0.969. The four errors are 8 to 1, 8 to 3, 9 to 3, and 9 to 4 |
