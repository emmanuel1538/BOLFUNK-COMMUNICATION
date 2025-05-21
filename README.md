# **BOLFUNK COMMUNICATION**
## INTRODUCTION
This Power BI project is focused on analysing customer churn and call centre performance for *BOLFUNK COMMUNICATION*, a telecom and SaaS provider. The project aims to uncover actionable insights from customer behaviour and support data to enable proactive retention strategies and service quality improvements.
### Disclaimer
All datasets and reports are for demonstration purposes only and do not represent any real company or customer.
## Skills/Concepts Demonstrated:
The following Power BI skills and concepts were applied:
  * DAX Measures and Calculated Columns
  * Data Cleaning and Transformation
  * KPI Cards
  * Slicers and Filters
  * Interactive Visuals
  * Dashboard Design
  * Trend Analysis
## Problem Statement
*BOLFUNK* is facing rising churn, especially among long-tenured and high-value customers. Despite capturing call center data, they lack real-time insight into emerging churn signals and service gaps.
### Key questions addressed:
1.	Which customers are at the highest risk of churning?
2.	How effective is the call center in resolving customer issues?
3.	What agent-level trends exist in satisfaction and performance?
4.	Which segments (e.g., tenure, contract type, payment method) show the highest churn?
## Modelling:
* The data model includes two independent datasets:
  +	CustomerData (tenure, contract, churn, service usage)
  +	CallCenterData (satisfaction, resolution, escalation, topic, agent)
*	No common key was found; each dataset was analyzed separately.
*	Calculated tables, new columns, and DAX measures were used to enhance the datasets.
  ![](MODELLING.png).
 ## Data Preparation
Performed in Power BI using Power Query and the data model:
* Removed duplicates and corrected inconsistent values.
*	Transformed columns (e.g., converted tenure to numeric).
*	Created logical DAX columns
  ![](tenure%20group%20column.png)
 	 ![](riskscore%20measures.png)
 
*	Created DAX measures:

	Average satisfaction
     ![](avg%20Satisfaction%20measures.png)
 	Churned Revenue
    ![](churned%20Revenue.png)

   

## POWERBI APPROACH
+	Used Customer Data for churn and risk dashboards
+	Used Call Center Data for agent and support trends
+	Built 3 dashboards

## CHURN OVERVIEW
### Purpose:
The Churn Overview Dashboard provides a high-level summary of customer churn trends across various business segments and customer behaviours. It enables the business to detect where churn is most prevalent and identify opportunities for targeted retention strategies.
![](CHURN%20OVERVIEW.png)

### Key Insights
* Overall Churn Rate: 27%, with 1,869 churned customers out of 7,043 total
* Revenue Impact: Churned customers contribute to 17.83% of total revenue, emphasizing the value at risk
* Contract Type Trends:
  + Month-to-month customers have the highest churn rate.
  + Longer-term contracts (one or two years) result in lower churn, suggesting commitment correlates with retention
* Loyalty and Tenure:
  + Customers with < 1 year tenure show the highest churn rate at 48.28%
  + Churn rate consistently declines as tenure increases, underscoring the link between loyalty and retention
* Payment Method Patterns:
  + Mailed checks and electronic checks are more frequent among churned customers.
    
### Recommendations:
* Incentivize longer-term contracts to reduce churn risk
*	Develop onboarding and loyalty-building programs for new customers (< 1 year tenure)
*	Encourage digital payment adoption to build engagement and loyalty
*	Monitor revenue loss trends and prioritize retention efforts for high-value customers
*	Use the dashboard monthly to track changes in churn segments and evaluate the effectiveness of interventions

## RISK OVERVIEW
### Purpose:
This dashboard was created to address the critical business problem of customer churn. The goal was to identify customers at risk of churning by assigning a churn risk score, enabling the company to take targeted retention actions.
![](HIGH%20RISK%20OVERVIEW.png)

#### How the Risk Score Works:
Customers receive points based on churn-related factors:
FACTOR                                 |     CONDITION                          |     POINTS
:-------------------------------------:|:--------------------------------------:|:------------:
Tenure < 6 months | High churn risk | 2
Tenure 6–12 months | Moderate churn risk| 1
Contract = Month-to-month | Most risky contract | 2
No Tech Support | Higher churn tendency| 1
High Monthly Charges (> 80) | Increased risk| 1


### Risk Categories:
Customers are grouped by total risk score:
Score Range	| Risk Level
:----------:|:------------:
5–6 | High
3–4	| Medium
0–2 | Low

### Key Insights:
* High-risk customers show the highest likelihood to churn (~60% precision)
*	Churn also occurs among medium and low-risk groups, indicating other factors at play
*	Retention strategies should not only focus on new customers but also address issues faced by long-term customers
### Recommendations:
*	Prioritize retention campaigns on high-risk customers
*	Conduct further analysis on medium-risk customers to better understand churn drivers
*	Incorporate behavioural data (e.g., usage patterns, support tickets) to refine risk predictions
*	Use the dashboard regularly to monitor churn risk trends and the effectiveness of retention efforts


## AGENT OVERVIEW
### Purpose:
This dashboard analyses call centre performance with a focus on agent efficiency, first contact resolution (FCR), customer satisfaction, and escalation trends. It aids operational decisions by identifying service gaps and highlighting opportunities for agent support and process improvement.
![](AGENT%20OVERVIEW.png)

### Key Insights:
*	A large portion of calls (nearly half) are being escalated, especially in the Technical and Billing areas
*	Billing inquiries receive the highest satisfaction scores (3.2), while Technical and Account topics trail behind (2.9)
*	Monthly satisfaction scores fluctuate, with the lowest in April (2.92) and the highest in November (3.07) — potentially reflecting seasonal staff capacity or service demand
*	Agent performance varies; some agents consistently outperform others, indicating a need for best practice sharing or training
*	The low FCR rate (26.02%) indicates a major issue in customer Agent efficiency.

### Recommendations:
*	Strengthen training programs, especially in technical issue handling
*	Reduce escalations by improving knowledge bases and frontline resolution capacity
*	Monitor agents with consistently low satisfaction or resolution scores and provide coaching
*	Investigate April's dip in satisfaction to identify root causes (e.g., understaffing, peak load)
*	Use trend data to optimize staffing and performance targets across months

## Conclusion & Recommendations
* The Risk Analysis Dashboard helps proactively target high-risk customers with tailored retention offers.
* The Agent Overview Dashboard reveals operational gaps, particularly in technical resolution and satisfaction.
* The Churn Overview Dashboard shows strong links between short tenure, month-to-month contracts, and churn.

### Next Steps include:
* Agent re-training,
* contract optimization strategies,
* churn prediction automation.

