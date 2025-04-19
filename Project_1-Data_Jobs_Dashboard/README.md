# Excel Data Jobs Dashboard  
![1](https://github.com/user-attachments/assets/b5ed4862-242a-4cf7-84f3-1813f7b8e54b)

## Introduction  
This data jobs salary dashboard was created to help job seekers investigate salaries for their desired jobs and ensure they are being adequately compensated.  

The data is from my Excel course, which provides a foundation in analyzing data using this powerful tool. The data contains detailed information on job titles, salaries, locations, and essential skills that are presented here.  

### Dashboard File 
My final dashboard is in [Data_Jobs_Dashboard](https://github.com/Wassimadt/My_Excel_Projects/blob/98a7ade1a5e97b265452f9a38f2bededa34a3528/Project_1-Data_Jobs_Dashboard/Data_Jobs_Dashboard.xlsx)

### Excel Skills Used

The following Excel skills were utilized for analysis:

- **📉 Charts**
- **🧮 Formulas and Functions**
- **❎ Data Validation**

### Data Jobs Dataset

The dataset used for this project contains real-world data science job information from 2023.  
**👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

The dataset is available here [data_jobs_salary_all](https://github.com/Wassimadt/My_Excel_Projects/blob/eb1c852eef5f600f7198d93b3455970af9cdb8c1/Project_1-Data_Jobs_Dashboard/data_jobs_salary_all.xlsx)

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart
![2](https://github.com/user-attachments/assets/80f6c0f5-ecb6-4e50-82ea-f9722092065a)

- 🛠️ **Excel Features:** Utilized bar chart feature (with formatted salary values) and optimized layout for clarity.
- 🎨 **Design Choice:** Horizontal bar chart for visual comparison of median salaries.
- 📉 **Data Organization:** Sorted job titles by descending salary for improved readability.
- 💡 **Insights Gained:** This enables quick identification of salary trends, noting that Senior roles and Engineers are higher-paying than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart
![3](https://github.com/user-attachments/assets/bae6eeac-ff98-4d85-bb00-3a6ea7df7d9e)

- 🛠️ **Excel Features:** Utilized Excel's map chart feature to plot median salaries globally.
- 🎨 **Design Choice:** Color-coded map to visually differentiate salary levels across regions.
- 📊 **Data Representation:** Plotted median salary for each country with available data.
- 👁️ **Visual Enhancement:** Improved readability and immediate understanding of geographic salary trends.
- 💡 **Insights Gained:** Enables quick grasp of global salary disparities and highlights high/low salary regions.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
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

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

![4](https://github.com/user-attachments/assets/6f301608-8874-46ba-9eba-4df14104fc19)

📉 Dashboard Implementation

<img src="C:\Users\R-Tech\Documents\Project\Github\5
" width="400" height="500" alt="Salary Dashboard Title">

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table
![6](https://github.com/user-attachments/assets/dbb73dd3-59a6-4ff2-b862-52e6f416f0aa)

📉 Dashboard Implementation
![7](https://github.com/user-attachments/assets/fafaedfc-8d44-43c0-8f52-a00082cc7cc1)

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Overall usability of the dashboard is enhanced

![8](https://github.com/user-attachments/assets/1ffe322d-c089-4165-8398-d15576236f6d)


## Conclusion

I created this dashboard to showcase insights into salary trends across various data-related job titles. This dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.




