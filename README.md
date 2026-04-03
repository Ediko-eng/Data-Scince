# 📊 HIV/AIDS Attitudes Analysis in Timor-Leste (2009-2016)

*A statistical study on social stigma and accepting attitudes toward people living with HIV/AIDS, utilizing DHS data and Python-based econometric modeling.*

---

## 📖 Project Overview
This project analyzes the evolution of social stigma toward HIV/AIDS in Timor-Leste. By processing **Demographic and Health Survey (DHS)** data, the system evaluates whether public perception has shifted over a 7-year period and identifies if variables like gender or specific social indicators significantly impact "Accepting Attitudes."

## 🚀 Key Features
* **Automated Data Cleaning:** Handles DHS summary-level data for longitudinal analysis.
* **Comparative Statistics:** Executes Independent T-Tests to find disparities between groups.
* **Predictive Modeling:** Uses Ordinary Least Squares (OLS) to measure the significance of temporal changes.
* **Tetum/English Reporting:** Analysis results are interpreted for local and academic contexts.

## ➗ Calculation & Statistical Methods

The following mathematical methods were implemented in the `main.ipynb` logic:

### 1. Data Normalization & Weighted Averages
Before analysis, indicator percentages are normalized to ensure comparability across different survey years.
$$\bar{x} = \frac{\sum_{i=1}^{n} w_i x_i}{\sum_{i=1}^{n} w_i}$$
*Where $x$ represents the attitude percentage and $w$ represents the sample weight.*

### 2. Independent Samples T-Test
Used to determine if the difference in stigma scores between Men and Women is statistically significant.
$$t = \frac{(\bar{X}_1 - \bar{X}_2)}{\sqrt{\frac{s_1^2}{n_1} + \frac{s_2^2}{n_2}}}$$
* **Null Hypothesis ($H_0$):** There is no difference in attitudes between genders.
* **Result:** A $p$-value $> 0.05$ indicates that gender does not significantly impact stigma levels.

### 3. Linear Regression (OLS)
To analyze the trend over time, we use a regression model where "Year" is the independent variable.
$$Y = \beta_0 + \beta_1(Year) + \epsilon$$
* **$\beta_1$ (Coefficient):** Measures the direction and strength of the trend.
* **$\epsilon$ (Error Term):** Accounts for variables not included in the model.

---

## 📁 Repository Structure
* **`main.ipynb`**: Core analysis script featuring T-Tests and Regression models.
* **`main1.ipynb`**: Data visualization and secondary statistical checks.
* **`Relatorio_Projetu_Final.docx`**: Full academic report containing the study's background and final conclusions.

## ⚙️ Setup & Execution
1. **Dependencies:** `pip install pandas numpy seaborn scipy statsmodels`
2. **Run Analysis:** Open `main.ipynb` in Jupyter and execute all cells to reproduce the T-Test results (e.g., $p = 0.580$ for gender comparison).

---

## 🔗 Project Metadata
* **University:** National University of Timor-Lorosa'e (UNTL)
* **Faculty:** FECT — Department of Informatic Engineering
* **Project Documentation:** [View Full License](https://github.com/Ediko-eng/Data-Scince/blob/main/LICENSE)
