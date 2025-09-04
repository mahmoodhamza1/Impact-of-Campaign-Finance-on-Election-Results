# Impact of Campaign Finance on Election Results

This project explores the **relationship between campaign finance and electoral outcomes** in the United States using data analysis, visualization, and predictive modeling.  
It was completed as part of my master’s program and demonstrates how financial data can be leveraged to explain and predict election results.

---

## 📄 Project Overview

Elections are becoming increasingly costly and competitive. Campaign finance—through fundraising, expenditures, and cash on hand—plays a central role in determining visibility, outreach, and ultimately electoral success.  

This project investigates how different **financial variables** influence election outcomes, with a focus on the **2016 U.S. election cycle**.  
The analysis combines **exploratory data analysis (EDA)**, **visualization**, and a **predictive logistic regression model with Lasso regularization** to study patterns in candidate financing and success.

---

## ⚙️ Methodology

### 1. Data
- **Source:** Open-source dataset from Kaggle.  
- **Scope:** Candidates from the 2016 U.S. election cycle (House, Senate, and Presidential).  
- **Key Variables:**  
  - Net Contributions  
  - Cash on Hand (beginning and end of period)  
  - Net Operating Expenditures  
  - Party Affiliation, Incumbency Status, and Election Outcome  

### 2. Tools & Environment
- Language: **R**  
- Libraries: `tidyverse`, `ggplot2`, `glmnet`, `caret`  
- Deliverables: R Markdown report with EDA, visualizations, and predictive model.

### 3. Exploratory Data Analysis (EDA)
- **Candidate distribution** by party and state.  
- **Correlation analysis** among financial variables.  
- **Expenditure analysis** across states and parties.  
- **Visualizations**: bar charts, scatter plots, correlation matrix, and vote vs. spending patterns.

### 4. Predictive Modeling
- **Model:** Logistic Regression with **Lasso regularization**.  
- **Split:** Training (80%) and Testing (20%).  
- **Evaluation:**  
  - Confusion Matrix  
  - ROC Curve (AUC ~ high accuracy)  
- **Findings:** High predictive power in distinguishing winning vs. losing candidates, with **sensitivity ≈ 0.98** and good specificity.

---

## 📊 Results & Insights

### Exploratory Analysis
- **Party Distribution:** Republicans fielded ~882 candidates vs. ~800 Democrats in 2016.  
- **State Distribution:** California (CA) and Texas (TX) contributed the highest number of candidates, reflecting both population and political engagement.  
- **Correlations:**  
  - Net Contributions (NC) and Net Operating Expenditures (NOE) were **almost perfectly correlated (0.99)**, showing that funds raised were directly translated into campaign spending.  
  - Cash on Hand at Beginning (COH_Begin) correlated moderately (0.37) with Cash on Hand at Close (COH_Close), reflecting varied campaign burn rates.  
  - Debt Owed by Committee (DOBC) showed little correlation, indicating it did not strongly influence financial capacity or outcomes.  

### Spending Patterns
- **State-Level Expenditures:**  
  - Republicans invested most heavily in **Florida, Pennsylvania, and California**.  
  - Democrats spent most in **California, Florida, and Maryland**, underscoring strategic targeting of high-stakes states.  
- **Votes vs. Spending:**  
  - Incumbents consistently achieved **higher votes per dollar spent**, leveraging recognition and established networks.  
  - Challengers and open-seat candidates required disproportionately higher expenditures for similar vote totals.  

### Predictive Modeling
- **Model:** Logistic Regression with Lasso Regularization.  
- **Performance Metrics:**  
  - **Sensitivity (True Positive Rate):** ~0.98 → the model was highly effective at correctly identifying winning candidates.  
  - **Specificity (True Negative Rate):** ~0.61 → moderate success at identifying losing candidates, suggesting that some well-funded losers were difficult to classify.  
  - **ROC Curve:** Steep and close to the top-left corner, confirming strong discriminatory power.  
- **Interpretation:**  
  - The model achieved **high overall predictive accuracy**, validating the central role of financial indicators in determining electoral outcomes.  
  - However, the lower specificity highlights the nuance: **financial strength is necessary but not sufficient** for victory. Factors such as political climate, incumbency, and campaign strategy introduce variability.  

### 🔑 Key Insight
This study confirms that **financial resources are a powerful predictor of electoral success**, but they are not the sole determinant.  
- Candidates with **greater net contributions and expenditures** generally had higher chances of winning.  
- **Incumbency advantage** reduced the cost per vote significantly, showing incumbents could “do more with less.”  
- Importantly, the model revealed cases where financially strong campaigns still lost (e.g., Hillary Clinton in 2016) — illustrating that **strategic factors, voter sentiment, and external shocks can outweigh pure monetary advantage**.  

Together, these findings underscore that while campaign finance provides a **decisive edge**, victory ultimately depends on a combination of **money, incumbency, and message resonance**.

## 📂 Repository Contents
- CandidateSummaryAction1.csv # Dataset (from Kaggle)
- Final_Project_Data Visualization.Rmd # R Markdown analysis
- Final-Project.pdf # Full project report
