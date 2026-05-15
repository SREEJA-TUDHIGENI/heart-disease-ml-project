# Heart Disease ML Project

This is supervised machine learning project using the UCI Heart Disease dataset.

---

# Project Goal

The goal is to predict whether a patient has heart disease or not based on medical features such as:

* Age
* Cholesterol
* Blood pressure
* Chest pain type
* Maximum heart rate
* ECG-related measurements

---

# Dataset Used

Dataset file used:

```text
processed.cleveland.data
```

Each row represents one patient.

The target column is:

```text
target
```

Original target values:

```text
0 = no heart disease
1, 2, 3, 4 = heart disease present
```

For this project, the target was converted into binary form:

```text
0 = healthy
1 = heart disease
```

---

# Project Workflow

## 1. Created Project Folder

```bash
mkdir heart-disease-project
cd heart-disease-project
```

---

## 2. Created Conda Environment

```bash
conda create -n mlproject python=3.11
```

---

## 3. Activated Environment

```bash
conda activate mlproject
```

---

## 4. Installed Required Libraries

```bash
conda install pandas numpy matplotlib scikit-learn jupyter ipykernel -y
```

Libraries used:

* pandas
* numpy
* matplotlib
* scikit-learn
* jupyter

---

## 5. Added Environment to Jupyter

```bash
python -m ipykernel install --user --name mlproject --display-name "Python (mlproject)"
```

---

## 6. Started Jupyter Notebook

```bash
jupyter notebook
```

---

## 7. Selected Correct Kernel

Inside Jupyter Notebook:

```text
Kernel → Change Kernel → Python (mlproject)
```

---

# Data Preprocessing

## 8. Loaded Dataset

Used pandas to load the dataset and manually assigned column names.

---

## 9. Cleaned Missing Values

The dataset contained missing values represented by:

```text
?
```

These were:

* replaced with NaN
* converted into numeric format
* rows with missing values were removed

---

## 10. Prepared Features and Target

```text
X = input features

y = target/output
```

---

## 11. Split Dataset

Used train-test split:

```text
80% training data
20% testing data
```

Purpose:

* Training set → model learns patterns
* Testing set → model evaluates on unseen data

---

# Model Training

## 12. Model Used

```text
Logistic Regression
```

Reason:

* Simple
* Fast
* Good beginner baseline model

---

## 13. Trained the Model

The model learned patterns from patient data to predict heart disease.

---

# Model Evaluation

## Accuracy

```text
88.33%
```

Meaning:

The model predicted correctly for about 88 out of 100 patients.

---

## Confusion Matrix

```text
[[32  4]
 [ 3 21]]
```

Interpretation:

* 32 healthy patients predicted correctly
* 21 disease patients predicted correctly
* 7 total prediction mistakes

---

## Classification Metrics

### Precision

How reliable the positive predictions are.

### Recall

How many actual disease cases the model successfully detected.

### F1-score

Balance between precision and recall.

---

# What I Learned

* How to understand ML datasets
* Difference between raw and processed datasets
* How to clean missing values
* How to prepare features and targets
* How train-test split works
* How Logistic Regression works
* How to evaluate a machine learning model
* How to use Git and GitHub
* How to upload projects to GitHub

---

# Repository Structure

```text
heart-disease-project/
│
├── heart-disease-commented-explained.ipynb
├── processed.cleveland.data
├── README.md
└── .gitignore
```

---

# GitHub

Project uploaded using:

* Git
* GitHub
* VS Code

---

# Future Improvements

Possible future improvements:

* Try Random Forest
* Add visualizations
* Deploy using Streamlit
* Hyperparameter tuning
* Feature engineering
* Add cross-validation
