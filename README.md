# B2B-Travel-Performance-Dashboared---TravClan-Case-Study-
## B2B Travel Analytics Dashboard

#### Excel-Based Business Intelligence Project | 10,000 Records | KPI + RFM + Root Cause Analysis

1. Project Overview

This project simulates a B2B travel platform dataset (10,000 records) and demonstrates how a Business Analyst converts raw transactional data into decision-ready insights.

The dashboard focuses on:

Revenue performance (GMV)

Cancellation behavior

Agent segmentation (RFM)

Platform-level opportunity analysis

Regional root cause investigation (Dubai case)

The goal is to replicate a real-world business review scenario typically discussed in analytics or strategy interviews.

2. Business Problem

A travel platform wants to understand:

Why cancellation rates are high (37%)

Which platform is driving (or losing) revenue

Which agents are most valuable

Why Dubai bookings dropped Month-over-Month

Where operational intervention is required

This Excel project answers these questions using structured KPI analysis and segmentation logic.

3. File Structure
Tab 1 — Data_Clean

Contains 10,000 rows of transformed and engineered data.

Key Columns:

Agent_ID

Agent_Tier (Gold / Silver / Bronze)

Platform (App / Website / Offline)

Product_Type (Hotel / Package / Flight)

Region

Arrival_Date

Total_Revenue

Column U contains exact Excel formulas used for engineered columns — helpful for explaining logic during interviews.

Tab 2 — Pivot_Calculations

Contains structured analysis sections:

KPI Summary

Total GMV

Cancellation Rate: 37%

Active Agents: 315

Average ADR

Average Lead Time

Revenue by Platform

Shows revenue split across:

App

Website

Offline

Identifies offline dependency and digital migration opportunity.

Bookings by Product Type

Hotel: 87%

Package: 13%

Flight: <1%

Highlights core revenue concentration.

Agent RFM Table

Top 30 agents segmented into:

Champion

At-Risk

New

Loyal

Occasional

Each segment includes recommended business action.

Formula Reference Sheet

Key business logic used:

Agent_Tier

=IF(C2>=1000,"Gold",IF(C2>=200,"Silver","Bronze"))

Platform

=CHOOSE(RANDBETWEEN(1,3),"App","Website","Offline")

Product_Type

=IF(AND(J2=0,K2=0),"Flight",
   IF(AND(H2="Resort Hotel",(J2+K2)>=5),"Package","Hotel"))

RFM Segment

=IF(AND(R2<=30,S2>=500,T2>=50000),"Champion",
   IF(AND(R2>30,T2>=20000),"At-Risk",
   IF(AND(R2<=15,S2<=50),"New",
   IF(S2>=100,"Loyal","Occasional"))))
Tab 3 — Dashboard

This is the executive view shown to stakeholders.

KPI Cards

Total GMV

Cancellation Rate (Red color-coded)

Active Agents

Total Bookings

Visualizations

Revenue by Platform (Bar Chart)

Product Market Share (Pie Chart)

Monthly Trend (Total vs Dubai)

Cancellation Rate by Agent Tier

RFM Summary Table

Color-coded segmentation:

Champions

At-Risk

New

Top 10 Champion Agents

Ranked by revenue contribution with recommended retention actions.

Dubai RCA Framework

6-step structured root cause analysis table.

4. Key Insights

Cancellation rate is significantly high (37%) → Requires operational review.

Revenue is highly concentrated in Hotels (87%).

Offline channel still contributes strongly → App conversion opportunity exists.

RFM analysis identifies high-value Champions and revenue-risk At-Risk agents.

Dubai bookings declined 20% Month-over-Month.

App bookings dropped sharply while Offline remained stable → Indicates possible App-specific issue.

5. Dubai Root Cause Analysis (Interview Explanation)

When asked about Dubai performance:

“I filtered the Pivot Table by Region = Dubai and compared Month-over-Month performance. Total bookings fell 20%. When I cross-tabbed by Platform, Offline bookings remained flat but App bookings dropped sharply. This suggests a potential technical issue in the App booking flow for Dubai routes rather than a demand problem. My recommendation would be a QA audit of the Dubai App funnel followed by a temporary agent incentive campaign.”

6. Tools Used

Microsoft Excel

Pivot Tables

Conditional Formatting

Logical Formulas

KPI Dashboard Layout

RFM Segmentation

7. Business Impact

If implemented in a real environment, this analysis would enable:

15–20% potential GMV recovery through App optimization

Improved retention of high-value agents

Reduction in cancellations

Better channel strategy planning

8. How to Use

Open the Excel file.

Review Data_Clean to understand engineered columns.

Explore Pivot_Calculations for analytical breakdown.

Use Dashboard tab for presentation.

Practice explaining Dubai RCA using structured reasoning.

9. Author

Business Analytics Project
Focused on practical, interview-ready decision analysis using Excel.
