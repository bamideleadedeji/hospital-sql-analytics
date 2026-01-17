# Hospital Operations: SQL-Driven Business Intelligence 

![SQL](https://img.shields.io/badge/Language-SQL_SQLite-blue)
![Database](https://img.shields.io/badge/Architecture-Normalized_Relational-orange)
![Insights](https://img.shields.io/badge/Focus-Operational_Efficiency-green)

## Project Overview
This project demonstrates the transition from flat-file data processing to **Relational Database Management**. I converted a medical appointment dataset into a normalized SQLite database to perform complex operational analysis that simple spreadsheets cannot handle.

##  Database Architecture
I architected a two-table relational system to reduce data redundancy:
* **Patients Table:** Stores demographic info (Age, Gender, Scholarship) with `PatientId` as the Primary Key.
* **Appointments Table:** Stores transactional visit data with a Foreign Key link to the Patients table.

##  Key SQL Techniques Demonstrated
* **JOIN Operations:** Merging patient demographics with visit history to find high-risk cohorts.
* **Date Engineering:** Using `strftime` and `CASE` statements to extract Day-of-Week trends.
* **Aggregation & Filtering:** Utilizing `GROUP BY` and `HAVING` to identify "Repeat Offenders" (patients with multiple no-shows).

##  Strategic Insight
The analysis revealed that **Monday** and **Friday** carry the highest no-show rates. 
**Recommendation:** Implement an automated SMS reminder 24 hours prior to Monday appointments to reclaim lost revenue.

##  Repository Contents
* `hospital_analytics.ipynb`: Python/SQL hybrid notebook.
* `hospital.db`: The SQLite database file containing the normalized tables.
* `noshow_by_day.png`: Visualization of the SQL-derived results.
