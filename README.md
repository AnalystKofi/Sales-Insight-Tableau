# Sales Performance Dashboard (Tableau + MySQL)
## 🔗 Tableau Public Dashboard

View the live interactive dashboard here:  
https://public.tableau.com/app/profile/kofi.obeng.nti/viz/salesinsight_17625514686700/Dashboard1

This repository contains my first Tableau project, where I built a full end-to-end sales performance dashboard using data sourced from MySQL. The project demonstrates the complete analytical workflow: data extraction, cleaning, transformation, modeling, visualization, and business insight communication.

---

## 🗂 Project Overview

The goal of this project was to analyze company sales performance across multiple markets, customers, and products, and to highlight key business opportunities. The dashboard provides visibility into revenue trends, customer contribution, product profitability, and geographic performance.

---

## 🔄 Data Workflow

| Step | Task | Tool | Description |
|------|------|------|-------------|
| 1 | Data Extraction | MySQL | Queried and exported multiple relational tables from a MySQL database. |
| 2 | Data Loading | Tableau | Connected Tableau directly to MySQL for live data integration. |
| 3 | Data Cleaning | Tableau Prep / Tableau Data Pane | Standardized formats, resolved inconsistencies, removed duplicates, validated joins. |
| 4 | Data Modeling | Tableau | Joined tables based on keys (e.g., product code, customer ID, region code). |
| 5 | Data Transformation | Tableau Calculated Fields | Converted USD to INR using an `IF` condition to maintain currency consistency. |
| 6 | Dashboard Development | Tableau | Designed interactive visuals for business understanding and decision-making. |

---

## 💡 Currency Conversion Logic

To ensure consistent reporting, all USD denominated fields were converted to INR.  
This was achieved using a Tableau **Calculated Field**:
```DAX
IF [Currency] = "USD" THEN [SalesAmount] * 72
ELSE [Sales Amount]
END
```
This brought all measures into a single comparable currency for accurate aggregations.

---

## 📊 Dashboard Features

The final dashboard includes:

- **Revenue KPIs** (Total Revenue, Quantity Sold, Avg Revenue per Unit)
- **Revenue Trend Over Time** (Yearly and Monthly performance patterns)
- **Market/Regional Performance Comparison**
- **Top 5 Customers by Revenue Contribution**
- **Top 5 Products by Revenue**
- **Interactive Filtering** for product category, region, or time period

The layout was designed for clarity, stakeholder readability, and insight-driven storytelling.

---

## 🔍 Key Business Insights

- **One region accounts for more than 50% of total revenue**, indicating strong market performance but also concentration risk.
- **Revenue growth peaked in 2018–2019**, followed by a soft decline, suggesting market change or external factors.
- **One product (Product040)** drives a large portion of total sales, showing strong market fit but also product dependency.
- **Top-tier customers contribute disproportionately to revenue**, highlighting opportunities to strengthen mid-tier customer relationships.
- **Seasonal demand trends are visible**, which can inform inventory planning and promotional timing.

These insights would support strategic decisions in market expansion, customer retention, and product diversification.

---

## 📁 Repository Structure
📦 Sales-Performance-Dashboard
┣ 📁 data/ # (If applicable) Raw or sample data files
┣ 📁 workbook/ # Tableau workbook (.twb/.twbx)
┣ 📁 screenshots/ # Dashboard images for preview
┗ README.md # Project documentation


---

## 🧭 Next Steps / Enhancements

- Add explanatory insight call-outs directly onto the dashboard panels.
- Incorporate forecasting models (e.g., moving averages, exponential smoothing).
- Extend customer segmentation using RFM (Recency, Frequency, Monetary Value) analysis.
- Publish the dashboard to Tableau Public and link for live interaction.

---

## 🤝 Feedback & Connection

I am continuously improving my data storytelling and dashboard design skills.  
I welcome feedback on structure, visuals, and insight interpretation.

If you're working in **Data Analytics, Business Intelligence, or Visualization**, feel free to:
- ⭐ Star the repo
- 📝 Open issues or suggestions
- 🔗 Connect with me on LinkedIn

Let’s grow together.












