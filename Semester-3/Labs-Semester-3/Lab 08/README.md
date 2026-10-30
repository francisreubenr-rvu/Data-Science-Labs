# Lab 08: K-Means Clustering

**Name:** Francis Reuben R  
**USN:** 1RUA25CSE0168  
**Section:** G  
**Experiment:** 8  
**Title:** Implementation of K-Means Clustering using Python

## Objective

Cluster seven points by hand, separate 22 people by age and income once the two columns share a scale, and cluster 178 wines from 13 chemical measurements with a NumPy K-Means and with scikit-learn.

## Notebooks

| File | What it does |
|---|---|
| `Ex.No.8.ipynb` | Executed notebook. Hand example, income before and after scaling, NumPy K-Means on the z-scored columns, and the wine exercise |
| `1RUA25CSE0168_Francis_Reuben_R_Lab8.ipynb` | Same notebook, named for upload |
| `Record_Exp8_Francis_Reuben_R.pdf` | Lab record: objective, pipeline, hand example, income model, wine comparison |

## Data

| File | Role |
|---|---|
| `income.csv` | 22 people. Columns are Name, Age, and Income($). Age runs from 26 to 43. Income runs from 45,000 to 162,000 |

The wine table comes from scikit-learn (`load_wine`): 178 rows, 13 chemical features, cultivars 59, 71, and 48. No wine CSV is stored.

## Figures

| File | Role |
|---|---|
| `flowchart.png` | Pipeline used in the record |
| `figures/hand_clusters.png` | Seven points after convergence, K = 2 |
| `figures/income_raw.png` | Age against income, uncoloured |
| `figures/income_unscaled.png` | K = 3 on the raw columns |
| `figures/income_scaled.png` | Age against income after min-max scaling |
| `figures/income_scaled_clusters.png` | K = 3 after min-max scaling |
| `figures/income_elbow.png` | SSE and silhouette for K = 2 to 9 |
| `figures/income_zscore_clusters.png` | NumPy K-Means on the z-scored columns, K = 3 |
| `figures/wine_k_selection.png` | WCSS and silhouette for K = 2 to 10, both implementations |
| `figures/wine_pca.png` | First two principal components: cultivar, scratch labels, sklearn labels |

## Run

```bash
pip install -r ../../../requirements.txt
jupyter notebook Ex.No.8.ipynb
```

Use the DSLAB venv at `Lab/DSLABs/dslab`. The raw income model is K = 3 with `random_state` 42. The min-max model is K = 3 with `random_state` 42 and `n_init` 10. The NumPy income run uses seed 42 on z-scores. The wine models use `n_init` 10 and seed 42, and they cluster the 13 scaled features. PCA is only for the plot.

## Results

| Model | Result |
|---|---|
| Hand example, K = 2 | Converges at centroids (1.25, 1.5) and (3.9, 5.1). C1 is {A, B}. C2 is {C, D, E, F, G}. WCSS path 33.250, 11.226, 8.525. Point A silhouette 0.778 |
| Income, raw columns, K = 3 | Inertia 1,606,229,737.68. Groups of 7, 12, and 3, split by income. The group of 12 mixes ages 26 to 43 |
| Income, min-max, K = 3 | Inertia 0.4751. Young 9 (mean age 28.33, mean income 58,611), high income 7 (mean income 150,000), older middle 6 (mean age 40.50, mean income 68,667). Silhouette peaks at K = 3 (0.7130) |
| Income, z-score, NumPy, K = 3 | WCSS 3.8893. Same partition as the min-max model (adjusted Rand index 1.0) |
| Wine, K = 3 | Both implementations: WCSS 1,277.928, silhouette 0.285, ARI 0.897, NMI 0.876. Silhouette peaks at K = 3. Six of 71 class_1 wines sit in the other two clusters |
