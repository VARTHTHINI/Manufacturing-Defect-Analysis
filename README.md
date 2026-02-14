Excel Case study - Analysis of manufacturing defects
Overview:
This case study is about analysing the data of manufacturing quality to detect the defect patterns, machines and performance of operators, shift wise issues, monthly trends and critical defect spike days. This analysis is done using Microsoft Excel with formulas, pivot tables and charts.

Dataset Description:
The handled dataset is about 500 production records with the below given columns:
•	Production Date 		– Production date	
•	Shift (A/B/C)			- Production shift
•	Machine ID			- Machine used for production
•	Units Produced		- Total units produced
•	Defective Units		-Number of defective units per production
•	Operator Name		-Operator handling the machine
•	Defect as percentage		-Calculated field

Data Preparation:
Defect as percentage field calculation:
A new column was created to calculate the defect percentage per record. 
Defect % = (defective Units/ Units produced) * 100
This ensures low level defect measurement before aggregation.

Analysis & Insights:
Q1. Defect Percentage per Record
•	Calculated defect percentage for each production record.
•	Values ranged approximately between 0.7% and 10%, indicating realistic manufacturing variation.

Q2. Machines with Defect Rate Above 5%
Method: Pivot Table
•	Rows: Machine ID
•	Values: Average of Defect Percentage
•	Filter: Average > 5%
Insight:
Machine M006 showed an average defect rate above 5%, indicating potential maintenance or calibration issues.
Q3. Shift with Highest Average Defect Rate
Method: Pivot Table
•	Rows: Shift (A/B/C)
•	Values: Average of Defect Percentage
Result:
Shift C had the highest average defect rate (~4.74%).
Insight:
Shift C may require closer supervision, process review, or operator training.
Q4. Top 3 Operators with Lowest Defect Percentage
Method: Pivot Table (Sorted Ascending)
•	Rows: Operator Name
•	Values: Average of Defect Percentage
Top 3 Best Performing Operators:
Operator_18 - ~3.32%
Operator_8 - ~3.69%
Operator_10 - ~3.79%
Insight:
These operators consistently maintain high-quality production standards.


Q5. Monthly Defect Trend
Method: Pivot Chart
•	Axis: Year => Month
•	Values: Average of Defect Percentage
Observations:
•	Monthly defect rates fluctuated between ~3.8% and ~5.4%.
•	Peaks observed around April-May and February 2025.
•	Defects remained relatively stable overall with periodic increases.
Q6. Critical Defect Spike Days
Definition:
In this case, a day is considered critical if Defect Percentage > 8%.
Method:
•	Daily-level Pivot Chart
•	Conditional highlighting (Red bars) for defect % > 8
Insight:
•	Critical spikes were observed during April-May, June-July, and October-December.
•	These dates indicate abnormal production behaviour and require root cause analysis.

Tools & Techniques Used:
•	Microsoft Excel
•	Formulas (IF, percentage calculations)
•	Pivot Tables & Pivot Charts
•	Sorting & Filtering
•	Data-driven threshold definition
Key Takeaways:
•	Average-based aggregation is essential when entities repeat (machines, operators).
•	Defect percentages should never be summed for analysis.
•	Clear thresholds help identify critical quality issues.
•	Pivot Tables are powerful for operational and quality analysis.
