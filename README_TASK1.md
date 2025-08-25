# Iris Dataset EDA, Scaling & Classification

## Objective
Explore the Iris dataset.
Visualize features.
Detect outliers.
Scale features.
Train classifiers and compare results.

## Dataset
- File: iris.csv
- Target: species
- Features: sepal_length, sepal_width, petal_length, petal_width

## Steps Performed
1) Load data, view head/tail.
2) Check missing values and duplicates.
3) Define numerical columns.
4) Outlier check using IQR method.
5) Visualize distributions (KDE, boxplots).
6) Pairplot with hue=species.

## Feature Scaling
- Copy to df_scaler.
- StandardScaler on: sepal_length, petal_length, petal_width.
- RobustScaler on: sepal_width.

## Modeling (Original Data)
- Split: train_test_split (test_size=0.3, random_state=42).
- Models:
  - LogisticRegression(max_iter=200)
  - RandomForestClassifier()  (default params)
- Metrics:
  - Accuracy (printed)
  - Classification report (printed)
  - Confusion matrix (sklearn display + seaborn heatmap)

## Modeling (Scaled Data)
- Use df_scaler for X, y.
- Split with same test_size and random_state.
- LogisticRegression(max_iter=200).
- Metrics:
  - Accuracy (printed)
  - Classification report (printed)
  - Confusion matrix heatmap (seaborn)

## Visualizations
- KDE plots per numeric column (original vs scaled).
- Boxplots per numeric column.
- Pairplot with target hue.
- Confusion matrix heatmaps (original and scaled).

## Requirements
- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

## How to Run
1) Place `iris.csv` in the same folder as the notebook.
2) Open `codeAlpha Task 1.ipynb` in Jupyter.
3) Run cells in order.


- Random state fixed for reproducibility.
- No hard-coded accuracy in this README; check printed outputs in the notebook.
