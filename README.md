# HR Analysis Report

This repository contains an interactive HR Analysis Report, designed to provide comprehensive insights into employee overview, trends, performance, compensation, and data quality within an organization. The report is built using Power BI and leverages various Power Query views and DAX measures/calculated columns to prepare and transform the data effectively. It aims to help HR departments make data-driven decisions.

## Table of Contents

* [Project Overview](#project-overview)

* [Key Features](#key-features)

* [Power Query Views](#power-query-views)
 
* [DAX Measures and Calculated Columns](#dax-measures-and-calculated-columns)
 
* [Dataset Fields](#dataset-fields)

* [Dashboards](#dashboards)

  * [Employee Overview & Trends](#1-employee-overview--trends)

  * [Performance, Compensation & Data Quality](#2-performance-compensation--data-quality)

* [How to Use](#how-to-use)

* [Future Enhancements](#future-enhancements)

* [Contact](#contact)

* [License](#license)

## Project Overview

The HR Analysis Report is a powerful tool for visualizing key HR metrics and trends. It consolidates various aspects of HR data into two main dashboards, enabling quick identification of patterns, potential issues, and areas for improvement. This report is invaluable for HR managers, department heads, and executives seeking to understand their workforce better.

## Key Features

* **Interactive Filters:** Easily filter data by Year, Month, Department, and Gender to get specific insights.

* **Employee Overview:** Get a quick snapshot of active employees, average salary, and number of departments.

* **Trend Analysis:** Monitor active vs. inactive employee trends and monthly joiners & exits over time.

* **Attrition Analysis:** Understand attrition rates across different departments and years.

* **Manager Load Analysis:** Visualize the distribution of employees under different managers.

* **Performance Insights:** Analyze gender ratio by department and identify performance-related metrics.

* **Compensation Analysis:** Gain insights into average leave balance and salary banding.

* **Data Quality Monitoring:** Identify potential data inconsistencies like invalid joining/exit records or negative salaries.

* **Leave Balance Utilization:** Analyze leave balance distribution (High, Low, Normal) across departments.

## Power Query Views

Several custom views have been created using Power Query to prepare and shape the data for effective analysis:

* **Active Employees:** A view specifically created to show the current active employees in the organization.

* **Upcoming Retirements:** This view identifies employees nearing retirement. Currently based on age, it has conditions to also consider Date of Birth (DOB) for more precise calculations if DOB data becomes available.

* **Employees with <3 years of tenure:** A view to highlight employees who have been with the organization for less than three years, aiding in talent retention strategies.

## DAX Measures and Calculated Columns

The report utilizes several DAX measures and calculated columns for advanced calculations and data categorization:

* **Date Error**: A calculated column to identify and flag potential errors related to dates (e.g., ExitDate before DOJ).

* **Employee Stat.** (Employee Status): Likely a calculated column to determine the current employment status (e.g., Active, Exited).

* **Leave Category**: A calculated column to categorize LeaveBalance into segments like High, Low, or Normal.

* **Salary Band**: A calculated column to categorize salaries into predefined bands for better analysis and visualization.

* **Salary Outlier**: A calculated column to flag salaries that fall outside the normal range, indicating potential outliers.

## Dataset Fields

The core dataset includes the following fields, used for analysis and reporting:

* `EmployeeID`

* `Name`

* `Department`

* `DOJ` (Date of Joining)

* `Salary`

* `ManagerID`

* `LeaveBalance`

* `Attendance`

* `Gender`

* `ExitDate`

## Dashboards

The report consists of two primary dashboards:

### 1. Employee Overview & Trends

This dashboard focuses on the overall employee landscape and key trends.
<img width="879" height="494" alt="image" src="https://github.com/user-attachments/assets/fb36303f-f296-4742-a672-dac42433e711" />

**Key Metrics & Visualizations:**

* **No. of Active Employees:** Current count of active employees.

* **Avg. Salary:** Average salary across the organization.

* **Departments:** Number of departments.

* **Active vs Inactive Employee Report:** Bar chart showing the number of active and exited employees per department.

* **Attrition Analysis:** Stacked bar chart illustrating attrition rates by department over different years.

* **Manager Load Analysis:** Line chart showing the number of employees under various managers.

* **Gender Ratio by Department:** Donut chart displaying the percentage distribution of gender across departments.

### 2. Performance, Compensation & Data Quality

This dashboard delves into employee performance, compensation aspects, and the integrity of HR data.
<img width="873" height="498" alt="image" src="https://github.com/user-attachments/assets/f5d3d6fe-41d3-498a-a50c-5d82f7d94062" />

**Key Metrics & Visualizations:**

* **Monthly Joiners & Exits:** Line chart tracking the count of new joiners and exits each year.

* **No. of Employees with Attendance Less Than 90%:** Count of employees with low attendance, derived from the `Attendance (%)` measure.

* **Avg Leave Balance:** Average leave balance across all employees.

* **No. of Invalid Joining and Exit Records:** Identifies data quality issues flagged by the `Date Error` calculated column.

* **No of Records Having Negative Salary:** Highlights data errors where salary entries are negative.

* **Leave Balance Utilization:** Stacked bar chart showing the breakdown of High, Low, and Normal leave balances per department, using the `Leave Category` column.

* **Salary Analysis & Banding:** Box plot visualizing salary distribution and outliers by department, leveraging `Salary Band` and `Salary Outlier` columns.


## How to Use

To view and interact with this report:

1. **Clone the repository:**

   ```
   git clone [https://github.com/Mridul180304/HR-Data-Analysis.git](https://github.com/Mridul180304/HR-Data-Analysis.git)
   
   ```

2. **Open the Power BI file:**
   Navigate to the cloned directory and open the `.pbix` file (e.g., `HR Report Analysis.pbix`) using Power BI Desktop.

3. **Explore the Dashboards:**
   Switch between the "Employee Overview & Trends" and "Performance, Compensation & Data Quality" tabs at the bottom of the Power BI interface.

4. **Utilize Filters:**
   Use the "Filter By" pane on the left to refine your analysis by Year, Month, Department, and Gender.

*(Note: Power BI Desktop is required to open and interact with the `.pbix` file.)*

## Future Enhancements

* Integration with real-time HR data sources.

* Addition of more granular performance metrics (e.g., performance ratings, training data).

* Predictive analytics for attrition forecasting.

* Drill-through capabilities for detailed employee profiles.

* Mobile-friendly optimization.

## Contact

For any questions or suggestions, please feel free to reach out.
Gmail- mridulchawla20@gmail.com

## License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details
