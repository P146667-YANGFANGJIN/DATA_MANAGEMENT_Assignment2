# DATA_MANAGEMENT_Assignment2
# Airline On-Time Performance Analysis (2007)

This project investigates flight delays and cancellations in the United States using the 2007 on-time performance dataset. Data was extracted from Hive using SQL, and all visualizations and statistical breakdowns were performed using Python (Pandas + Matplotlib).

---

## 1. Project Structure

The project is organized into five core sections:

### 1.1 Preliminary Setup
- Hive database connection and inspection of table schema.

### 1.2 Delay Patterns
- Analysis of how delays vary by:
  - Time of day
  - Day of the week
  - Month and season

### 1.3 Delay Causes
- Aggregation and comparison of five types of delay causes:
  - Carrier, Weather, NAS, Security, Late Aircraft

### 1.4 Cancellation Analysis
- Exploration of cancellation reasons (Codes A–D)
- Cancellation rate breakdown by:
  - Airline
  - Airport
  - Month
  - Hour of departure

### 1.5 Problematic Routes
- Identification of:
  - Routes and flights with highest average delays
  - Routes with highest total delay minutes
  - Most frequently cancelled routes

---

## 2. Key Visualizations

| Section | Visualization |
|---------|----------------|
| 2.1 | `2.1_delay_by_time.png` |
| 2.1 | `2.1_hourly_delay_and_count.png` |
| 2.2 | `2.2_arrival_otp_by_day.png` |
| 2.3 | `2.3_arrival_otp_by_month.png` |
| 3.1 | `3.1_total_delay_by_factor.png` |
| 3.1 | `3.1_delay_proportion_pie.png` |
| 4.1 | `4.1_primary_cancellation_reasons.png` |
| 4.2 | `4.2_cancel_rate_by_airline.png` |
| 4.2 | `4.2_cancel_rate_by_origin_airport.png` |
| 4.2 | `4.2_cancel_rate_by_month.png` |
| 4.2 | `4.2_monthly_cancel_reason_breakdown.png` |
| 4.2 | `4.2_cancel_rate_by_hour.png` |
| 5.1 | `5.1_top_routes_by_avg_delay.png` |
| 5.1 | `5.1_top_flights_by_avg_delay.png` |
| 5.2 | `5.2_delay_cause_stack_top_routes.png` |
| 5.2 | `5.2_cancel_reason_stack_top_routes.png` |

---

## 3. Findings Summary

- **Morning flights** are the most punctual; **late-night and winter flights** show higher delays and cancellations.
- **Carrier** and **late aircraft delays** are the top contributors to total delay time.
- **Weather** and **airline issues** are the most common cancellation reasons.
- Routes such as **ORD–LGA**, **ORD–EWR**, and **LGA–ORD** showed the highest total delay minutes.
- Flights operated by **OO** and **CO** had the worst average delays.
- Routes like **LGA–LEX** and **TEX–PHX** were most prone to weather-related cancellations.

---

## 4. Conclusion

This analysis highlights both temporal and operational dimensions of airline disruptions in 2007. Delays are concentrated in specific time windows and routes, often due to systemic factors such as airspace congestion and aircraft turnover. Cancellations are dominated by weather and airline decisions, particularly on regionally exposed or poorly buffered connections.

The results provide a data-backed foundation for prioritizing improvements in scheduling resilience, hub coordination, and proactive management of vulnerable routes.
