# Predictive accident Mapping 

🚦 Predictive Accident Mapping and Visualization System
This project delivers a comprehensive data-driven solution for analyzing road traffic accidents across three major U.S. cities — New York City, Chicago, and Austin. By leveraging ETL pipelines, data profiling, dimensional modeling, SQL aggregation, and modern business intelligence tools, we provide actionable insights into accident patterns, contributing factors, and public safety trends.

The primary goal is to support urban planners, city officials, and traffic management authorities in identifying high-risk zones, optimizing policy interventions, and improving public safety through data-backed decisions.

📌 Objective
To develop a cross-city accident analysis and visualization system that enables:

✅ Identification of high-risk accident zones

✅ Analysis of injury vs. fatality ratios

✅ Understanding of vehicle and pedestrian crash impact

✅ Seasonal, hourly, and daily crash trend analysis

✅ Data consolidation through dimensional modeling and SQL queries

✅ ETL workflows for consistent data transformation across cities

✅ Delivery of intuitive dashboards using Power BI and Tableau

🧠 Technologies & Tools Used
Category	Technologies Used
ETL	Talend Open Studio for data extraction, transformation, and loading
Data Analysis	Python (pandas, ydata_profiling)
Data Modeling	ER Studio, Star Schema Design
Querying	SQL (PostgreSQL-style syntax)
Visualization	Power BI, Tableau
Reporting & Docs	Excel, PDF Reports, Statistical Profiling

📊 Analytical Workflow
1. ETL Pipeline (with Talend)
Used Talend Open Studio to design ETL workflows that:

Extracted raw datasets from NYC, Chicago, and Austin

Performed schema alignment and field renaming

Handled null values, standardization of date/time formats

Consolidated and transformed data into structured staging tables

Ensured consistency across datasets with different structures

Talend's drag-and-drop interface allowed rapid development and reusability of jobs for future data refresh cycles.

2. Data Profiling
Using Python and ydata_profiling, each dataset was statistically profiled to identify:

Missing data patterns

Value distributions

Anomalies and outliers

Field uniqueness and correlation matrices

This step guided preprocessing decisions in both Talend and SQL stages.

3. Dimensional Modeling
A star schema was created for fast aggregation and drill-down analysis:

Fact Tables:
fact_crash: Master crash records with location, date, injuries, and deaths

fact_vehicle: Vehicle involvement per crash

fact_contribution: Primary and secondary crash causes

Dimension Tables:
date_dim, time_dim, location_dim, dim_vehicle, scd_contribution_dim

The schema was modeled in ER Studio and validated for referential integrity, enabling accurate OLAP-style querying and visual filtering.

4. SQL Query Design
City-specific SQL queries were written to:

Identify top crash ZIP codes and intersections

Detect time-based trends (by hour, day, month, season)

Isolate pedestrian vs. vehicle-related fatalities

Classify crashes by contributing factors

Segment injury-only vs. fatal crashes

Filter by number of vehicles, severity, borough/area

Queries were used to populate dashboards and are included in Final SQL Query.pdf.

5. Insight Generation
Compared injury and fatality trends across all three cities

Analyzed the impact of time-of-day, vehicle type, and road conditions

Revealed differences in pedestrian vs. motorist risks

Identified patterns in crash causes and behavioral factors

Enabled location-based intervention recommendations via ZIP code analysis

📈 Dashboards & Visualizations
🟡 Power BI Dashboard
Multi-tab layout for each city

Interactive slicers for timeframe, vehicle type, and borough

KPI cards, stacked bar charts, and ZIP-level maps

Heatmaps for pedestrian fatalities

🔵 Tableau Dashboard
Comparative views between cities

ZIP code heatmaps for crash hotspots

Filters by daypart, weekday, vehicle class, and crash cause

Both dashboards were built with clarity, responsiveness, and executive usability in mind.

📍 Key Insights Discovered
Insight	Impact
🚗 Brooklyn and Queens had the highest accident counts in NYC	Aimed at optimizing traffic enforcement zones
🕒 Accidents peaked during commute hours and weekends	Informs EMS and law enforcement resource planning
❄️ Austin showed spikes during Q1 (winter months)	Likely due to unpreparedness for icy road conditions
💥 NYC pedestrian fatalities were disproportionately high	Supports sidewalk and signal redesign
🚦 "Failure to yield" was the most cited contributing factor	Highlights behavioral re-education need for drivers

📚 Deliverables
NYC Analysis Report.pdf, Chicago Analysis Report.pdf, Austin Analysis Report.pdf

Final SQL Query.pdf — with all analytical queries

FINAL_DIMMODEL.pdf — dimensional ER schema

PowerBI_Vizualization.pbix — Power BI dashboard

Visualizations - Tableau -Final.twb — Tableau workbook

Work_Flow_Diagram.pdf — Complete pipeline architecture

PowerBI Visualizations Document.pdf — UI breakdown
