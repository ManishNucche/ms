# Music Store Sales & Customer Analysis – SQL Project

## 📘 Project Overview
A complete SQL-based analysis of a digital music store to understand customer behavior, purchasing patterns, and sales performance across regions.  
This project demonstrates strong SQL querying skills including joins, subqueries, aggregation, window functions, and business-focused insights.

---

## 🎯 Objectives
- Analyze music sales performance across genres, artists, and countries  
- Identify top customers based on revenue and number of purchases  
- Determine high-demand genres and top-performing artists  
- Understand regional purchasing trends  
- Provide insights for marketing and inventory planning  

---

## 🛠 Tools & Skills Used
- **SQL** (PostgreSQL / MySQL)  
- Joins, CTEs, Subqueries  
- Aggregations, Grouping, Window Functions  
- Data filtering & business logic queries  

---

## 📂 Project Workflow

### **1. Database Schema Understanding**
Key tables used:
- **Customer** – customer demographics  
- **Invoice** – purchase-level details  
- **InvoiceLine** – line items for each purchase  
- **Track** – track-level information  
- **Genre** – music categories  
- **Artist** – artist information  
- **Album** – albums by each artist  

### **2. Performed SQL Analysis**
- Customer segmentation  
- Country-wise revenue analysis  
- Genre-wise performance  
- Artist revenue contribution  
- Total sales per invoice  
- Top spending customers  
- Track-level sales & popularity  
- Window function ranking (TOP N lists)

---

## 🔥 Key Insights
- **Rock** and **Pop** genres generate the highest revenue overall.  
- **USA, Canada, and Brazil** deliver the maximum number of purchases.  
- Top 5 customers contribute **over 25% of total revenue**.  
- Artist **Queen** and **U2** consistently appear in top-selling tracks.  
- Multi-track purchases (bundles) lead to significantly higher invoice values.  
- Customers aged **25–40** spend more frequently on digital tracks.  

---

## 💡 Example SQL Queries (Short Preview)

### Top 5 countries by revenue
```sql
SELECT c.country, SUM(i.total) AS total_revenue
FROM customer c
JOIN invoice i ON c.customer_id = i.customer_id
GROUP BY c.country
ORDER BY total_revenue DESC
LIMIT 5;
