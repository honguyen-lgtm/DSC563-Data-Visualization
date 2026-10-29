# DSC563-Data-Visualization
DSC 563 Data Visualization Projects
DSC 563 – Module 2: Tableau Visualization and Verification
Project Overview
This project recreates a Python visualization from Module 1 using Tableau and verifies that both tools produce consistent results.
The analysis focuses on community workshop attendance across four neighborhoods: East, North, South, and West.
Research Question: How does workshop attendance vary across neighborhoods, and how do utilization methods and missing attendance affect the interpretation of results?
Intended Audience: Community workshop coordinators responsible for monitoring attendance and planning seating capacity.

Data Source
The project uses a simulated community workshop attendance dataset provided for the DSC 563 course assignment.
•	Data Period: May–October 2026
•	Neighborhoods: East, North, South, and West
•	Data Type: Simulated workshop attendance and seating capacity
•	Source Attribution: DSC 563 course-provided workshop dataset
•	Reuse Restrictions: The dataset is intended for educational analysis. No additional redistribution rights are claimed; any course-specific reuse restrictions should be followed.
The data does not represent actual community workshop attendance.
Repository Files
File	Description
tableau_workshops_tidy.csv	Simulated workshop dataset used in Tableau
m01_claim_check.csv	Python-verified October attendance values
m01_after_chart.png	Improved Python attendance visualization from Module 1
DSC563_Module2_Tableau.twbx	Packaged Tableau workbook containing attendance and utilization worksheets
tableau_comparison.png	Screenshot or crosstab supporting the Python–Tableau numerical comparison
README.md	Project documentation and reproduction instructions

Note: File names should match the actual files uploaded to this repository.
Module 1: Python Visualization
In Module 1, there is an improved horizontal bar chart using Python to compare neighborhood workshop attendance.
The revised chart included numerical labels, descending sorting, and a zero baseline to make the results easier to interpret.
Personal Google Colab Notebook: https://colab.research.google.com/drive/1WKUa0ywnZdD1laNoS8qA34P2djBsRX0r
How to Run the Notebook
1.	Open the personal Module 1 notebook in Google Colab.
2.	Select Runtime → Run all.
3.	Review the original and improved attendance charts.
4.	Locate the October 2026 attendance results.
5.	Review the graduate analysis comparing missing-attendance assumptions.
6.	Download or inspect m01_after_chart.png and m01_claim_check.csv.
Module 2: Tableau Visualization
I recreated the improved Python attendance chart in Tableau using the same data, month, measure, and aggregation.
Tableau Chart Settings
•	Selected Month: October 2026
•	Dimension: Neighborhood
•	Measure: Attendance Visits
•	Aggregation: SUM
•	Units: Seat visits
•	Chart Type: Horizontal bar chart
•	Sorting: Descending attendance
•	Design: Numerical labels and zero baseline
Tableau Workbook: DSC563_Module2_Tableau.twbx
To open the workbook, download the .twbx file and open it in a compatible version of Tableau Desktop or Tableau Public.
Python vs. Tableau Verification
I compared the October 2026 attendance values to verify that Tableau reproduced the Python results.
Neighborhood	Python	Tableau	Difference
East	94	94	0
North	90	90	0
West	90	90	0
South	82	82	0
All four neighborhoods had a difference of zero, confirming that Tableau matched the Python results.
Verification Evidence:
•	Python results: m01_claim_check.csv
•	Tableau results: October attendance worksheet in the packaged workbook
•	Supporting screenshot: tableau_comparison.png
DSC 563 Graduate Analysis
Module 1: Missing Attendance Treatment
The Module 1 Python analysis examined how missing attendance affects utilization calculations.
East had attendance recorded for five out of six months (83.3% coverage), while the other neighborhoods had complete records.
Two missing-data assumptions were compared:
•	Observed Months Only: Calculates utilization using months with recorded attendance.
•	Missing as Zero: Assumes zero attendance for the missing month while retaining its available seating capacity.
For East, utilization decreased from 73.57% to 62.42%, a difference of 11.15 percentage points, when the missing month was treated as zero.
This demonstrates how missing-data assumptions can influence the interpretation of workshop utilization.
Evidence Location: Graduate missing-attendance analysis in the personal Module 1 Google Colab notebook.
Module 2: Tableau Utilization Comparison
In Module 2, I compared two methods for calculating workshop utilization.
•	Mean Monthly Utilization: Averages the monthly utilization percentages across observed months.
•	Capacity-Weighted Observed-Month Utilization: Divides total recorded attendance by total available seating capacity across months with attendance records.
Neighborhood	Mean Monthly	Capacity-Weighted	Observed Months
East	73.4%	73.6%	5/6
North	73.1%	73.2%	6/6
South	79.9%	80.0%	6/6
West	59.2%	59.4%	6/6
South had the highest utilization at approximately 80%, while West had the lowest at approximately 59%.
Both methods produced similar percentages and the same neighborhood rankings.
Evidence Location: Utilization comparison and Monthly Coverage worksheets in the Tableau workbook.
Consequential Assumption
One important assumption concern how missing attendance is treated.
A missing attendance record does not necessarily mean that no participants attended.
When East's missing month was treated as zero, its calculated utilization decreased by 11.15 percentage points.
This illustrates why missing data should be identified and documented before drawing conclusions.
Analytical Value
Comparing utilization methods helps determine whether differences in available seating capacity meaningfully affect neighborhood comparisons.
Both methods produced the same rankings, suggesting that the choice between these two utilization calculations had little effect on the overall comparison.
The missing attendance analysis also highlights the importance of checking data completeness.
Limitations
The dataset is simulated and does not represent actual community workshop attendance.
Additionally, East had one missing month of attendance data. The analysis demonstrates how different assumptions affect utilization but cannot establish the actual attendance for that missing month.
How to Verify the Project
1.	Open the personal Module 1 Google Colab notebook and run all cells.
2.	Locate m01_claim_check.csv and review the Python attendance results.
3.	Download and open the Tableau packaged workbook.
4.	Open the October 2026 attendance worksheet.
5.	Verify that the Tableau values match Python for all four neighborhoods.
6.	Review the utilization comparison worksheet to compare mean monthly and capacity-weighted utilization.
7.	Open the Monthly Coverage worksheet to confirm East has 5/6 observed months and the remaining neighborhoods have 6/6.
8.	Review the missing-attendance sensitivity analysis in Module 1 notebook.
Tools Used
•	Python (Google Colab)
•	Tableau
•	GitHub
Conclusion
The Tableau visualization successfully reproduced the October 2026 attendance results from Python, with zero differences across all four neighborhoods.
The Utilization comparisons demonstrated that mean monthly and capacity-weighted utilization produced similar results, while missing-attendance assumptions could substantially change an individual neighborhood's utilization.
Together, these findings highlight the importance of accurate calculations, data completeness, and clear visual communication.

