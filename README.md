# 🧠 State Complaints Dashboard | PowerBI

A dynamic and insightful Power BI dashboard visualizing **complaint patterns across Indian states (2023–2025)**.  
This project focuses on uncovering trends, resolution performance, and regional complaint distribution.

---

## 🚀 Project Overview

This dashboard provides an analytical view of:
- Total complaints and resolution rate 📊  
- Average resolution days ⏱️  
- State-wise complaint heat map of India 🗺️  
- Monthly and yearly complaint trends  
- Filters for year, status, and complaint category  

---

## 🛠️ Tools & Tech Stack

| Tool | Purpose |
|------|----------|
| **Power BI** | Dashboard & Visualizations |
| **Excel / CSV** | Data Source |
| **Python (EDA)** | Data Cleaning & Transformation |
| **GitHub** | Version Control |

---

## 📈 Key Insights

- ⚡ **Highest complaint volume:** Uttar Pradesh, Maharashtra, and Bihar  
- ✅ **Best resolution rate:** Kerala & Himachal Pradesh  
- ⏳ **Longest resolution time:** Delhi  
- 📅 **Trends show**: steady rise in domestic violence and cyber fraud cases

---

## 🧮 DAX Measures Used

```DAX
Total Complaints = COUNTROWS(Complaints)
Resolved Complaints = CALCULATE(COUNTROWS(Complaints), Complaints[Status] = "Resolved")
Resolution Rate % = DIVIDE([Resolved Complaints], [Total Complaints])
Average Resolution Days = AVERAGE(Complaints[Resolution_Days])
Open Complaints = COUNTROWS(FILTER(Complaints, Complaints[Status] <> "Resolved"))

--- 

🔗 View EDA Notebook: [`EDA/state-complaint-eda.ipynb`](./EDA/state-complaint-eda.ipynb)

---

## 📂 Folder Structure (Current)

state-complaints-dashboard/
├── data/ # Contains all raw CSV files
├── sql/ # Will contain database schema & EDA queries
├── powerbi/ # Will contain .pbix and exported dashboards
└── README.md # You're here!

---

👩‍💻 Author
Shaurya Shrivastava
📊 Data Analytics Enthusiast | Power BI | SQL | Python
