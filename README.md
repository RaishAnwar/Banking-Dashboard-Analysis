# 🏦 Banking Customer Financial Analysis – EDA + Power BI Dashboard

This project analyzes **Banking Customer Financial Data** using Python (EDA) and builds an **interactive Power BI dashboard** to uncover insights on loans, deposits, customer demographics, income levels, and bank relationships.

The objective is to understand:
- Customer financial behavior  
- High-value and low-value customer segments  
- Loan & deposit patterns  
- Branch-level and nationality-level performance  
- Income band contribution  
- The impact of gender, BRId, and occupation on banking metrics  

---

# 📂 Project Structure

```
├── EDA (Python)
│   ├── Data cleaning
│   ├── Univariate analysis
│   ├── Bivariate analysis
│   ├── Correlation analysis
│   ├── Financial pattern analysis
│   └── Manual segmentation (qcut)
│
└── Power BI Dashboard
    ├── Banking Dashboard (Home)
    ├── Loan Analysis Page
    └── Deposit Analysis Page
```

---

# 🧰 Tools & Technologies
### 🐍 **Python**
- Pandas  
- NumPy  
- Matplotlib  
- Seaborn  

### 📊 **Power BI**
- DAX Measures  
- Interactive Visuals  
- Filters & Slicers  
- Multi-page Dashboard  

---

# 📌 Dataset Overview

The dataset contains **3000 customers** with fields like:

### 🔹 Demographics  
- Gender  
- Nationality  
- Occupation  
- Income Band  

### 🔹 Financial Metrics  
- Estimated Income  
- Superannuation Savings  
- Savings Accounts  
- Checking Accounts  
- Bank Loans  
- Business Lending  
- Bank Deposits  
- Credit Card Balance  

### 🔹 Banking Relationship  
- BRId  
- Investment Advisor  
- Fee Structure  
- Loyalty Classification  

---

# 📊 Exploratory Data Analysis (EDA)

### 🔍 **1. Univariate Analysis**
Performed on:
- Estimated Income  
- Savings  
- Credit Card Balance  
- Deposits  
- Loans  
- Lending  

Used **histograms**, **KDE plots**, **countplots**.

### 🔍 **2. Categorical Analysis**
- Gender distribution  
- Nationality distribution  
- Occupation frequency  
- Income Band segmentation  

### 🔍 **3. Correlation Analysis**
A correlation matrix uncovered:

- **Bank Deposits ↔ Checking Accounts (0.84)**  
- **Bank Deposits ↔ Saving Accounts (0.75)**  
- **Business Lending ↔ Bank Loans (0.42)**  
- Moderate relationships between income & financial activity.

### 🔍 **4. Bivariate Insights**
- High-income groups deposit more & take higher loans  
- European customers dominate loan portfolios  
- Private Bank relationship gives highest loan & deposit volume  

### 🔍 **5. Manual Segmentation (No sklearn used)**
Using `pd.qcut()`:
- Customers split into Low / Mid / High categories  
- Segmented loan and deposit patterns analyzed  

---

# 📈 Power BI Dashboard (3 Pages)

Below are actual dashboard screenshots:

### 📌 **1. Home – Banking Dashboard**
- Total Clients  
- Total Loans  
- Total Deposits  
- Savings Accounts  
- Checking Accounts  
- Business Lending  
- Gender Filters  
- Year Slicer  
- Navigation Buttons  
- Banking Relationship Slicer  

Includes **KPI cards** and quick navigation to Loan & Deposit pages.

---

### 📌 **2. Loan Analysis Page**
Key Visuals:
- Loan by Banking Relationship (BRId)
- Loan by Nationality  
- Loan by Occupation (Top Professions)
- Loan by Income Band (Donut Chart)
- Total Loan KPI  
- Business Lending KPI  
- Credit Card Balance KPI  
- Gender Filter  
- Year Filter  
- Investment Advisor Filter  

**Insight:**  
Private Bank → Highest loan volume  
European customers → Largest contributors  
High-income band → 53% of total loan share  

---

### 📌 **3. Deposit Analysis Page**
Key Visuals:
- Deposits by BRId  
- Deposits by Nationality  
- Deposits by Income Band (Donut chart)  
- Saving Accounts KPI  
- Checking Accounts KPI  
- Total Deposits KPI  

**Insight:**  
Private Bank → Top deposit contributor  
Medium Income Band → Majority deposit share  
Saving + Checking Accounts → Strong correlation with Deposits  

---

# 🧮 DAX Measures Used

### ✔ **Total Loan**
```DAX
Total Loan = SUM(Financials[Bank Loans])
```

### ✔ **Total Deposit**
```DAX
Total Deposit = SUM(Financials[Bank Deposits])
```

### ✔ **Year of Joining**
```DAX
Year Joined = YEAR(Financials[Joined Bank])
```

These measures drive the KPIs and time intelligence visuals.

---

# 💡 Key Insights from Project

### 🔸 High-value customers
- Customers with **Private Bank** relationship contribute the most to both loans and deposits.

### 🔸 Income impact
- **High Income** → highest lending  
- **Medium Income** → highest deposit generation  

### 🔸 Nationality insights
- Europeans dominate most financial metrics  
- Africans & Australians contribute the least  

### 🔸 Occupation insights
- Software Consultants, Structural Analysts, and General Managers show high borrowing trends  

### 🔸 Account behavior
- Checking Accounts & Deposits → strongest correlation (0.84)  
- Savings Accounts → influences deposits significantly (0.75)  

---

# 📦 Final Deliverables

- **Jupyter Notebook:** Full EDA  
- **Power BI Dashboard:** 3-page interactive banking analysis  
- **Insights Document:** Data-driven findings  
- **README.md:** Complete project documentation  

---

# 🏁 Conclusion

This project demonstrates complete end-to-end analytics:
- Raw data → Cleaning → EDA → Insights  
- Visual storytelling via Power BI  
- Business-focused KPIs & segment analysis  

Shows skills in:
✔ Python  
✔ Data Analysis  
✔ Power BI  
✔ DAX  
✔ Storytelling  
✔ Dashboard Design  
✔ Financial Data Interpretation  

---

## 🔗 Live Power BI Dashboard

👉 **Click here to view the interactive dashboard:**  
https://app.powerbi.com/links/dnXR3-cvw8?ctid=7d1c740f-1bf8-418a-b860-1bd15fad68d7&pbi_source=linkShare

<img width="1396" height="781" alt="Bank report 3" src="https://github.com/user-attachments/assets/b440b80a-d5f3-42d5-8b17-60e31bdd3d70" />
<img width="1561" height="767" alt="Bank report 2" src="https://github.com/user-attachments/assets/93b205e5-be73-4721-8eb3-6891a30edcff" />
<img width="1830" height="818" alt="bank report 1" src="https://github.com/user-attachments/assets/68c67412-1ce4-444a-8979-963eb22e1f7c" />
