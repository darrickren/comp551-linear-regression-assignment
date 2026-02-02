# Linear Regression Assignment

This repository contains the complete implementation for a **Linear Regression assignment**, designed to be **run primarily on Google Colab**.
The project includes data preprocessing, feature engineering, linear regression from scratch, and model evaluation.

---

## Repository Structure

```
.
├── day.csv
├── Linear Regression Assignment.ipynb
├── README.md
```

> All intermediate CSV files (train/test splits and feature-engineered datasets) are **generated automatically** when the notebook is executed.

---

## File Descriptions

### `day.csv`

Original dataset containing daily bike rental information.

### `Linear Regression Assignment.ipynb`

Main notebook that contains:

* Data preprocessing pipeline
* Linear regression implementation from scratch (NumPy only)
* Feature engineering experiments
* Model training and evaluation


---

## Models Implemented

All models use **linear regression with a bias term**, solved using the **least-squares closed-form solution** (`np.linalg.lstsq`).

Implemented models:

* **Baseline Linear Regression**
* **Polynomial Features (squares only)**
* **Pairwise Interaction Features**
* **Gaussian Basis Expansion** (`D_g = 10`)
* **Sigmoid Basis Expansion** (`D_s = 5`)

Continuous features used for nonlinear expansion:

* `temp`, `atemp`, `hum`, `windspeed`

---

## Evaluation

Models are evaluated using **Mean Squared Error (MSE)** on:

* Training set
* Testing set

This enables comparison of model complexity, underfitting, and overfitting behavior.

---

## How to Run (Google Colab)

1. Upload all repository files to a folder in **Google Drive**
2. Open `Linear Regression Assignment.ipynb` using **Google Colab**
3. Run the first cell to mount Google Drive when prompted
4. Ensure the dataset file `day.csv` is in the same folder as the notebook
5. Run **all cells from top to bottom**

The notebook will automatically:

* Load `day.csv`
* Perform all preprocessing steps
* Generate intermediate CSV files
* Train and evaluate all models

---


## Notes

* Linear regression is implemented **from scratch** using NumPy (no scikit-learn regression models).
* All intermediate datasets are saved for transparency and reproducibility.
* Basis expansion parameters (`D_g`, `D_s`) are chosen to balance model flexibility and overfitting risk.

---

## Summary

This project demonstrates:

* End-to-end data preprocessing
* Linear regression implemented from first principles
* Feature engineering with polynomial, interaction, Gaussian, and sigmoid bases
* Empirical comparison of model complexity using test MSE
