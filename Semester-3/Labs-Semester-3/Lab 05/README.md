# Lab 05 – Linear Regression

**Name:** Francis Reuben R  
**USN:** 1RUA25CSE0168  
**Section:** G  
**Experiment:** 5  
**Title:** Implementation of Linear Regression using Python

## Objective

Predict weight from height, check that line with gradient descent, and predict food delivery time from distance, preparation time, traffic, and weather.

## Notebooks

| File | What it does |
|---|---|
| `Ex.No.5.ipynb` | Executed notebook. Height model, gradient descent, and the delivery assignment |
| `1RUA25CSE0168_Francis_Reuben_R_Lab5.ipynb` | Same notebook, named for upload |
| `Record_Exp5_Francis_Reuben_R.pdf` | Lab record: objective, pipeline, both models, coefficients |

## Data

| File | Columns |
|---|---|
| `weight-height.csv` | Gender, Height (inches), Weight (pounds). 3 rows with height above 90 inches are dropped |
| `Food_Delivery_Times.csv` | Order_ID, Distance_km, Weather, Traffic_Level, Time_of_Day, Vehicle_Type, Preparation_Time_min, Courier_Experience_yrs, Delivery_Time_min. 60 rows missing traffic or weather are dropped |

## Figures

| File | Role |
|---|---|
| `flowchart.png` | Pipeline used in the record |
| `figures/height_weight_fit.png` | Test points and the fitted line |
| `figures/gd_loss.png` | MSE over 1,000 gradient-descent steps |
| `figures/delivery_actual_vs_predicted.png` | Test orders against the diagonal |

## Run

```bash
pip install -r ../../../requirements.txt
jupyter notebook Ex.No.5.ipynb
```

Use the DSLAB venv at `Lab/DSLAB/dslab`. The split is 80/20 with `random_state` 67.

## Results

| Model | Test result |
|---|---|
| Height to weight | R2 0.8531, MAE 9.91 pounds, slope 7.71 pounds per inch |
| Gradient descent | Slope 0.9248, same as least squares. Final MSE 0.144745 |
| Delivery time | R2 0.7684, MAE 6.49 minutes, against 17.11 minutes for the training mean |

Distance adds 3.02 minutes per kilometre. Preparation adds 1.02 minutes per minute. Each traffic step adds 5.69 minutes. Against clear weather, snow adds 10.39 minutes, fog 9.48, rain 5.82, and wind 2.75.
