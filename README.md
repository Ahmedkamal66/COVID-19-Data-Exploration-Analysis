# 🦠 COVID-19 Data Exploration & Analysis

## 📝 Project Overview
This project involves an in-depth exploration of global COVID-19 data, focusing on infection rates, death tolls, and vaccination progress across various countries and continents. Using **SQL Server (T-SQL)**, the analysis transforms raw data into actionable insights, providing a clear picture of the pandemic's impact from a statistical perspective.

The project demonstrates the ability to handle large datasets, perform complex joins, and use advanced SQL features to answer critical questions about global health trends.

---

## 🛠️ Tools & Technologies
* **Language:** SQL (T-SQL)
* **Database Management System:** Microsoft SQL Server
* **Key SQL Techniques Used:**
  * **Joins:** Combining datasets (Deaths and Vaccinations) for holistic analysis.
  * **Window Functions:** Calculating rolling totals and partitioned data.
  * **CTEs (Common Table Expressions):** Structuring complex queries for better readability.
  * **Temp Tables:** Managing intermediate data for performance and calculation efficiency.
  * **Views:** Creating persistent virtual tables for future visualizations (e.g., Tableau/Power BI).
  * **Data Transformation:** Using `CAST`, `CONVERT`, and `NULLIF` for data integrity.

---

## 🔍 Key Analysis & Insights

### 1. Mortality & Infection Risk
* **Total Cases vs. Total Deaths:** Calculates the likelihood of dying if you contract COVID-19 in specific regions (e.g., Africa).
* **Total Cases vs. Population:** Determines the percentage of the population that has been infected over time.
* **Peak Infection Rates:** Identifies countries with the highest infection counts relative to their population size.

### 2. Regional & Global Impact
* **Death Toll by Continent:** Aggregates total death counts to show the impact at a continental level.
* **Global Numbers:** Provides a snapshot of global cases, deaths, and the overall death percentage.

### 3. Vaccination Progress
* **Rolling Vaccination Count:** Uses `SUM(...) OVER (Partition by...)` to track the cumulative number of people vaccinated daily per location.
* **Vaccination Percentage:** Calculates what percentage of the population has received at least one vaccine dose using both CTEs and Temporary Tables to demonstrate different technical approaches.

---

## 🚀 SQL Implementation Highlights

### Advanced Calculations
The project showcases proficiency in resolving the "division by zero" error using `NULLIF` and ensuring correct data types for mathematical operations using `CAST` and `CONVERT`.

### Data Architecture
* **CTEs:** Used to perform calculations on the results of window functions in the same query.
* **Temp Tables:** Created to store vaccination data temporarily for more flexible querying.
* **Views:** A dedicated view `PercentPopulationVaccinated` was created to serve as a clean data source for visualization tools.

---

## 📂 How to Run
1. Ensure you have **SQL Server Management Studio (SSMS)** installed.
2. Import the `covidDeaths` and `covidVAccinatio` datasets into your database.
3. Run the scripts in `Coviod_project1.sql` sequentially to explore the data and generate the final views.

---

## 💡 Future Scope
The outputs generated from these SQL scripts are structured to be easily integrated into a data visualization tool like **Tableau** or **Power BI** to create an interactive COVID-19 Dashboard.
