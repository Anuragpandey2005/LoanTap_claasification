# 📊 LoanTap Creditworthiness Prediction

## 📝 Problem Statement  
LoanTap is an online platform that delivers customized loan products to millennials. The company aims to build an **underwriting layer** to determine the **creditworthiness of individuals** applying for **Personal Loans**.  

The key business question:  
> **Given a set of attributes for an individual, should a credit line be extended to them? If yes, what repayment terms should be recommended?**

This project involves building a **Logistic Regression model** to predict loan repayment outcomes (loan status) and provide actionable business recommendations.

---

## 📂 Dataset Overview  

The dataset provided (`LoanTapData.csv`) contains borrower details and loan-related information.  

### Key Features:  
- **loan_amnt**: Loan amount requested by the borrower  
- **term**: Loan term (36 or 60 months)  
- **int_rate**: Interest rate of the loan  
- **installment**: Monthly payment owed  
- **grade, sub_grade**: LoanTap-assigned grades for creditworthiness  
- **emp_title, emp_length**: Employment details  
- **home_ownership**: Borrower’s homeownership status  
- **annual_inc**: Annual income (self-reported)  
- **verification_status**: Income verification status  
- **purpose**: Purpose of the loan (e.g., debt consolidation, home improvement)  
- **dti**: Debt-to-income ratio  
- **credit history attributes**: (earliest_cr_line, open_acc, revol_bal, pub_rec, etc.)  
- **loan_status (Target Variable)**: Loan repayment status  

### Engineered Features:  
- **pub_rec_flag** (1 if borrower has public record, else 0)  
- **mort_acc_flag** (1 if mortgage accounts > 0, else 0)  
- **bankruptcy_flag** (1 if bankruptcies > 0, else 0)  

---

## 🔎 Project Workflow  

1. **Exploratory Data Analysis (EDA)**  
   - Data structure, missing value analysis, statistical summary  
   - Univariate & Bivariate analysis (distribution, boxplots, correlations)  
   - Insights on loan amount, installment trends, grade-wise repayment  

2. **Data Preprocessing**  
   - Handling missing values  
   - Outlier treatment  
   - Feature engineering (flags, ratio-based features)  
   - Encoding categorical variables  
   - Scaling numeric features using StandardScaler / MinMaxScaler  

3. **Model Building**  
   - Logistic Regression using **Scikit-learn** / **Statsmodels**  
   - Interpreting coefficients & feature importance  

4. **Model Evaluation**  
   - **Classification Report** (Accuracy, Precision, Recall, F1-score)  
   - **Confusion Matrix**  
   - **ROC-AUC Curve**  
   - **Precision-Recall Curve**  
   - Tradeoff analysis (minimizing false negatives vs false positives)  

---

## 🛠️ Tech Stack Used  

- **Python 3.10+**  
- **Pandas, NumPy** → Data wrangling  
- **Matplotlib, Seaborn** → Visualization & EDA  
- **Scikit-learn** → Modeling & evaluation  
- **Statsmodels** → Logistic regression interpretation  
- **Jupyter Notebook** → Development & documentation  

---

## ✅ Business Insights & Recommendations  

- Borrowers with **lower DTI and stable employment** are more likely to repay.  
- **Home ownership and higher annual income** correlate with safer borrowers.  
- **Grades A & B** are associated with higher repayment likelihood.  
- **Precision-Recall tradeoff** must be carefully optimized to reduce **NPAs (non-performing assets)**.  
- For a safer lending strategy, focus on **Recall (identifying real defaulters)**, but balance with **Precision** to avoid losing good borrowers.  

---

## 📌 Repository Structure  

