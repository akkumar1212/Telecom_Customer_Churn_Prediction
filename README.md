=> Telecom Customer Churn Analysis (Python)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)

=> Project Overview
Customer Churn is a critical metric for telecom companies. This project analyzes a dataset of 1,000 customers to identify **why customers leave** and which segments are at the highest risk.
I used **Python (Pandas)** for data cleaning and **Seaborn** for exploratory data analysis (EDA).

=> Key Insights
* **The "Month-to-Month" Trap:** Customers on monthly contracts are **5x more likely to churn** than those on 1-2 year contracts.
* **The "Newbie" Risk:** The highest churn rate occurs within the **first 1-6 months** of tenure. If a customer stays past 6 months, their loyalty increases significantly.
* **Pricing Sensitivity:** Churned customers had a significantly higher *Average Monthly Charge* than retained customers, suggesting pricing is a friction point.

=> Tech Stack
* **Data Manipulation:** Pandas, NumPy
* **Visualization:** Seaborn, Matplotlib
* **Environment:** Google Colab

=> Code Snippet (Data Cleaning)
*Handling missing values in the 'TotalCharges' column:*
```python
# Convert to numeric and drop nulls
df['TotalCharges'] = pd.to_numeric(df['TotalCharges'], errors='coerce')
df.dropna(inplace=True)
