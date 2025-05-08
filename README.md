# Call-Centre-analysis
Call Center Performance Dashboard — Excel Power Pivot &amp; DAX Project Overview: Developed an interactive and dynamic Excel dashboard to monitor and analyze call center performance using advanced Excel capabilities such as Power Pivot, DAX, Pivot Tables, Slicers, and Conditional
📊 Project Objective:
Build a dynamic Call Center Dashboard in Excel that provides:

Overall performance metrics

Representative-level KPIs

Interactive filters (slicers)

Visual enhancements (conditional formatting, charts, images)

🗃️ Dataset Structure:
1. Calls Table
Column Name	Description
Call Number	Unique ID of the call
Customer ID	Identifier of customer
Duration	Call length in minutes
Representative	Agent name
Date	Date of call
Purchase Amount	Sales amount from the call
Satisfaction Rating	Rating (0–5), also a rounded version
Financial Year	Derived using formula
Day of the Week	Derived using formula
Duration Bucketing	Derived (e.g., short, medium, long call)

2. Customers Table
Column Name	Description
Customer ID	Unique identifier
Gender	M / F
Age	Age in years
City	Columbus, etc.

🛠️ Step-by-Step Implementation:
✅ 1. Theme and Fonts Setup
Use Slipstream theme under Page Layout → Colors.

Use Aptos Extra Bold and Aptos fonts (or alternatives).

Helps keep styling consistent across all visuals and elements.

✅ 2. Add Data to Data Model
When inserting Pivot Table → check "Add this data to the Data Model".

Enables relationships, Power Pivot, and DAX.

✅ 3. Create Relationships
Go to: Analyze → Relationships → New.

Join:

calls[Customer ID] ↔ customers[Customer ID]

✅ 4. Define DAX Measures
Define key metrics using Power Pivot → Measures:

Measure Name	Formula (DAX)	Notes
Call Count	=COUNTROWS(calls)	Total calls
Total Amount	=SUM(calls[Purchase Amount])	Total revenue
Total Duration	=SUM(calls[Duration])	Sum of call durations
Average Rating	=AVERAGE(calls[Satisfaction Rating])	Mean customer rating
5-Star Calls	=CALCULATE([Call Count], calls[Rating Rounded] = 5)	Number of happy callers

Apply formatting as:

Currency (for amounts)

Whole number with separator (for counts)

✅ 5. Create Pivot Tables
Summary Pivot: Uses all DAX measures, no filters.

Rep Pivot: Same DAX metrics filtered by Representative.

✅ 6. Add Interactive Slicers
Insert → Slicer → Choose "Representative"

Link to Rep Pivot only

Allows dynamic selection of one or more agents

✅ 7. Visual Elements
Use stock images for representatives (from Excel’s online images)

Add:

Bar charts for call counts by region or rep

Conditional formatting in tables

Color-coded KPI cards

🧠 Why This Project Is Important (From a Data Science Perspective):
Data Integration: Merging multiple tables using primary keys (joins).

DAX Logic: Builds critical thinking around measures and filter context.

Data Modeling: Introduces normalization and star schema-like structures.

Dashboarding Skills: Good for portfolio and client reporting scenarios.

Interactive UX: Business users love slicers & personalized views
