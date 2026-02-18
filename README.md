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
Dashboard 1: Operational Overview
Purpose: This tab focuses on the "What"—ticket volumes, adherence to deadlines (SLAs), and the nature of the issues coming in.

1. Top KPI Cards (The Big Numbers)
Total Tickets Assigned (384): The total workload that came into the queue.

Total Tickets Resolved (344): The number of tickets closed. Insight: The team has cleared ~90% of the assigned volume, which is a strong closure rate.

Open Tickets (40): What is currently pending in the pipeline.

SLA Compliance % (56%): The percentage of tickets resolved within the agreed-upon time limit. Insight: This is a critical red flag. Ideally, this should be 90%+. A 56% compliance means nearly half of all tickets are breaching deadlines.

Average Resolution Time (5.81 Hours): It takes the team nearly 6 hours on average to fix an issue.

2. Charts & Visuals
Customer Satisfaction by Issue and Priority (Combo Chart):

What it shows: The bars show the volume of tickets per issue type (Software, Database, etc.), and the line/dots likely represent the Customer Satisfaction (CSAT) score.

Insight: "Software" has the highest volume (tallest bar). You can check if high-volume areas have lower satisfaction scores to identify pain points.

Ticket Distribution by Priority (Column Chart):

What it shows: A breakdown of tickets by urgency (High, Medium, Low, Critical).

Insight: The majority of tickets are High and Medium priority. This explains the pressure on the team and might correlate with the low SLA score—if everything is "High Priority," it's hard to prioritize effectively.

Count of Ticket_ID by Issue_Type (Donut Chart):

What it shows: The percentage composition of incoming tickets.

Insight: Software (24%) and Database (20%) make up nearly half of all requests. This suggests where training or documentation should be focused.

SLA Compliance by Issue (Bar Chart):

What it shows: Adherence to deadlines broken down by category.

Insight: Hardware seems to have the lowest SLA compliance (shortest bar), while Database is slightly better. Hardware issues might be taking longer due to physical repair times or part shipping.

3. The Detailed Grid (Bottom Right)
What it shows: A granular list of individual tickets (Ticket ID, Agent, Priority, Issue Type, etc.).

Use case: Use this if asked about specific "failed" tickets (those marked "No" in the SLA_Met column) during the Q&A.

Dashboard 2: Agent Performance and Quality Analysis
Purpose: This tab focuses on the "Who"—comparing individual team members to identify top performers and those needing coaching.

1. Top KPI Cards
Resolution Efficiency % (89.6%): Overall, the team resolves almost 90% of what they touch.

Avg Resolution Time (5.81 hrs): Consistent with the first dashboard.

SLA Compliance (56.0%): Consistent with the first dashboard.

Backlog Tickets (40): The number of unresolved tickets currently sitting with agents. (Note: There is a typo in the dashboard "Backlog Tickes"—you might want to mentally correct this while speaking).

2. Charts & Visuals
Resolution Efficiency % by Agent_ID (Bar Chart):

What it shows: A leaderboard of agent performance.

Insight: Agents A102 and A105 are your top performers with 95% efficiency. Agent A103 is lagging significantly at 74%. This indicates a need for performance review or additional training for A103.

Average Resolution Time by Agent_ID (Bar Chart):

What it shows: How fast each agent works.

Insight: Agent A103 has the longest bar (slowest), confirming the issue seen in the efficiency chart. Agent A101 appears to be the fastest.

Agent vs Issue Type Workload (Heatmap/Matrix):

What it shows: Who is working on what.

Insight: The workload is distributed fairly evenly (mostly 5 tickets per category per agent), so no single agent is being overloaded with harder tasks. This rules out "unfair workload" as an excuse for A103's poor performance.

Ticket Reopen Rate by Agent (Stacked Column Chart):

What it shows: The dark blue represents "Reopened" tickets (tickets sent back because they weren't fixed right the first time).

Insight: Agent A103 has the largest dark blue block. This means they are closing tickets too fast or incorrectly, causing customers to reopen them. This "Double Handling" is likely killing the team's overall productivity.
  
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
