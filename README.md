# Employee Attrition Analysis

A rapid, end-to-end HR analytics dashboard built natively in Excel — from raw CSV to a fully interactive, cross-filtered two-page BI report — using Power Query, Power Pivot, and DAX. Built as a focused, agile analysis: a lean data model and a tight set of measures, iterated quickly into a working dashboard rather than over-engineered from the start.

## Overview
This project investigates why employees leave the company and which factors are most associated with attrition — department, job role, income level, overtime, tenure, age, marital status, and work-life balance — using a real IBM HR dataset. The result is a two-page, slicer-driven dashboard: one page for the headline picture, one for digging into drivers.

## Dataset
IBM HR Analytics Employee Attrition dataset (Kaggle) — 1,470 employees, 35 original attributes covering demographics, compensation, job role, satisfaction scores, and tenure.

## Approach
Built in a single, focused working session, prioritizing speed without cutting corners on the data model:
1. Clean and shape the data (Power Query)
2. Build a lean Data Model with just the calculated fields needed (Power Pivot)
3. Layer in measures (DAX)
4. Assemble two dashboard pages, cross-filtered by shared slicers

## Process

**Data Cleaning (Power Query)**
Imported the raw dataset and cleaned it before modeling: verified data types, removed constant and low-value columns (identifiers and near-constant fields like EmployeeCount, Over18, DailyRate, HourlyRate, MonthlyRate, PerformanceRating, EducationField, TrainingTimesLastYear), and confirmed there were no missing values across the remaining fields.

**Data Modeling (Power Pivot)**
Loaded the cleaned table into the Data Model and added calculated columns to support grouped analysis: SalaryStatus (income banded into Low/Medium/High), PromotionGap (years since last promotion, banded), and AgeBand (age grouped into ranges).

**Measures (DAX)**
Built a set of core measures on top of the model: Total Employees, Attrition Count, Attrition Rate, Overtime Attrition Rate, Low Income Attrition Rate, Average Monthly Income, Average Monthly Income (Leavers), Average Years at Company, and Average Years Since Promotion (Leavers).

## Key Insights
- Overall attrition rate across the workforce: **16%**
- **By department:** Sales highest (21%), HR (19%), R&D lowest (14%)
- **By job role:** Sales Representative stands out sharply at **40%** attrition — more than double any other role — followed by Laboratory Technician (24%) and HR (23%); Research Director (3%) and Manager (5%) are the most stable
- **Overtime is the single biggest driver:** employees working overtime attrit at **31%** vs. just **10%** for those who don't
- **Under-30 employees** attrit at **28%**, roughly double every older age band
- **Single employees** attrit at **26%** vs. 12% for married employees
- **Low-income employees** attrit at **25%** vs. 9% for high earners
- Employees with the **lowest work-life balance rating (1)** attrit at **31%**, nearly double the rate at rating 4 (18%)


## Tools
Microsoft Excel, Power Query, Power Pivot, DAX

## Repository Structure
```
├── Attrition_sheet.xlsx
├── README.md
├── recommendation.md
└── deck/
    ├── page1_overview.png
    └── page2_key_drivers.png
```
