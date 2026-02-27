Below is your **clean, structured, recruiter-ready README.md**.
You can copy and paste this directly into your GitHub repository.

---

# B2B Travel Analytics Dashboard

Excel-Based Business Intelligence Project | 10,000 Records | KPI + RFM + Root Cause Analysis

---

## 1. Project Overview

This project simulates a B2B travel platform dataset (10,000 records) and demonstrates how a Business Analyst converts raw transactional data into structured, decision-ready insights.

The dashboard evaluates:

* Revenue performance (GMV)
* Cancellation behavior
* Agent segmentation using RFM framework
* Platform-level revenue opportunity
* Regional root cause analysis (Dubai case)

The objective is to replicate a real-world business performance review environment.

---

## 2. Business Problem

The travel platform aims to understand:

* Why cancellation rates are high (37%)
* Which platform drives the most revenue
* Which agents contribute the highest business value
* Why Dubai bookings declined Month-over-Month
* Where operational intervention is required

This project answers these questions using structured KPI modeling and segmentation logic.

---

## 3. Dataset & File Structure

### Tab 1 — Data_Clean

Contains 10,000 rows of transformed and engineered data.

**Key Columns:**

* Agent_ID
* Agent_Tier (Gold / Silver / Bronze)
* Platform (App / Website / Offline)
* Product_Type (Hotel / Package / Flight)
* Region
* Arrival_Date
* Total_Revenue

Column U includes exact Excel formulas used for engineered fields for interview explanation.

---

### Tab 2 — Pivot_Calculations

Contains structured analytical sections:

#### KPI Summary

* Total GMV
* Cancellation Rate: 37%
* Active Agents: 315
* Average ADR
* Average Lead Time

#### Revenue by Platform

Revenue split across:

* App
* Website
* Offline

Identifies offline dependency and digital migration opportunity.

#### Bookings by Product Type

* Hotel: 87%
* Package: 13%
* Flight: <1%

Highlights revenue concentration risk.

#### Agent RFM Table

Top 30 agents segmented into:

* Champion
* At-Risk
* New
* Loyal
* Occasional

Each segment includes recommended action strategy.

#### Formula Reference

Agent_Tier

```
=IF(C2>=1000,"Gold",IF(C2>=200,"Silver","Bronze"))
```

Platform

```
=CHOOSE(RANDBETWEEN(1,3),"App","Website","Offline")
```

Product_Type

```
=IF(AND(J2=0,K2=0),"Flight",
IF(AND(H2="Resort Hotel",(J2+K2)>=5),"Package","Hotel"))
```

RFM Segment

```
=IF(AND(R2<=30,S2>=500,T2>=50000),"Champion",
IF(AND(R2>30,T2>=20000),"At-Risk",
IF(AND(R2<=15,S2<=50),"New",
IF(S2>=100,"Loyal","Occasional"))))
```

---

### Tab 3 — Dashboard

Executive-level performance view designed for stakeholders.

#### KPI Cards

* Total GMV
* Cancellation Rate (highlighted for risk visibility)
* Active Agents
* Total Bookings

#### Visualizations

* Revenue by Platform (Bar Chart)
* Product Market Share (Pie Chart)
* Monthly Trend (Total vs Dubai)
* Cancellation Rate by Agent Tier

#### RFM Summary

Segment-level performance view highlighting high-value and risk agents.

#### Top 10 Champion Agents

Ranked by revenue contribution with retention recommendations.

#### Dubai Root Cause Analysis Framework

6-step structured diagnostic approach.

---

## 4. Key Insights

* Cancellation rate is significantly high (37%) and requires operational review.
* Revenue is heavily concentrated in Hotels (87%).
* Offline channel remains strong, indicating App growth opportunity.
* RFM segmentation identifies high-value Champions and revenue-risk At-Risk agents.
* Dubai bookings declined 20% Month-over-Month.
* App bookings dropped sharply while Offline remained stable, indicating a potential App-specific issue.

---

## 5. Tools Used

* Microsoft Excel
* Pivot Tables
* Logical Functions (IF, AND, CHOOSE)
* Conditional Formatting
* KPI Dashboard Design
* RFM Segmentation Framework

---

## 6. Business Impact

If implemented in a real business environment, this analysis could enable:

* 15–20% GMV recovery through App optimization
* Improved retention of high-value agents
* Reduction in cancellations
* Stronger channel performance strategy

---

## 7. Author
# Mohit Vishwakarma
# MBA [ Business Analytics ]

---

If you want next, I can prepare a **clean GitHub folder structure section** to place below this README so your entire repo looks enterprise-level structured.
