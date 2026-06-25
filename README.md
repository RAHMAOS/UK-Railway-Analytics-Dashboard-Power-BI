
# UK Railway Analytics Dashboard — Power BI

## 📌 Project Overview
This Power BI project provides an in-depth analysis of UK Railway data, focusing on ticket purchases, journey performance, and customer behavior. The dashboard enables users to explore trends in passenger travel, delays, ticket sales, and refund requests across multiple interactive report pages. The analysis helps railway operations teams understand how the system operates and identify areas for improvement in efficiency, punctuality, and customer satisfaction.

## 📊 Key Features
- **Ticket Sales Analysis**: Breakdown of ticket purchases by type, class, payment method, and purchase channel (Online vs Station).
- **Revenue Insights**: Total revenue across ticket types, seat classes, railcard segments, and monthly trends — including refund impact analysis.
- **Journey Performance**: On-time rate, delay rate, cancellation rate, and delay cause breakdown by station and route.
- **Passenger Flow**: Popular routes, busiest departure stations, peak travel hours, and demand patterns.
- **Refund Analysis**: Refund request rate and its relationship to journey status, ticket type, and delay reasons.
- **Time Trend Analysis**: Monthly revenue, trip volume, disruption trends, and average ticket price with constant reference lines.
- **Customer Behavior**: Purchase channel trends, payment method splits, railcard holder distribution, and customer segment analysis.
- **Drillthrough Pages**: Deep-dive analysis at the station level, route level, and ticket type level — triggered by right-clicking any data point.

## 📂 Dataset Information
- **File Name**: `railway.csv`
- **Total Records**: 31,653
- **Date Range**: December 2023 – April 2024
- **Columns**:
  - `Transaction ID`: Unique identifier for each ticket purchase.
  - `Date of Purchase`, `Time of Purchase`: Timestamp of the ticket purchase.
  - `Purchase Type`: Whether the ticket was purchased online or at a station.
  - `Payment Method`: Payment method used (Credit Card, Contactless, or Debit Card).
  - `Railcard`: Whether the passenger holds a railcard (Adult, Senior, Disabled, or None). Railcard holders receive 1/3 off ticket price.
  - `Ticket Class`: Seat class for the ticket (Standard or First Class).
  - `Ticket Type`: When the ticket was purchased or can be used — Advance (1/2 off, must be purchased at least 1 day prior), Off-Peak (1/4 off, valid outside peak hours), or Anytime (full price, no restrictions).
  - `Price`: Final cost of the ticket in GBP (£1 – £267).
  - `Departure Station`: Origin station (12 unique stations).
  - `Arrival Destination`: Destination station (32 unique destinations).
  - `Date of Journey`: Scheduled travel date.
  - `Departure Time`: Scheduled departure time.
  - `Arrival Time`: Scheduled arrival time (can be the day after departure).
  - `Actual Arrival Time`: Actual arrival time (can be the day after departure).
  - `Journey Status`: Whether the journey was On Time, Delayed, or Cancelled.
  - `Reason for Delay`: Cause of delay when applicable (Weather, Signal Failure, Technical Issue, Staff Shortage, Traffic).
  - `Refund Request`: Whether the passenger requested a refund (Yes or No).

## 🛠️ Tools & Technologies Used
- **Power BI Desktop**: Interactive visualizations, data modeling, and report pages.
- **DAX (Data Analysis Expressions)**: 30+ custom measures including time intelligence, TOPN station rankings, drillthrough dynamic titles, and on-time rate with station threshold filtering.
- **Power Query (M Language)**: Data transformation, type conversions, delay reason standardization, calculated columns (Journey Duration, Delay Minutes, Route, Discount Percentage, Hour of Purchase, Purchase Lead Days).


## 📄 Dashboard Pages
| Page | Type | Description |
|---|---|---|
| Home | Main | Landing page with headline KPIs and navigation cards to all pages |
| Overview | Main | High-level KPIs, monthly revenue trend, journey status, payment and delay breakdowns |
| Regional | Main | Revenue and on-time rate by station, top routes by revenue table |
| Product | Main | Ticket type revenue, class split, railcard distribution, avg price by type |
| Customer | Main | Purchase channel trends, payment method, matrix, refund trend, customer treemap |
| TimeTrend | Main | Monthly combo chart, disruption stacked bars, on-time trend, avg price trend |
| Station Details | Drillthrough | Hidden — right-click any station to drill through for station-level deep dive |
| Route Details | Drillthrough | Hidden — right-click any route to drill through for route-level deep dive |
| Ticket Type Details | Drillthrough | Hidden — right-click any ticket type to drill through for product-level deep dive |

## 🚀 How to Use
1. Download and install **Power BI Desktop** from https://powerbi.microsoft.com/desktop
2. Clone or download this repository.
3. Place `railway.csv` in the same folder as `UK_Railway_Projectfinal.pbix`.
4. Open `UK_Railway_Projectfinal.pbix` in Power BI Desktop.
5. If prompted about the data source path, go to **Transform Data → Data source settings** and update the path to your local `railway.csv` location.
6. Click **Refresh** (Home tab) to reload all data.
7. Explore the report pages using the left sidebar Page Navigator.
8. Use slicers and cross-filtering to drill down into specific stations, ticket types, or time periods.
9. Right-click any station, route, or ticket type data point to access the drillthrough detail pages.

## 📈 Key KPIs
| KPI | Value |
|---|---|
| Total Revenue | £741,921 |
| Total Journeys | 31,653 |
| On-Time Rate | 86.8% |
| Delay Rate | 7.2% |
| Cancellation Rate | 5.9% |
| Average Ticket Price | £23.44 |
| Refund Request Rate | 3.53% |
| Most Common Payment | Credit Card (60.5%) |
| Most Common Ticket Type | Advance (55.5%) |
| Top Revenue Station | London Kings Cross (£199,650) |
| Busiest Route | Manchester Piccadilly → Liverpool Lime Street |
| Top Delay Cause | Weather (32.9% of delays) |

## ⚡ Future Enhancements
- Incorporate real-time data updates via Power BI Service scheduled refresh.
- Implement predictive modeling for train delays using Python/R visuals in Power BI.
- Add geographical analysis with an interactive map visual showing passenger flow between stations.
- Integrate customer satisfaction (CSAT) survey data to correlate with delay and cancellation patterns.
- Add Revenue per Passenger-Kilometer KPI once distance data between stations becomes available.
- Build a mobile-optimized report layout for on-the-go access by operations teams.

---

### 👥 Team Members & Roles

| Name | Role |
|---|---|
| Amr Ahmed Farouk  | Data Preparation & Cleaning Lead |
| Salma Ibrahim Omair | Data Modeling Lead & Report Storytelling & Interactivity |
| Malak Wael | DAX & Measures Lead |
| Rahma Osama Mohamed | Visuals & Dashboard Lead |
| Mahmoud Ahmed Mahmoud| Testing, QA & Documentation Lead |
| Alaa Mohamed Sayed & Salma Ibrahim | Presentation & Reporting Lead |
