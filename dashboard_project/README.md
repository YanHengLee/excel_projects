# Excel Salary Dashboard

![excel_projdb_rec-ezgif com-crop](https://github.com/user-attachments/assets/7a63eba8-1803-4bf7-af05-b5f951c74943)

## 🚀 Introduction

This project is an interactive Excel dashboard that analyzes **median annual salaries** for **tech-related jobs** among **different scheduled job types(full-time, part-time etc.)** across **different countries**. The "Salary Calculator" sheet contains a dashboard, designed to allow users to explore and compare salary trends dynamically.

### 🛠️ Excel Skills Used

The following excel skill were utilized for analysis:
* 📉 Charts
* 🧮 Formulas and Functions
* ❎ Data Validation

## 🔎 Project Structure

The [salary_dashboard.xlsx]() excel file contains a data sheet, the salary calculator dashboard sheet, and other behind the scene sheets that contains the logic behind creating the dashboard.

* **Data:** Raw dataset from a [web-scrapping website](https://datanerd.tech/) containing informations on job titles, locations, salaries, countries, skills required etc.
* **Salary Calculator:** Interactive dashboard where users can select a **job title**, **country**, and **job scheduled type** to view various informations about the job. It contains two bar charts, a world map, median annual salary card, the top job posting platform card, and a job count card.

## 📖 Dashboard Build
### 📊 Charts

**Median Annual Salaries from Various Tech-related Jobs - Bar Chart**
<img width="1063" height="557" alt="image" src="https://github.com/user-attachments/assets/88342760-946e-40f0-b013-95cad5409143" />
* **✅ Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
* **🎨 Design Choice:** Horizontal bar chart for visual comparison of median salaries.
* **📉 Data Organization:** Sorted job titles by descending salary for improved readability.
* **💡 Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

**Country Median Annual Salaries - Map Chart**
<img width="980" height="559" alt="image" src="https://github.com/user-attachments/assets/a70fa213-c2bf-4330-8c92-23f3743c5087" />
* **✅ Excel Features:** Utilized excel's map chart feature to plot median salaries globally.
* **🎨 Design Choice:** Color-coded map to visually differentiate salary levels across regions.
* **📋 Data Representation:** Plotted median salary for each country with available data.
* **👁️ Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
* **💡 Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

**Median Annual Salaries of Different Scheduled Type Jobs - Bar Chart**
<img width="888" height="533" alt="image" src="https://github.com/user-attachments/assets/bcc1042c-3705-47c5-8db2-0ee189fc9960" />
* **💡 Insights Gained:** Using the same design choice and features as the previous bar chart, enables user to gain insights on salary trends on different type of scheduled work.

### 🧮 Formulas and Functions

**Median Annual Salary by Job Titles**

```excel
=MEDIAN(
    IF(
        (jobs[job_title_short]=A2)*
        (jobs[job_country]=country)*
        (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
        (jobs[salary_year_avg]<>0),
        jobs[salary_year_avg]
    )
)
```

* **🔍 Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
* **📈 Array Formula:** Utilizes MEDIAN() function with nested IF() statement to analyze an array.
* **🎯 Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
* **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

**📑 Backgroud Table**

<p align="center">
  <img width="400" height="320" alt="image" src="https://github.com/user-attachments/assets/483bb4af-b5bd-40f8-bb3e-b0e9433c3912" />
</p>

<p align="center">
  <img width="290" height="300" alt="image" src="https://github.com/user-attachments/assets/80d25356-b4ad-4835-8ed3-41e7888d1295" />
</p>

**📈 Dashboard Implementation**

<p align="center">
  <img width="500" height="610" alt="image" src="https://github.com/user-attachments/assets/cb88c5ee-a4d2-4383-b1d6-94dbb3d79001" />
</p>

**📐 Count of Job Schedule Type**

```excel
=FILTER(K2#,NOT(ISNUMBER(SEARCH("and",K2#)))*(K2#<>0))
```

* **🔍 Unique List Generation:** This Excel formula below employs the FILTER() function to exclude entries containing "and", and omit zero values.
* **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

**📑 Backgroud Table**

<p align="center">
  <img width="344" height="200" alt="image" src="https://github.com/user-attachments/assets/2439ae36-1ff6-4bb7-baa9-a8004d92ca6d" />
</p>

<p align="center">
  <img width="344" height="200" alt="image" src="https://github.com/user-attachments/assets/b539df35-b53f-45e8-8489-93a9605a334d" />
</p>

**📈 Dashboard Implementation**

<p align="center">
  <img width="350" height="410" alt="image" src="https://github.com/user-attachments/assets/eef20165-98ce-4ee9-b2f7-1398bee3f189" />
</p>

### ✅ Data Validation

Implementing the filtered list as a data validation rule under the <code>Job Title</code>, <code>Country</code>, and <code>Type</code> option in the Data tab ensures:
* User input is restricted to predefined, validated schedule types
* Incorrect or inconsistent entries are prevented
* Overall usability of the dashboard is enhanced

## ⭐ Conclusion

This excel dashboard contain insights on annual salary trends across various data-related jobs. Utilizing data from online sources, this dashboard allow users to make informed decisions while choosing their career paths, exploring the functionalities to understand how location and job type influence salaries.

This project showcased my ability to use **Excel** for building interactive analytical dashboards, using excel formulas, functions, and charts to transform raw datasets into meaningful insights.
