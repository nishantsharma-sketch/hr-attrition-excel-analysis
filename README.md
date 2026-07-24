# Employee Attrition Analysis

An interactive HR analytics dashboard built in Excel, analyzing employee attrition patterns for a workforce of 1,470 employees using Power Query, Power Pivot, and DAX.

## Overview
This project explores why employees leave the company and which factors are most associated with attrition — department, job role, income level, overtime, tenure, and more — using a real IBM HR dataset. The end deliverable is a dynamic, slicer-driven dashboard built natively in Excel.

## Dataset
IBM HR Analytics Employee Attrition dataset (Kaggle) — 1,470 employees, 35 original attributes covering demographics, compensation, job role, satisfaction scores, and tenure.

## Process

**Data Cleaning (Power Query)**
Imported the raw dataset and cleaned it before modeling: verified data types, removed constant and low-value columns (identifiers and near-constant fields like EmployeeCount, Over18, DailyRate, HourlyRate, MonthlyRate, PerformanceRating, EducationField, TrainingTimesLastYear), and confirmed there were no missing values across the remaining fields.

**Data Modeling (Power Pivot)**
Loaded the cleaned table into the Data Model and added calculated columns to support grouped analysis: SalaryStatus (income banded into Low/Medium/High), PromotionGap (years since last promotion, banded), and AgeBand (age grouped into ranges).

**Measures (DAX)**
Built a set of core measures on top of the model: Total Employees, Attrition Count, Attrition Rate, Overtime Attrition Rate, Low Income Attrition Rate, Average Monthly Income, Average Monthly Income (Leavers), Average Years at Company, and Average Years Since Promotion (Leavers).

## Dashboard
The first dashboard page, "Employee Attrition Overview," brings together four KPI cards (Attrition Rate, Total Employees, Average Monthly Income, Average Years at Company), slicers for Department, OverTime, Age Band, Business Travel, and Job Satisfaction, and two charts breaking down attrition rate by Department and by Job Role.

A second page, "Employee Attrition — Key Drivers," is in progress and will add further breakdowns by overtime status, salary band, age group, promotion gap, marital status, and work-life balance rating.

## Key Insights
The overall attrition rate across the workforce is 16.12%. Sales has the highest attrition of any department at 20.63%, followed by HR at 19.05%, while Research & Development is lowest at 13.84%. By job role, Sales Representative stands out sharply at 39.76% attrition — more than double any other role — followed by Laboratory Technician (23.94%) and HR (23.08%), while Research Director (2.50%) and Manager (4.90%) are the most stable roles.

## Recommendation
A full business recommendation is being finalized alongside the second dashboard page — see `recommendation.md`.

## Tools
Excel, Power Query, Power Pivot, DAX

## Repository Structure
```
├── Attrition_sheet.xlsx
├── WA_Fn-UseC_-HR-Employee-Attrition.csv
├── README.md
└── recommendation.md
```
