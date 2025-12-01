# 📞 Call Centre Dashboard – Power BI  
A complete two-page interactive Power BI dashboard designed to analyze call centre performance using detailed operational metrics and customer interaction data.  
This project provides both **high-level insights (Home Page)** and **record-level visibility (Grid Page)** with multiple slicers for dynamic filtering.

---

## 🖥️ Dashboard Pages

### **1️⃣ Home Page – Executive Summary**
The Home page provides a complete overview of call centre performance using KPI cards and visual analytics.

#### **KPIs Displayed**
- **Calls:** 32.94K  
- **Call Duration (Hrs):** 13.74K  
- **Call Duration (Min):** 824.22K  
- **Avg Call Duration (Min):** 25.02  
- **Response Time %:** 75%

#### **Visuals on Home Page**
- **Calls by Day (Bar Chart)**  
  - Daily call volume: Sun–Sat  
  - Range: 4.3K to 5.6K  

- **Calls by State (Filled Map)**  
  - State-wise call density  
  - Darker shades = higher call volume  

- **Calls by Reason (Treemap)**  
  - Billing Question  
  - Payments  
  - Service Issues  
  - Others

- **Calls by Channel (Donut Chart)**  
  - Call-Center (largest category)  
  - Chatbot  
  - Email  
  - Web  

- **Calls by Sentiment (Bar Chart)**  
  - Negative: 11.1K  
  - Neutral: 8.8K  
  - Very Negative: 6.0K  
  - Positive: 3.9K  
  - Very Positive: 3.2K  

- **Calls by Call Centres (Bar Chart)**  
  - Los Angeles – 14K  
  - Baltimore – 11K  
  - Chicago – 5K  
  - Denver – 3K  

---

## **2️⃣ Grid Page – Detailed Record-Level View**
This page displays a detailed, scrollable table for granular analysis.

#### **KPIs Displayed**
- **Calls:** 29  
- **Call Duration (Hrs):** 12.53  
- **Call Duration (Min):** 752.00  
- **Avg Call Duration (Min):** 25.93  
- **Response Time %:** 76%  

#### **Grid Table Columns**
- ID  
- Customer Name  
- Channel  
- State  
- Reason  
- Response Time (Within SLA / Below SLA)  
- City  
- Call Duration (Min)

---

## 🎛️ Filters / Slicers Used in Both Pages

### **Home Page Slicers**
- **Date range** (From → To)  
- **Channel** (All, Call-Center, Chatbot, Email, Web)  
- **City** (All cities)

### **Grid Page Slicers**
- **Date (Two selectors: start date & end date)**  
- **Channel** (Call-Center selected in example screenshot)  
- **City** (Albany selected in example screenshot)

---

## 🧠 Data Model Overview
- **Fact Table:** Call Log/Interaction Data  
- **Dimensions:**  
  - Date  
  - Channel  
  - Call Reason  
  - State  
  - City  
  - Customer  

Relationships are used to support cross-filtering and dynamic interactions.

---

## 📐 Metrics / DAX (Example Measures)
```DAX
Total Calls = COUNT(CallData[ID])

Total Duration (Hrs) = SUM(CallData[CallDurationMin]) / 60

Average Duration (Min) = AVERAGE(CallData[CallDurationMin])

Response Time % = 
DIVIDE(
    CALCULATE(COUNTROWS(CallData), CallData[Response]="Within SLA"),
    COUNTROWS(CallData)
)
```
## 🔧 Tools & Technologies

Power BI Desktop

Power Query for data cleaning

DAX for calculated measures

Interactive UI with navigation menu

KPI cards, maps, treemaps, donut charts, bar charts, grid tables

## 🚀 How to Use

Download the .pbix file.

Open in Power BI Desktop (latest version).

Refresh data and adjust visuals if needed.

Use slicers to interact with the dashboard.

## ⭐ About This Project

This dashboard is ideal for:

Understanding call centre performance

Monitoring SLA compliance

Evaluating agent/call center productivity

Studying customer sentiment trends

Analyzing call reasons and traffic patterns

## 👤 **Author**

**SAGAR SS :**
Data Analyst || 
6-Month Internship Experience
