# Freelancer-Market-Analysis
# Global Freelancer Market Analysis

## Description
This project analyzes a global freelancer dataset to uncover patterns in hourly rates, skill demand, client satisfaction, and freelancer activity across different countries. The goal was to practice end-to-end data analysis — from raw data cleaning in Excel to building an interactive dashboard in Power BI that business stakeholders can use to make informed decisions about freelancer hiring and pricing.

## Dashboard Features
- Filter the entire dashboard by gender, primary skill, and country using interactive slicers
- Compare average hourly rates across 9 different skill categories
- Identify which countries have the highest freelancer supply
- Analyze active vs inactive freelancer distribution
- Track client satisfaction scores by skill to identify service quality patterns

## Project Overview
**Dataset:** Global Freelancers Dataset — Kaggle  
**Rows:** 1000 | **Columns:** 12  
**Tools Used:** Microsoft Excel, Power BI  

---

## Project Structure
- raw data folder — original untouched dataset
- cleaned data folder — cleaned working file
- Power BI file — dashboard and visualizations
- README — project documentation

---

## Data Cleaning Log
**Tool:** Microsoft Excel  
**Source file:** global_freelancers_raw (untouched)  
**Cleaning file:** global_freelancers_raw Copy  

- **gender** — Standardized inconsistent values to Male and Female
- **hourly_rate** — Removed currency symbols and USD prefix, converted to whole numbers
- **is_active** — Standardized 1, 0, Y, N, yes to TRUE and FALSE
- **years_of_experience** — Fixed accidental TRUE/FALSE replacement using nested IF formula
- **rating** — Fixed accidental TRUE/FALSE values, range confirmed 1 to 5
- **client_satisfaction** — Standardized mixed percentage and plain number formats to whole numbers 0 to 100
- Headers verified — all lowercase with underscores
- All categorical columns verified using filter — no inconsistencies found

**Blank Cell Policy:** Blanks in hourly_rate, years_of_experience, rating, and client_satisfaction are intentionally left blank. Blank means data not collected. Filling with zero would corrupt aggregations.

---

## Power BI Dashboard
**Tool:** Microsoft Power BI Desktop  
**File:** Project 1.pbix  

**DAX Measures:**
- Total Freelancers = COUNTROWS
- Avg Hourly Rate = AVERAGE of hourly_rate
- Avg Rating = AVERAGE of rating
- Avg Client Satisfaction = AVERAGE of client_satisfaction

**Visuals Built:**
- 4 KPI cards — Total Freelancers, Avg Hourly Rate, Avg Rating, Avg Client Satisfaction
- Bar chart — Avg Hourly Rate by primary skill
- Bar chart — Total Freelancers by primary skill
- Bar chart — Avg Client Satisfaction by primary skill
- Bar chart — Total Freelancers by country
- Donut chart — Active vs Inactive freelancers
- 3 slicers — gender, primary skill, country

---

## Key Insights
1. Cybersecurity commands the highest average hourly rate at $54.37 despite not being the most common skill — suggesting a supply-demand gap
2. DevOps has the highest freelancer count at 112 but ranks third in hourly rate at $53.97 — most competitive skill to enter
3. Active and inactive freelancers are nearly evenly split at 51% vs 49% — high inactive rate suggests project-based work cycles
4. Client satisfaction is consistent across all skills ranging 79 to 80 — no skill significantly outperforms others
5. South Korea and Canada lead in freelancer count by country

---

## Status
- Excel cleaning — Complete
- Power BI dashboard — Complete
- GitHub — Complete
- LinkedIn update — Pending
