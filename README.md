# Optimizing-IT-Support-Team-Performance-Using-Analytics
# Cleaning + Dashboard

## 1) Problem Statement
IT support teams handle high volumes of tickets daily, but poor data quality, inefficient ticket handling, SLA breaches, and frequent ticket reopens reduce overall performance and customer satisfaction.

This project focuses on:

Cleaning and validating raw IT support ticket data

Analyzing agent productivity and SLA compliance

Identifying performance bottlenecks

Providing actionable insights to optimize IT support operations

---

## 2) Dataset Description

Data Source:Kaggle

Each record represents IT support ticket performance at the agent level, including:

Ticket priority and issue type

Tickets assigned vs resolved

Resolution time vs SLA target

Customer satisfaction ratings

Reopened tickets

Data Files:

Data/it_support_team_performance.csv → Raw data

Data/it_support_team_performance_clean.csv → Cleaned & processed data

---

## 3) KPIs / Metrics Used

The following Key Performance Indicators were calculated:

1.SLA Compliance Rate

-Percentage of tickets meeting SLA targets

2.Average Resolution Time

-Mean time taken to resolve tickets

3.Resolution Efficiency

-Tickets Resolved ÷ Tickets Assigned

4.First-Time Resolution Rate

-Percentage of tickets not reopened

5.Customer Satisfaction Score (CSAT)

-Average customer rating (1–5)

6.SLA Breach Count

-Number of tickets violating SLA conditions
---

## 4) Dashboard Details (Power BI)
  
## 5) Key Insights (From Data Cleaning)

-Critical priority tickets have the highest SLA breach rate

-Indicates process or escalation inefficiencies rather than agent performance issues

-High ticket volume does not guarantee high efficiency

-Some agents resolve fewer tickets but with higher SLA compliance and CSAT

-Reopened tickets strongly reduce customer satisfaction

-Tickets reopened more than once consistently show CSAT below 3

-SLA flags in raw data were unreliable

-SLA needed recalculation based on business logic

## 6) Recommendations

1.Implement Skill-Based Ticket Routing

-Assign tickets based on agent expertise and issue type

2.Improve First-Time Resolution

-Add quality checks before ticket closure

3.Automate SLA Validation

-Recalculate SLA dynamically instead of relying on manual flags

4.Use ETL Pipeline (KPL / ETL Concept)

-Extract → Validate → Clean → Load → Visualize

-Ensures consistent, scalable reporting

## 7) Tools Used
### Python
- pandas: Used to load, clean, and process the dataset.
  
### Power BI
- Used to create dashboards and visualize KPIs.

### GitHub
- Used to organize and upload all project files, including code, data, and screenshots.
