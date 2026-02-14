# Excel Salary Dashboard

![excel_projdb_rec-ezgif com-crop](https://github.com/user-attachments/assets/7a63eba8-1803-4bf7-af05-b5f951c74943)

## 🚀Introduction

This project is an interactive Excel dashboard that analyzes **median annual salaries** for **tech-related jobs** among **different scheduled job types(full-time, part-time etc.)** across **different countries**. The "Salary Calculator" sheet contains a dashboard, designed to allow users to explore and compare salary trends dynamically.

## 🔎Project Structure

The [salary_dashboard.xlsx]() excel file contains a data sheet, the salary calculator dashboard sheet, and other behind the scene sheets that contains the logic behind creating the dashboard.

* **Data:** Raw dataset from a [web-scrapping website](https://datanerd.tech/) containing informations on job titles, locations, salaries, countries, skills required etc.
* **Salary Calculator:** Interactive dashboard where users can select a **job title**, **country**, and **job scheduled type** to view various informations about the job. It contains two bar charts, a world map, median annual salary card, the top job posting platform card, and a job count card.

## 📖 Dashboard Build
### 📊Charts

**Median Annual Salaries from Various Tech-related Jobs - Bar Chart**
<img width="1063" height="557" alt="image" src="https://github.com/user-attachments/assets/88342760-946e-40f0-b013-95cad5409143" />
* **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
* **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
* **Data Organization:** Sorted job titles by descending salary for improved readability.
* **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

**Country Median Annual Salaries - Map Chart**
<img width="980" height="559" alt="image" src="https://github.com/user-attachments/assets/a70fa213-c2bf-4330-8c92-23f3743c5087" />
* **Excel Features:** Utilized excel's map chart feature to plot median salaries globally.
* **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
* **Data Representation:** Plotted median salary for each country with available data.
* **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
* **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

**Median Annual Salaries of Different Scheduled Type Jobs - Bar Chart**
<img width="888" height="533" alt="image" src="https://github.com/user-attachments/assets/bcc1042c-3705-47c5-8db2-0ee189fc9960" />

