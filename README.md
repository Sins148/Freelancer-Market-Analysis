# Freelancer-Market-Analysis
PROJECT: Global Freelancer Market Analysis
Dataset: Global Freelancers Dataset — Kaggle
Rows: 1000
Columns: 12
Tools Used: Microsoft Excel, Power BI

PROJECT STRUCTURE
raw data folder — original untouched dataset
cleaned data folder — cleaned working file
Power BI file — dashboard and visualizations
README — this file, project documentation

DATA CLEANING LOG
Tool used: Microsoft Excel
Source file: global_freelancers_raw — untouched
Cleaning file: global_freelancers_raw Copy

gender — Standardized inconsistent values to Male and Female using Find and Replace.
hourly_rate — Removed currency symbols and USD prefix. Converted currency formatted cells to plain numbers. Formatted as whole number.
is_active — Standardized 1, 0, Y, N, yes to TRUE and FALSE using Find and Replace with Match Entire Cell Contents.
years_of_experience — Fixed accidental TRUE and FALSE replacement using nested IF formula. Blanks retained.
rating — Fixed accidental TRUE and FALSE values using nested IF formula. Blanks retained. Range confirmed 1 to 5.
client_satisfaction — Standardized mixed percentage and plain number formats using nested IF formula. Converted to plain whole numbers 0 to 100. Blanks retained.
Headers verified — all lowercase with underscores.
All categorical columns verified using filter. No inconsistencies found.

Blank cell policy: Blanks in hourly_rate, years_of_experience, rating, and client_satisfaction are intentionally left blank. Blank means data not collected. Filling with zero would corrupt aggregations. NULL handling managed at the Power BI stage.

POWER BI DASHBOARD
Tool: Microsoft Power BI Desktop
File: Project 1.pbix
DAX Measures created:
Total Freelancers = COUNTROWS of table
Avg Hourly Rate = AVERAGE of hourly_rate
Avg Rating = AVERAGE of rating
Avg Client Satisfaction = AVERAGE of client_satisfaction
Visuals built:
4 KPI cards — Total Freelancers, Avg Hourly Rate, Avg Rating, Avg Client Satisfaction
Bar chart — Avg Hourly Rate by primary skill
Bar chart — Total Freelancers by primary skill
Bar chart — Avg Client Satisfaction by primary skill
Bar chart — Total Freelancers by country
Donut chart — Active vs Inactive freelancers
3 slicers — gender, primary skill, country
Key insights:
Cybersecurity pays the most at $54.37 average hourly rate despite not being the most common skill. This suggests higher demand relative to supply compared to other skills.
DevOps has the highest freelancer count at 112 but ranks third in hourly rate at $53.97. Most competitive skill to enter due to high supply.
Active and inactive freelancers are nearly evenly split at 51% vs 49%. A high inactive rate suggests either project-based work cycles or platform retention issues.
Client satisfaction is remarkably consistent across all skills ranging from 79 to 80. No skill significantly outperforms others in client satisfaction.
South Korea and Canada lead in freelancer count by country, suggesting strong remote work culture in those regions.
