# Financial-Loan-Default-Report
## Problem Statement

Financial institutions and lending agencies require comprehensive visibility into borrower demographics, loan purposes, and default risks to optimize their lending strategies and mitigate financial loss. This dashboard provides a deep dive into applicant financial profiles, tracking average income, median loan amounts, and credit score impacts across different demographics.

By analyzing historical default rates and Year-Over-Year (YOY) changes, stakeholders can identify high-risk applicant profiles. For instance, understanding that unemployed individuals have a higher default rate (3.4%) compared to full-time employees (2.4%) allows the institution to adjust credit requirements. Tracking metrics such as loan amounts by purpose—where Home loans lead at 6545M—enables better allocation of funds and tailored financial product offerings.

## Steps Followed:

**Step 1 :** Downloaded, installed, & configured the Standard Mode Gateway to connect on-premise data sources.

**Step 2 :** Downloaded & installed Microsoft SQL Server, and subsequently imported the raw loan dataset into SQL Server.

**Step 3 :** Created a Dataflow using Power BI Service.

**Step 4 :** Imported data into Power BI Desktop directly from the established dataflow.

**Step 5 :** Defined column structures, added dataset descriptions, and performed Data Types & Profiling in Power Query Editor.

**Step 6 :** In the report view, renamed the initial canvas and inserted shapes on Page 1 to establish the UI layout.

**Step 7 :** Created a calculated measure for "Loan Amount by Purpose".

DAX Used: SUMX, FILTER, NOT, ISBLANK

**Step 8 :** Created calculated measures for Income and Default rates:

"Average Income by Employment Type" (DAX Used: CALCULATE, AVERAGE, ALLEXCEPT)

"Default Rate by Employment type" (DAX Used: ALL, ALLEXCEPT, COUNTROWS, DIVIDE, FILTER)

**Step 9 :** Created measures for Demographic analyses:

"Average Loan by Age Groups" (DAX Used: AVERAGE, AVERAGEX, VALUES)

"Default Rate by Year" (DAX Used: CALCULATE, COUNTROWS, ALLEXCEPT, FILTER, DIVIDE)

Validated data for these newly created metrics.

**Step 10 :** Calculated and validated medians, specifically "Median Loan Amount by credit score category", utilizing the MEDIANX DAX Function.

**Step 11 :** Added various visual charts to the report design area:

A Donut Chart to show Average Loan Amount by Age Group & Marital Status (followed by data validation).

Clustered Column Charts to represent Total Loan (Adults) by credit categories and Total Loan (Middle Age Adults) by Mortgage/Dependents status.

Number of Loans by education type visual.

**Step 12 :** Created Year-Over-Year (YOY) DAX Measures for "YOY Loan amount change" and "YOY Default Loans change". Line charts were added to represent these YOY metrics.

**Step 13 :** Added a visual for "YTD Loan amount by credit score bins & marital status".

**Step 14 :** Added a Decomposition Tree visual to break down the sum of loan amounts by Income Bracket and Employment Type.

DAX Used: SWITCH Function

**Step 15 :** Configured automated data refreshes by setting up Schedule Refresh and Incremental Refresh for the Dataflow.

**Step 16 :** The report was published to Power BI Service, automated refreshes were scheduled for the report was shared with stakeholders.


## Insights

A comprehensive report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

**[1]** Loan Amount By Purpose
Home = 6545M

Business = 6522M

Education = 6511M

Auto = 6501M

Other = 6498M

  Thus, the highest volume of loan amounts is allocated for Home purposes.

**[2]** Employment Type Metrics
Average Income By Employment Type:

Full-time = 82,890

Self-employed = 82,447

Part-time = 82,389

Unemployed = 82,272

Default Rate (%) By Employment Type:

Unemployed = 3.4 %

Part-time = 3.0 %

Self-employed = 2.9 %

Full-time = 2.4 %

  Thus, while full-time employees have the highest average income, unemployed individuals pose the highest default risk.

**[3]** Age Groups & Education
Average Loan Amount By Age Groups:

Adults = 127,901

Middle Age Adults = 127,459

Senior Citizens = 127,355

Teen = 126,674

Number of Loans By Education Type:

Bachelor's = 64,366

High School = 63,903

Master's = 63,541

PhD = 63,537

  Thus, maximum loan amounts are taken by Adults, and the highest number of loan applications come from individuals with a Bachelor's degree.

**[4]** Credit Score Metrics
Median Loan Amount By Credit Score Category:

Low = 128,397

Medium = 127,764

Very Low = 127,515

High = 127,149

  Thus, individuals in the "Low" credit score category hold the highest median loan amounts.

[5] Historical Default Rates
Default Rate (%) By Year:

2013 = 11.62 %

2014 = 11.50 %

2015 = 11.70 %

2016 = 11.75 %

2017 = 11.50 %

2018 = 11.60 %

Thus, the default rate peaked historically in 2016 at 11.75%.
