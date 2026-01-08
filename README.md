# HR_Analytics : Employee Presence & Trends Dashboard
📊 Project Overview
AtliQ Technologies required a data-driven approach to monitor employee attendance and work preferences. This project transforms raw attendance data from Excel into an interactive Power BI dashboard that helps stakeholders (HR Managers and Founders) make decisions regarding office capacity planning, team-building activities, and employee wellness.

🏨 Business Problem
The HR department was manually managing Excel sheets across multiple months. They needed to answer:

What is the overall employee presence percentage?

Are there specific days when WFH is significantly higher?

Is there a trend in sick leaves that might indicate a seasonal health issue or "burnout"?

How can office space be better utilized based on hybrid work patterns?

🛠️ Tech Stack
Tool: Power BI Desktop

Data Source: Excel (Multi-sheet attendance data)

ETL: Power Query

Data Modeling: Star Schema / Measures Table

Language: DAX (Data Analysis Expressions)

🏗️ Project Workflow
1. Requirement Gathering
Identified key metrics (KPIs) like Presence %, WFH %, and Sick Leave (SL) %.

Defined the "why" behind the metrics: e.g., using presence data to schedule team lunches on high-attendance days (Tuesdays) and planning infrastructure maintenance on low-attendance days (Fridays).

2. Data Transformation (Power Query)
Multi-Sheet Extraction: Handled the challenge of combining multiple Excel sheets with inconsistent column headers (dates).

Custom Functions: Created a Power Query template and converted it into a custom function to automate the transformation of new monthly data.

Unpivoting: Transformed wide-format date columns into a long-format "Date" and "Status" column for better analysis.

Data Cleaning: Removed non-working days (Weekends/Holidays), handled nulls, and filtered out error rows.

3. Data Modeling & DAX
Created a dedicated Measures Table to keep the model organized.

Key DAX Measures Created:

Total Working Days: Excludes weekends and public holidays.

Presence %: Calculated as total present days over total working days.

WFH %: Calculated as WFH days over total present days to see preference.

Sick Leave %: Calculated to monitor wellness trends.

Dynamic Columns: Added columns for Month and Day of Week to enable trend filtering.

4. Dashboard Design & Visualization
KPI Cards: High-level summary of Presence, WFH, and SL percentages.

Trend Charts: Area charts showing patterns over time, helping to spot seasonal declines in presence.

Attendance Matrix: A granular table showing individual employee status (Present, Sick Leave, WFH, Half-Day) for every day of the month.

Day-of-Week Analysis: Bar charts highlighting attendance patterns by day (e.g., identifying Fridays as high WFH days).

💡 Key Insights
Presence Patterns: Tuesdays usually see the highest in-office presence, while Fridays see the highest WFH requests.

Trend Analysis: Identified a gradual decline in presence as certain months approach, suggesting a need for better resource planning during those periods.

Hybrid Planning: Data provides a baseline for "hot-desking" or reducing office rental costs by alternating team office days.
