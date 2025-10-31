&nbsp;Healthcare Waitlist Analytics Dashboard

Power BI | Inpatient, Outpatient \& Day Case | Multi-Year Analysis

&nbsp;Overview



This project delivers a comprehensive Power BI dashboard that analyzes hospital waitlist data across Inpatient, Outpatient, and Day Case categories from 2018–2021.

The report presents waitlist trends, specialty-level backlogs, time-band distributions, and demographic insights for healthcare decision-making.



&nbsp;Key Features



Latest Month vs Previous Year Waitlist KPIs

Case Type Bifurcation (Inpatient / Outpatient / Day Case)

Age Profile \& Time Band Waitlist Analysis

Specialty-Level Backlog Comparison

Multi-Year Trend Visualization

Fully Filterable Detailed View

Modern UI with drill-through capability



&nbsp;Dataset Columns Used



The dashboard is built using the following key fields:



**Column Name	Description**

Archive\_Date	Snapshot date of the waitlist record

Case\_Type	Inpatient / Outpatient / Day Case

Specialty\_Name	Detailed clinical specialty

Specialty\_Group	Grouped clinical specialty (Bones, General, ENT, Eyes, etc.)

Age\_Profile	0–15, 16–64, 65+

Time\_Bands	0–3, 3–6, 6–9, 9–12, 12–15, 15–18, 18+ Months

Day Case	Number of patients under Day Case

Inpatient	Count of inpatient waitlisted patients

Outpatient	Count of outpatient waitlisted patients

Total	Sum of all patient categories

&nbsp;Data Preparation



Performed in Power Query:



Cleaned date \& text formats



Standardized Case Types



Merged multiple years of data



Created Age Group \& Time Band mappings



Established relationship model for analysis



&nbsp;DAX Measures



Some core measures used:



Latest Wait List =

CALCULATE(

&nbsp;   SUM('Waitlist'\[Total]),

&nbsp;   LASTDATE('Waitlist'\[Archive\_Date])

)



PY Latest Wait List =

CALCULATE(

&nbsp;   SUM('Waitlist'\[Total]),

&nbsp;   SAMEPERIODLASTYEAR('Waitlist'\[Archive\_Date])

)



Avg Wait List =

AVERAGE('Waitlist'\[Total])



Total by Specialty Group =

SUM('Waitlist'\[Total])



&nbsp;Dashboard Pages

1️⃣ Summary Dashboard


<img width="1379" height="767" alt="Screenshot 2025-10-31 132027" src="https://github.com/user-attachments/assets/c2735f9f-ffd6-4ffc-b570-19e16e427351" />

Latest Month Waitlist



PY Latest Month Waitlist



Waitlist Bifurcation by Case Type



Age \& Time Band Waitlist Comparison



Specialty-wise Avg/Median Waitlist



Multi-year Monthly Trend for IP/DC vs OP



2️⃣ Detailed View



A hierarchical drill-down matrix:



Archive\_Date  

&nbsp;  └── Specialty\_Name  

&nbsp;        └── Age\_Profile  

&nbsp;              └── Time\_Bands  





Columns include: Day Case | Inpatient | Outpatient | Total



Fully filterable by:

&nbsp;Case\_Type

&nbsp;Specialty\_Name

&nbsp;Age\_Profile

&nbsp;Time\_Bands

&nbsp;Date Range



3️⃣ Specialty Group Analysis



Total Waitlist by Specialty Group



Ranked bar chart (Bones, General, ENT, Eyes, Skin, etc.)



Highlights highest-pressure clinical areas



&nbsp;Insights Highlight



Outpatient demand is the largest contributor to total waitlist.



Significant backlog growth visible in 2020–2021.



Specialty groups like Bones, General, ENT, Eyes show highest totals.



Time band 18+ Months indicates long-term pressure areas.



Day Case remains stable compared to rising Outpatient backlog.



&nbsp;Tools \& Technologies



Power BI Desktop



DAX



Power Query (M Language)



CSV structured data



&nbsp;How to Use



Clone or download this repository.



Open the .pbix file using Power BI Desktop.



Interact using slicers for:



Case Type



Specialty



Age Profile



Time Band



Date Range



Explore all pages for detailed insights.



&nbsp;Future Enhancements



Predictive waitlist forecasting using ML



Benchmarking across multiple hospitals



Risk scoring for long-wait patients



Real-time waitlist updates via API



⭐ Support



If you like this dashboard, please ⭐ star the repository to support the project!



