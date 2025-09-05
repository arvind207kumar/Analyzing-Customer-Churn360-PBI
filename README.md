# 📉 Churn360 Insights: Telecom Customer Retention Dashboard

A dynamic Power BI dashboard designed to uncover churn patterns in a telecom company—focusing on customer demographics, contract types, payment methods, international usage, and service interactions.

---

## 📌 Table of Contents

- [🎯 Project Overview](#project-overview)
- [📚 Data Dictionary](#data-dictionary)
- [🛠️ Tech Stack](#tech-stack)
- [🗃️ Data Source](#data-source)
- [📊 Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [🧠 Feature Engineering & Segmentation](#feature-engineering--segmentation)
- [✨ Dashboard Highlights](#dashboard-highlights)
- [📈 Business Impact & Insights](#business-impact--insights)
- [🖼️ Screenshots](#screenshots)
- [🚀 Getting Started](#getting-started)
- [📬 Contact](#contact)

---

## 🎯 Project Overview

**Goal:**  
Build an interactive Power BI dashboard to analyze customer churn for a fictional telecom provider. The dashboard identifies churn-prone segments and supports strategic decisions for retention and upselling.

**Target Users:**  
Business analysts, data scientists, customer success teams.

**Key Questions Addressed:**
- Which customer segments are most likely to churn?
- How do contract types and payment methods influence churn?
- Does international usage or customer service interaction correlate with churn?

---

## 📚 Data Dictionary

### 🧾 Customer Status

| Column Name     | Description                                      |
|-----------------|--------------------------------------------------|
| Customer ID     | Unique identifier for each customer              |
| Churn Label     | Indicates if the customer churned (Yes/No)       |
| Churn Reason    | Specific reason for churn                        |
| Churn Category  | Grouped churn reasons for broader analysis       |

### 👥 Demographics

| Column Name | Description                                      |
|-------------|--------------------------------------------------|
| Under 30    | Is customer under 30? (Yes/No)                   |
| Senior      | Is customer 65+? (Yes/No)                        |
| Age         | Age of the customer                              |
| Gender      | Male, Female, or Prefer not to say              |
| Group       | Part of a group contract? (Yes/No)              |

### 📄 Contract Information

| Column Name     | Description                                      |
|-----------------|--------------------------------------------------|
| Group Size      | Number of customers in group                     |
| Phone Number    | Customer’s phone number                          |
| State           | State code                                       |
| Payment Method  | Credit Card, Direct Debit, Paper Check           |
| Contract Type   | Month-to-Month, One Year, Two Year               |

### 💰 Subscription & Charges

| Column Name               | Description                                      |
|---------------------------|--------------------------------------------------|
| Account Length            | Duration of relationship (months)                |
| Local Calls               | Number of US-based calls                         |
| Intl Calls / Mins         | International usage metrics                      |
| Intl Active / Plan        | Premium plan status                              |
| Extra Intl Charges        | Charges without premium plan                     |
| Customer Service Calls    | Number of support calls                          |
| Avg Monthly GB Download   | Data usage                                       |
| Unlimited Data Plan       | Yes/No                                           |
| Extra Data Charges        | Charges beyond plan limits                       |
| Monthly Charges / Total Charges | Billing metrics                          |

---

## 🛠️ Tech Stack

- **Power BI Desktop** – Core platform for interactive visuals  
- **Power Query Editor** – Data cleaning & transformation  
- **DAX (Data Analysis Expressions)** – Calculated columns & dynamic filtering  
- **Data Modeling** – Relationships across customer, contract, and churn tables  
- **File Format** – `.pbix` for dashboard, `.png` for previews

---

## 🗃️ Data Source

Simulated dataset from a fictional telecom company **Databel**, including:

- Customer demographics (age, gender, senior status)
- Subscription details (contract type, payment method)
- Usage metrics (international plan, service calls)
- Churn labels and reasons

Structured across multiple tables with metadata for business context.

---

## 📊 Exploratory Data Analysis (EDA)

### 🔍 Key Steps

#### 🧼 Data Cleaning
- Handled missing values and inconsistencies
- Converted monetary columns to currency format
- Transformed state codes to full names for geographic segmentation

#### 📊 Categorical & Numerical Analysis
- Analyzed churn across contract types, payment methods, age groups
- Frequency analysis of churn reasons
- Correlation between tenure, service usage, and churn
- Outlier detection in charges and service calls

---

## 🧠 Feature Engineering & Segmentation

### 📆 Tenure Buckets

| Bucket Name | Tenure Range |
|-------------|--------------|
| New         | 0–12 months  |
| Mid-Term    | 13–24 months |
| Long-Term   | 25+ months   |

### 🧍 Age Buckets

| Segment Name | Age Range     |
|--------------|---------------|
| Youth        | Under 30      |
| Adult        | 30–49         |
| Middle-Aged  | 50–64         |
| Senior       | 65 and above  |

### 📶 Monthly Data Usage Buckets

| Usage Category | Avg Monthly GB Download |
|----------------|--------------------------|
| Low Usage      | < 5 GB                   |
| Moderate Usage | 5–15 GB                  |
| High Usage     | 15–30 GB                 |
| Heavy Usage    | > 30 GB                  |

Separate buckets for:
- Customers with Unlimited Data Plans  
- Customers with Limited Data Plans  

### 📅 Contract Duration Consolidation

| Contract Group | Original Types Included |
|----------------|--------------------------|
| Monthly        | Month-to-Month           |
| Yearly         | One Year, Two Year       |

---

## ✨ Dashboard Highlights

### 🔢 Churn KPIs (Top Panel)
- **Total Customers**  
- **Churn Rate (%)**  
- **Active vs. Churned Customers**  
- **Tenure Distribution**

### 🧍 Demographic Breakdown
- **Churn by Gender**  
- **Churn by Senior Citizen Status**  
- **Churn by Tenure Buckets**

### 📄 Contract & Payment Analysis
- **Churn Rate by Contract Type**  
- **Churn by Payment Method**

### 🌐 Service Usage & Support
- **Impact of International Plan on Churn**  
- **Customer Service Calls vs. Churn Likelihood**

### 🎛️ Interactive Filters
- Slicers for:
  - Contract Type
  - Payment Method
  - Internet Service
  - Tenure Range  
- Dynamic visuals update based on user selections

---

## 📈 Business Impact & Insights

### 🔍 Strategic Takeaways

- **Retention Strategy**  
  Month-to-month contract holders show higher churn—suggesting need for loyalty incentives.

- **Payment Optimization**  
  Customers using electronic checks churn more—indicating potential friction in payment experience.

- **Support Intervention**  
  High churn among customers with frequent service calls—highlighting service quality issues.

- **Segment Targeting**  
  Senior citizens and long-tenure customers show lower churn—ideal for upselling and retention campaigns.

---

## 🖼️ Screenshots

### 📊 Dashboard Overview  
*Figure 1: High-level KPIs and churn distribution across tenure buckets*  
![Dashboard Overview](assets/dashboard-overview.png) 

### 📈 Churn by Contract Type  
*Figure 2: Month-to-month contracts show highest churn rate*  
![Contract Type Analysis](assets/contract-type-churn.png)

### 🧍 Churn by Age Bucket  
*Figure 3: Youth and Adult segments show higher churn*  
<img width="770" height="460" alt="image" src="https://github.com/user-attachments/assets/568910bc-8a8a-4505-97cc-3e61b6d63baa" />


### 📶 Data Usage vs. Churn  
*Figure 4: Heavy data users with limited plans show elevated churn*  
<img width="691" height="507" alt="image" src="https://github.com/user-attachments/assets/602d65ae-b617-461b-8a4f-c3a2eb0e642f" />

### 🌐 Churn Rate: International Plan vs. Activity Status

*Figure 5: Churn rate distribution based on whether customers have an international plan and whether they are active. Highlights how churn varies across combinations of plan type and activity level.*

| Intl Plan | No       | Yes      | Total   |
|-----------|----------|----------|---------|
| yes       | 71.19%   | 7.59%    | 24.88%  |
| no        | 20.01%   | 40.34%   | 27.07%  |
| Total     | 22.21%   | 34.31%   | 26.86%  |


---

## 🚀 Getting Started

To explore the dashboard:
1. Clone this repository  
2. Open `Dashboard.pbix` in Power BI Desktop  
3. Use slicers to filter by contract type, tenure, and payment method  
4. Explore churn patterns across segments

---

## 📬 Contact

For questions, feedback, or collaboration opportunities:

- **LinkedIn**: [Arvind Kumar](https://www.linkedin.com/in/arvind-kumar-560885231/)  
- **GitHub Issues**: Open a ticket in this repo  
- **Email**: arvind207kumar@gmail.com
