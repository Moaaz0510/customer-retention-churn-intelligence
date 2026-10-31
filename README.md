# Customer-retention-churn-intelligence
An exploratory customer analytics project using Python, SQL and data visualisation to investigate customer churn, retention patterns, revenue risk and support interactions.
# Customer Retention & Churn Intelligence

An end-to-end customer churn analytics project using Python, SQL, Pandas and data visualization.

**1. Project Overview**

Customer churn is a major challenge for subscription-based businesses, particularly in the OTT (Over-The-Top) streaming industry, where retaining existing subscribers is essential for sustainable revenue growth.

This project analyzes customer demographics, subscription information and customer support interactions to understand churn patterns, identify potentially high-risk customers and investigate the financial impact of customer cancellations.

The project integrates relational data using SQL and Python, performs data cleaning and feature engineering, and applies exploratory data analysis (EDA) and visualization to generate business-oriented insights.

## 2. Business Problem

The objective is to understand three important questions:

- **Who:** Which customers have left or may be at risk of leaving?
- **Why:** What customer behaviors, subscription characteristics or support experiences are associated with churn?
- **When:** During which periods are customers more likely to cancel their subscriptions?

The analysis focuses on customer retention, subscription plans, contract types, revenue at risk and customer support escalations.

## 3. Project Objectives

- Calculate customer churn and retention rates.
- Analyze churn across different subscription plans and contract types.
- Investigate monthly customer churn trends.
- Calculate Average Revenue Per User (ARPU).
- Analyze customer tenure and cancellation patterns.
- Estimate revenue associated with churned and high-risk customers.
- Examine customer complaints and support escalations.
- Investigate the relationship between support escalations and churn.
- Develop actionable recommendations to improve customer retention.

## 4. Tools & Technologies

| Technology | Application |
|---|---|
| Python | Data analysis and programming |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations and feature engineering |
| SQLite | Relational database and SQL queries |
| Matplotlib | Data visualization |
| Seaborn | Statistical visualization |
| Google Colab | Development environment |

## 5. Dataset Description

The project uses a relational customer churn dataset consisting of three main tables:

**1. Customer Table (`db_customer`)**
- Customer ID
- Name
- Country and state
- Gender
- Date of birth
- Interests
- Pincode

**2. Subscription Table (`db_subscription`)**
- Customer ID
- Subscription start date
- Subscription type
- Plan type
- Contract type
- Renewal date
- Cancellation date
- Cancellation reason
- Monthly charges
- Customer Lifetime Value (CLTV)
- Churn score

**3. Support Table (`db_support`)**
- Customer ID
- Complaint date
- Escalations
- Customer satisfaction score (CSAT)
- Comments

The datasets are provided in Excel and SQLite formats.

## 6. Project Workflow

### Step 1: SQL Database Integration
- Connected the SQLite database to Python using `sqlite3`.
- Retrieved database tables using SQL queries.
- Imported relational data into Pandas DataFrames.

### Step 2: Data Cleaning
- Renamed and selected relevant columns.
- Removed unnecessary columns.
- Converted columns to appropriate data types.
- Standardized data values.
- Identified and handled missing values.

### Step 3: Feature Engineering
- Created a binary churn flag using cancellation information.
- Calculated customer tenure in days.
- Created complaint counts.
- Merged customer, subscription and support datasets using customer IDs.
- Categorized customers into churn-risk groups using churn scores.
- Encoded categorical variables for correlation analysis.

### Step 4: Exploratory Data Analysis
Analyzed:
- Overall churn and retention rates.
- Churn by subscription plan.
- Customer tenure.
- Average revenue per user.
- Revenue associated with churned customers.
- Support escalation rates.
- Average complaints per customer.
- Relationship between support escalations and churn.

### Step 5: Data Visualization
Created visualizations using Matplotlib and Seaborn:

- Monthly churn trend.
- Churn rate by subscription plan.
- Churn rate by state.
- Correlation heatmaps.
- Monthly charges across subscription plans, genders and churn-risk categories.

### Step 6: Business Insights
Interpreted the analysis to identify customer retention opportunities and areas requiring further investigation.

## 7. Key Findings

The accompanying project report documents the following findings:

| KPI | Result |
|---|---:|
| Overall Churn Rate | 28.6% |
| Retention Rate | 71.4% |
| Average Customer Tenure | 1,451 days |
| ARPU | 18.8 |
| Total Revenue | 395 |
| Revenue Loss Due to Churn | 74 |
| CLTV Lost | 2,047 |
| Revenue Loss Percentage | 18% |

### Contract Type Analysis

The report highlights a significant difference between monthly and annual subscription contracts:

| Contract Type | Churn Rate |
|---|---:|
| Monthly | 55.6% |
| Annual | 8.3% |

Monthly-contract subscribers showed substantially higher churn than annual-contract subscribers in this dataset.

### Other Important Observations

- The Basic subscription plan contributed the largest share of customer churn.
- September 2024 was identified as the month with the highest churn.
- Karnataka was identified as the most affected state.
- The report highlights competitor switching, pricing sensitivity and content dissatisfaction as cancellation drivers to investigate.

**Note:** These results describe the supplied sample dataset, not the wider OTT industry. The dataset is small, so the findings should be treated as exploratory rather than statistically generalizable.

## 8. Business Recommendations

Based on the project report, the following actions are recommended:

1. **Investigate regional churn:** Examine customer complaints, pricing changes and technical issues in Karnataka.
2. **Review Basic subscription pricing:** Investigate whether price changes or plan modifications contributed to churn.
3. **Analyze competitor activity:** Understand why customers may be switching to competing platforms.
4. **Prioritize high-risk customers:** Identify customers with medium and high churn-risk scores.
5. **Improve customer support:** Review escalated complaints and contact affected customers through email, SMS or calls.
6. **Encourage annual subscriptions:** Investigate contract-migration strategies to improve long-term retention.

## 9. Repository Structure

```text
customer-retention-churn-intelligence/
│
├── README.md
├── .gitignore
│
└── customer-retention-churn-intelligence/
    ├── churn_analysis.ipynb
    ├── customer_churn.db
    ├── customer_churn_data_raw.xlsx
    └── requirements.txt
```

## 10. How to Run the Project

1. Clone or download this repository.
2. Open the folder containing the notebook and dataset files.
3. Install the required libraries:

```bash
pip install -r requirements.txt
```

4. Open `churn_analysis.ipynb` in Google Colab or Jupyter Notebook.
5. Ensure the Excel and SQLite files are accessible in the notebook's working directory.
6. Execute the notebook cells in sequence.

## 11. Skills Demonstrated

- Python programming
- SQL and SQLite database integration
- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Data merging and relational joins
- Customer churn and retention analysis
- Revenue and customer behavior analysis
- Data visualization
- Business insight generation

## 12. Author

**Moaaz Ahmed**

Master's Student – Computational Mathematics  
TU Chemnitz, Germany

[GitHub Profile](https://github.com/Moaaz0510)

---

*This project was developed as a practical learning and portfolio project focused on applying Python, SQL and data analytics techniques to a customer retention business problem.*
