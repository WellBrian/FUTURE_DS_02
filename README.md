# FUTURE_DS_02

# 📘 **Social Media Campaign Performance Tracker (Power BI)**

## 📌 **Project Overview**

The **Social Media Campaign Performance Tracker** is an interactive **Power BI dashboard** designed to analyze and visualize digital marketing performance across platforms such as Facebook, Instagram, and other paid ad channels.

This dashboard helps marketing teams monitor KPIs, compare campaign results, identify high-performing content, and make informed decisions to optimize future campaigns.

---

## 🎯 **Objectives**

The project aims to:
✔ Track overall campaign performance
✔ Compare engagement across audience segments (age, education, region)
✔ Identify top-performing ads or posts
✔ Calculate meaningful KPIs like CTR, Conversion Rate, CPC & ROI
✔ Provide insights using Power BI tools such as Decomposition Tree 

---

## 📁 **Dataset**

This project uses a **social media marketing dataset** 

---

## 🧰 **Tools Used**

| Tool            | Purpose                               |
| --------------- | ------------------------------------- |
| **Power BI**    | Dashboard development & data modeling |
| **Power Query** | Data cleaning & transformation        |
| **DAX**         | Calculated measures and KPIs          |
| **Excel**       | Initial exploration & quick checks    |

---

## 🛠️ **Data Cleaning & Transformation (Power Query)**

Key steps performed:

### ✔ Removed symbols from numeric columns

* Cleaned **Income/Spend** fields by removing `$` and `,`
* Converted them to decimal numbers

### ✔ Created new fields

* **Age = 2025 – Year_Birth**
* **Age Groups** (18–25, 26–35, 36–45, 46–60, 60+)
* **Total Children**

## 📊 **Key DAX Measures**

### **Engagement**

```DAX
Total_Engagement = SUM(marketing_data[NumWebPurchases]) +
SUM(marketing_data[NumStorePurchases]) +
SUM(marketing_data[NumDealsPurchases]) +
SUM(marketing_data[NumCatalogPurchases])
```

### **Engagement Rate**

```DAX
Engagement Rate = SUM(marketing_data[NumWebVisitsMonth]) /
marketing_data[Total_Engagement]
```

### **Conversion Rate**

```DAX
Conversion Rate = DIVIDE(SUM(marketing_data[Response]),
COUNTROWS(marketing_data))
```

---

## 📈 **Dashboard Features**

### 🔹 **1. Overview Page**

Displays key campaign metrics:

* CTR 
* Conversion Rate
* Total Spend 
* Trend analysis over time

---

### 🔹 **2. Audience Insights Page**

Breaks down engagement by:

* **Age Group**
* **Education Level**
* **Country**
* **Marital Status**

Includes a **Clustered Column Chart** comparing education levels across age groups.

---

### 🔹 **3. Campaign Performance Page**

Shows:

* Post engagement comparison
* Spend vs engagement efficiency scatter plot

---

### 🔹 **4. Advanced Analytics Page**

Contains:

* **Decomposition Tree**

  * Used to identify drivers of Engagement (Age, Education, Income, Country)

---

## 🔍 **Insights Generated**

Sample insights from the dashboard include:

* Most engagement comes from **26–35 age group**
* Users with **Graduation or Master’s level education** engage more
* Certain campaigns drive high impressions but low conversions

---

## 💡 **Future Improvements**

* Include sentiment analysis using ad comments
* Integrate real Instagram API data
* Add forecasting for future ad performance
* Build automated refresh with Power BI Gateway

---

## 👨‍💻 **Author**

**Brian Ouko**
Data Scientist | Analyst | Environmental Scientist
Passionate about data-driven marketing, analytics, and digital strategy.

