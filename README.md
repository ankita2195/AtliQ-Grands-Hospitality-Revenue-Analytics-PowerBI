# AtliQ Grands | Hospitality Revenue & Performance Analysis

**Power BI · DAX · Data Modelling · Business Intelligence**

The project is focused on diagnosing revenue and booking performance across AtliQ Grands' hotel portfolio in India. Built to help management understand occupancy patterns, revenue drivers, booking behaviour and opportunities to improve commercial performance.

## 👉 **Live Dashboard:** [View Power BI Dashboard](https://app.fabric.microsoft.com/view?r=eyJrIjoiNjQ4ZDZiOTUtMjZkNi00MjdjLWFmYjAtZmEzZDZkYjc1MGNmIiwidCI6ImE1ZmI3ZjgwLTIwNTEtNGE5Ny05YjEyLTZhYjIyMmQyYmQ1NSJ9)

## Business Problem

AtliQ Grands, a hotel chain with a 20-year operating history, was facing declining market share and revenue amid increasing competition. The objective was to turn historical booking data into actionable insights that could support better revenue management and business decisions.

## Project at a Glance

- 25 Properties
- 4 Cities
- 5 Source Tables
- 143790 Fact Records analyzed
- 26 DAX Measures used
- 2 Calculated Columns created

**Data volume:** 134,590 booking-level records and 9,200 aggregated booking records.

## Dashboard Highlights

<img width="1090" height="732" alt="image" src="https://github.com/user-attachments/assets/fabcdf36-5819-45c2-922e-122b57f33a8b" />

The Power BI dashboard provides an overview of revenue, occupancy, pricing, booking realisation and property-level performance.

| Key metric | Dashboard result |
|---|---:|
| Revenue Realised | ₹1.69 billion |
| Occupancy | 57.79% |
| RevPAR | ₹7,337 |
| ADR | ₹12,696 |
| Realisation | 70.14% |
| Cancellation Rate | 24.8% |
| Average Rating | 3.6 / 5 |

## Key Business Metrics

| Metric | Definition |
|---|---|
| **ADR (Average Daily Rate)** | Average revenue per booking. |
| **RevPAR (Revenue Per Available Room)** | Revenue earned per available room. |
| **Occupancy %** | Percentage of available room capacity successfully booked. |
| **Realisation %** | Percentage of bookings that were neither cancelled nor marked as no-show. |
| **DBRN** | Daily Booked Room Nights – average bookings per day. |
| **DSRN** | Daily Sellable Room Nights – average available room capacity per day. |
| **DURN** | Daily Utilised Room Nights – average checked-out bookings per day. |

**Notable findings**

- **Weekend demand is stronger:** Occupancy reaches 62.64% on weekends versus 55.85% on weekdays. Weekend RevPAR is also higher at ₹7,972 compared with ₹7,083 on weekdays.
- **Luxury drives revenue:** Luxury properties contribute 61.6% of total realised revenue, compared with 38.4% from Business properties.
- **Booking realisation needs attention:** Only 70.14% of bookings are realised, while cancellations account for 24.8%.

## Business Recommendations

**1. Introduce demand-based dynamic pricing**

Adopt differentiated pricing for weekdays and weekends, with higher rates during weekends and other high-demand periods. Use occupancy trends, booking patterns and property-level performance to adjust room prices rather than relying on fixed rates.

**2. Strengthen direct booking channels**

Introduce targeted offers or value-added incentives for customers booking through AtliQ's direct online and offline channels. Lower dependence on third-party platforms could help reduce commission costs and improve booking-channel profitability. Test incentives against incremental bookings and net revenue before scaling them.

## Data Model & Relationships

Designed a **star schema** data motel with **two fact tables and three shared dimension tables**.

<img width="1533" height="773" alt="Screenshot 2026-11-22 115931" src="https://github.com/user-attachments/assets/6f003c27-79b5-43f3-9530-495eefd6c0a8" />

- **Fact tables:** `fact_bookings`, `fact_aggregated_bookings`
- **Dimension tables:** `dim_date`, `dim_hotels`, `dim_rooms`
- Established one-to-many (1:*) relationships from each dimension table to both fact tables.
- Used shared dimensions to support consistent filtering and analysis across booking-level and aggregated booking data.

## DAX & Analytical Measures

Created **26 DAX measures and 2 calculated columns** to support KPI reporting, performance comparisons and time-based analysis.

**Revenue & Pricing**
- Revenue Realised
- ADR (Average Daily Rate)
- RevPAR (Revenue Per Available Room)

**Occupancy & Booking Performance**
- Occupancy %
- Total Capacity
- Successful Bookings
- DBRN, DSRN and DURN

**Booking Behaviour**
- Cancellation %
- No-Show Rate %
- Realisation %
- Booking Contribution by Platform and Room Class
- Average Rating

**Time Intelligence**
- Week-on-Week change in Revenue, Occupancy, ADR, RevPAR, Realisation and DSRN.

**Calculated columns**
- Week Number
- Day Type (Weekend / Weekday), based on the business-defined Friday–Saturday weekend.

## Tools & Techniques

- **Power BI:** Data modelling, interactive dashboards, KPI reporting and visual analysis.
- **DAX:** Calculated columns, context-aware measures, CALCULATE, DIVIDE, ALL, FILTER, HASONEFILTER and time-based comparisons.
- **Data Modelling:** Fact and dimension tables, shared dimensions and one-to-many relationships.
- **Business Analysis:** Revenue performance, occupancy trends, booking-channel analysis and pricing recommendations.

## Project Objective

Move beyond reporting hotel performance to identify where revenue opportunities and booking inefficiencies exist—and translate those findings into practical commercial recommendations.
