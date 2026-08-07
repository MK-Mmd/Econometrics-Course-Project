# Causal Analysis of Music Popularity on Spotify

**Student Name:** Mohammad Mokhtari  
**Student ID:** 401102478  
**Course:** Econometrics (Minor Program)  
**University:** Sharif University of Technology  

---

## Project Overview
[This repository](https://github.com/MK-Mmd/Econometrics-Course-Project) contains the final project for the Econometrics course. The project investigates the causal impact of acoustic and structural features (e.g., danceability, energy, valence) on the popularity of music tracks on Spotify. By addressing Omitted Variable Bias (OVB) through the engineering of an `artist_popularity` proxy and controlling for 125 genre fixed effects, the study successfully isolates the true behavioral drivers of listener preferences.

## Repository Contents
The submitted ZIP archive includes the following files:

1. **`Econometrics_Project_401102478.pdf`**
   * The comprehensive final report in Persian.
   * Includes the Research Log, Introduction, Data & Variables, Empirical Strategy (OLS & HC3 Standard Errors), Results Interpretation, Robustness Checks, Conclusion, Reflection, and Bibliography.

2. **`Econometrics_Project_401102478.ipynb`**
   * The fully reproducible Jupyter Notebook containing all Python codes.
   * Includes data acquisition, cleaning, Exploratory Data Analysis (EDA), multicollinearity diagnostics (VIF), Heteroskedasticity testing (Breusch-Pagan), model fitting, and data visualizations.

3. **`dataset.csv`**
   * The cleaned Spotify Tracks Dataset used for the econometric analysis.

4. **`README.md`**
   * This documentation file.

---

## How to Run the Code
To reproduce the findings, tables, and plots presented in the report, follow these steps:

### 1. Prerequisites
Ensure you have Python 3.8+ installed along with the following libraries:
* `pandas`
* `numpy`
* `matplotlib`
* `seaborn`
* `statsmodels`
* `kagglehub`

You can install the required packages using pip:
```bash
pip install pandas numpy matplotlib seaborn statsmodels kagglehub

```

### 2. Execution

* Open the `Econometrics_Project_401102478.ipynb` file using Jupyter Notebook, JupyterLab, or VS Code.
* Run the cells sequentially from top to bottom.
* **Note on Data:** The notebook is configured to automatically download the raw dataset via the `kagglehub` library in the first code cell. However, the static `dataset.csv` is also provided in the ZIP file for offline access or if the API connection fails.

---

## Key Econometric Highlights

* **Identification Strategy:** Ordinary Least Squares (OLS) with Fixed Effects.
* **Diagnostics:** Variance Inflation Factor (VIF) for multicollinearity and Breusch-Pagan test for heteroskedasticity.
* **Correction:** Heteroskedasticity-Consistent (HC3) robust standard errors were applied due to the non-constant variance of the residuals.
* **Robustness:** Sub-sample analysis was performed by splitting the data into 'Explicit' and 'Clean' tracks to ensure the stability of the `artist_popularity` coefficient.