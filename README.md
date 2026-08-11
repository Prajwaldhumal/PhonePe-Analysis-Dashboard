# PhonePe-Analysis-Dashboard
# 📊 PhonePe Transaction Analysis Dashboard

An interactive **Power BI dashboard** designed to analyze PhonePe-style UPI transaction data and uncover insights into transaction performance, user behavior, payment services, and time-based transaction trends.

The project was developed end-to-end, starting from raw Excel data through **Power Query data cleaning, data modeling, DAX calculations, and interactive dashboard development**.

---

## 📌 Dashboard Overview

The dashboard provides a single-page view of key transaction and user metrics.

### Key KPIs

- 💰 **Total Transaction Value**
- 🔢 **Total Transactions**
- ✅ **Success Rate**
- 👥 **Total Users**
- 📈 **Month-over-Month Transaction Value Growth**
- 📊 **Month-over-Month Transaction Volume Growth**

### Dashboard Visualizations

- **Top Users by Transaction Value**  
  Ranks users based on their total transaction value.

- **Transaction Value by Service**  
  Compares transaction values across different PhonePe services.

- **Monthly Transaction Trend**  
  Shows transaction value and transaction volume over time.

- **User Age Segments**  
  Categorizes users into:
  - Gen Z
  - Millennials
  - Gen X
  - Boomers

- **Weekday vs Weekend Analysis**  
  Compares transaction activity between weekdays and weekends.

- **Interactive Filters**  
  Users can filter the dashboard by:
  - Month
  - Payment Status

- **Custom Tooltips**  
  Additional information about service types and age segments is displayed through interactive hover tooltips.

---

## 🖼️ Dashboard Preview

![PhonePe Dashboard](![Uploading image.png…]()
)

> Replace `![Uploading image.png…]()
` with the actual screenshot file uploaded to this repository.

---

## 🗂️ Dataset

The dashboard was built using an Excel workbook containing two primary tables.

| Table | Columns |
|---|---|
| `All_Transactions` | Transaction_ID, Amount, User_ID, Service, Service Type, Payment_Status, Reason, Date |
| `All_Users` | User_ID, Name, Age, Join_Date |


To use the Power BI template with another dataset, maintain the same table and column structure or modify the Power Query source accordingly.

---

## 🧹 Data Cleaning & Transformation

Data preparation was performed using **Power Query**.

The following transformations were applied:

- Removed duplicate transaction records
- Removed records with blank User IDs
- Cleaned and standardized payment status categories
- Preserved detailed transaction failure reasons such as:
  - Wrong PIN
  - Insufficient Balance
  - Server Error
  - Other failure reasons
- Created an **Age Segment** column
- Created a dedicated **Date Table**
- Added month, quarter, weekday, and weekend attributes
- Prepared the data model for time-based analysis

---

## 🏗️ Data Model

The Power BI data model connects:

```text
All_Users
    │
    │ User_ID
    ▼
All_Transactions
    │
    │ Date
    ▼
Date_Table
