Healthcare Waitlist Analytics Dashboard
Power BI | Inpatient, Outpatient & Day Case | Multi-Year Analysis
📌Overview

This project delivers a comprehensive Power BI dashboard that analyzes hospital waitlist data across Inpatient, Outpatient, and Day Case categories from 2018–2021.

The report presents:

Waitlist trends

Specialty-level backlogs

Time-band distributions

Demographic insights

designed to support healthcare decision-making.

✨ Key Features

Latest Month vs Previous Year Waitlist KPIs

Case Type Bifurcation (Inpatient / Outpatient / Day Case)

Age Profile & Time Band Waitlist Analysis

Specialty-Level Backlog Comparison

Multi-Year Trend Visualizations

Fully Filterable Detailed View

Modern UI with drill-through capability

🗂 Dataset Columns Used
Column Name	Description
Archive_Date	Snapshot date of the waitlist record
Case_Type	Inpatient / Outpatient / Day Case
Specialty_Name	Detailed clinical specialty
Specialty_Group	Grouped clinical specialty (Bones, General, ENT, etc.)
Age_Profile	0–15, 16–64, 65+
Time_Bands	0–3, 3–6, 6–9, 9–12, 12–15, 15–18, 18+ Months
Day Case	Count of Day Case patients
Inpatient	Count of Inpatient patients
Outpatient	Count of Outpatient patients
Total	Combined patient count
🧹 Data Preparation (Power Query)

Cleaned date & text formats

Standardized case types

Merged multi-year data

Created Age Group & Time Band mappings

Established relationship model

📊 DAX Measures

Latest Wait List

Latest Wait List =
CALCULATE(
    SUM('Waitlist'[Total]),
    LASTDATE('Waitlist'[Archive_Date])
)


PY Latest Wait List

PY Latest Wait List =
CALCULATE(
    SUM('Waitlist'[Total]),
    SAMEPERIODLASTYEAR('Waitlist'[Archive_Date])
)


Avg Wait List

Avg Wait List = AVERAGE('Waitlist'[Total])


Total by Specialty Group

Total by Specialty Group = SUM('Waitlist'[Total])

📄 Dashboard Pages
1️⃣ Summary Dashboard
<img width="1379" height="767" alt="Screenshot 2025-10-31 132027" src="https://github.com/user-attachments/assets/c2735f9f-ffd6-4ffc-b570-19e16e427351" />
Includes:

Latest vs PY Waitlist KPIs

Case Type Split

Age & Time Band Distribution

Specialty-wise Avg/Median Waitlist

Multi-year Trend (IP/DC vs OP)

2️⃣ Detailed View
<img width="1366" height="757" alt="Screenshot 2025-10-31 132059" src="https://github.com/user-attachments/assets/609df4b4-d9cb-4a7e-aa13-66b5a040c624" />

Hierarchical Drill-Down:

Archive_Date

Specialty_Name

Age_Profile

Time_Bands

Columns:

Day Case | Inpatient | Outpatient | Total

Fully filterable by:

Case Type

Specialty

Age Profile

Time Band

Date Range

3️⃣ Drill-Down Page
<img width="489" height="789" alt="Screenshot 2025-10-31 132124" src="https://github.com/user-attachments/assets/00bfe780-00b5-489a-a75d-b8424187be3e" />

Specialty Group Analysis

Total Waitlist by Specialty Group

Ranked bar chart (Bones, General, ENT, Eyes, etc.)

Highlights highest-pressure specialties

🔍 Insights Highlight

Outpatient demand is the largest contributor to total waitlist.

Backlog rose significantly during 2020–2021.

Specialty groups like Bones, General, ENT, Eyes show highest totals.

18+ Month Time Band reveals long-term backlog pressure.

Day Case remains stable compared to rising Outpatient demand.

🛠 Tools & Technologies

Power BI Desktop

DAX

Power Query (M)

CSV data sources

🚀 How to Use

Clone or download the repository.

Open the .pbix file in Power BI Desktop.

Use slicers to interact with:

Case Type

Specialty

Age Profile

Time Band

Date Range

Explore all pages for insights.

📈 Future Enhancements

Predictive waitlist forecasting (ML)

Multi-hospital benchmarking

Risk scoring for long-wait patients

Real-time waitlist updates via API

⭐ Support

If you found this dashboard useful, please ⭐ star the repository!



