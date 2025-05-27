# DATA_MANAGEMENT_Assignment2
# Airline On-Time Performance Analysis (2007)
<p align="center">
  <img src="pic/flyfly.png" width="600"/>
</p>  

This project analyzes flight delays and cancellations in the U.S. commercial airline network using operational data from 2007. It examines when flights are most likely to be on time, what types of disruptions contribute most to delays, how cancellation patterns vary across carriers and airports, and which routes consistently perform the worst. Hive SQL is used for querying large-scale flight records, while Python supports data visualization and pattern interpretation.


---
## *1. Project Objectives*

This project aims to:

- Identify temporal trends in flight departure delays and cancellation rates.
- Analyze the operational causes contributing to total delays.
- Decompose cancellation patterns across airlines, airports, months, and time of day.
- Highlight underperforming flight routes and carriers based on delay and cancellation metrics.

---

## *2. Tools & Libraries*

- Python 3.10+
- Jupyter Notebook
- Hive SQL
- Pandas, Matplotlib
- Optional: Seaborn, Plotly

---

## *3. Data Source*

- [Data Expo 2009: Airline On Time Data_year_2007](https://www.kaggle.com/datasets/wenxingdi/data-expo-2009-airline-on-time-data/data?select=2007.csv)

---

## *4. Project Structure*

The project is organized into six core sections:

### 1 Preliminary Preparations
- Hive database connection and inspection of table schema.

### 2 Delay Patterns
- Analysis of how delays vary by:
  - Time of day
  - Day of the week
  - Month and season

### 3 Delay Factors
- Ranking of Delay Factors and Quantification of Influential Factors:
  - Carrier, Weather, NAS, Security, Late Aircraft

### 4 Cancellation Analysis
- Exploration of cancellation reasons (Codes A–D)
- Cancellation rate breakdown by:
  - Airline
  - Airport
  - Month vs Reason
  - Hour of departure

### 5 Problematic Routes
- Identification of:
  - Average Departure Delays by Route
  - Average Departure Delays by Flight Number
- Analysis of：
  - Breakdown of Delay Causes for Top Problematic Routes 
  - Breakdown of Cancellation Reasons for Top Cancelled Routes

### 6 Conclusion

---
<p align="center">
  <img src="pic/flypic.jpg" width="600"/>
</p>  


## *5. Findings Summary*

- **Morning flights (07:00–08:59)** are the most punctual, while **evening flights** face significantly higher delays due to propagation.
- **Delays tend to accumulate over the day**, reinforcing the importance of early departures in mitigating disruption.

- **Late Aircraft and Carrier delays account for ~70%** of total delay minutes, indicating strong inter-flight dependencies and airline-level inefficiencies.
- **Cancellations are most frequently caused by Carrier issues**, followed by **weather and NAS disruptions**.

- **Cancellations peak in winter**, especially **February and December**, with weather being a key driver.
- **Late-night flights (0–5 AM)** show high cancellation rates despite lower traffic volume.

- **Routes such as ORD–LGA and ORD–EWR** experience the most cumulative delay minutes, largely due to **NAS and aircraft connectivity issues**.
- **Routes like LGA–LEX and TEX–PHX** are most vulnerable to **weather-driven cancellations**, indicating regional operational risk.


---

## *6. Conclusion*


This project conducts a comprehensive analysis of U.S. airline delays and cancellations in 2007, using Hive SQL and Python to uncover temporal patterns, operational bottlenecks, and route-level vulnerabilities. The study reveals that delays accumulate over the course of the day, with morning flights being the most reliable, and cancellations peaking in winter months and early morning hours.


Late aircraft and carrier-related issues were the largest contributors to total delay time, while weather and airline decisions were the main drivers of cancellations—especially on routes linked to smaller regional airports. Underperforming routes and flights were identified based on both average delays and total disruption volume, with delay and cancellation causes further broken down for targeted understanding.


The results provide a data-driven foundation for improving airline reliability through better scheduling, risk-aware route planning, and enhanced operational flexibility, particularly on high-delay or weather-sensitive connections.

---

## *7. Key Visualizations*

| Section | Visualization |
|---------|----------------|
| 2.1 | `2.1.1_delay_by_time.png` |
| 2.1 | `2.1.2_hourly_delay_and_count_morning.png` |
| 2.2 | `2.2_arrival_otp_by_day.png` |
| 2.3 | `2.3.1_arrival_otp_by_month.png` |
| 2.3 | `2.3.2_arrival_otp_by_season.png` |
| 3.1 | `3.1_total_delay_by_factor.png` |
| 3.1 | `3.1_delay_proportion_pie.png` |
| 4.1 | `4.1_primary_cancellation_reasons.png` |
| 4.2 | `4.2.1_cancel_rate_by_airline.png` |
| 4.2 | `4.2.2_cancel_rate_by_origin_airport.png` |
| 4.2 | `4.2.3_cancel_rate_by_month.png` |
| 4.2 | `4.2.3_monthly_cancel_reason_breakdown.png` |
| 4.2 | `4.2.4_cancel_rate_by_hour.png` |
| 5.1 | `5.1.1_top_routes_by_avg_delay.png` |
| 5.1 | `5.1.2_top_flights_by_avg_delay.png` |
| 5.2 | `5.2.1_delay_cause_stack_top_routes.png` |
| 5.2 | `5.2.2_cancel_reason_stack_top_routes.png` |
