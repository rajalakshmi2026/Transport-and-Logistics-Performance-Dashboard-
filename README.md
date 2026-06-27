# Transport-and-Logistics-Performance-Dashboard-
# Fleet Management Dashboard | Excel + Power BI

> End-to-end logistics analytics solution to track trips, fuel efficiency, and on-time delivery performance for fleet operations.

![Dashboard Preview](dashboard-screenshot.png)

## 📌 Project Overview

Built an interactive Fleet Management Dashboard to help logistics teams monitor key operational metrics without manual Excel reports. The dashboard answers 4 critical questions:
1. Are we delivering on time?
2. Which routes/destinations have highest trip volume?
3. What is our fuel consumption vs distance covered?
4. Which vehicle type covers maximum distance?

## 🎯 Key Metrics from Dashboard

| KPI | Value | Insight |
| --- | --- | --- |
| **Total Trips** | 50 | Total shipments completed |
| **Total Distance** | 53K Km | Fleet coverage across cities |
| **Total Fuel** | 4.59K Litres | Fuel consumption tracking |
| **On-Time Deliveries** | 30 (60%) | SLA compliance rate |
| **Late Deliveries** | 20 (40%) | Improvement area identified |

**OTIF Rate: 60%** - 30 on-time out of 50 total deliveries

## 🛠️ Tech Stack & Workflow

**1. Microsoft Excel**
- **Power Query**: Cleaned vehicle logs, trip sheets, and fuel records
- **Data Modeling**: Created relationships between Trips, Vehicles, Destinations
- **Calculated Columns**: Delivery Status, Delay Days, Fuel Efficiency

**2. Microsoft Power BI**
- **KPI Cards**: Top 5 metrics for instant overview
- **Donut Chart**: On-Time vs Late delivery split - 60/40
- **Treemap**: Total Trips by Destination - Mumbai, Delhi, Bangalore leading
- **Bar Chart**: Distance covered by Vehicle Type - Van highest
- **Line Chart**: Monthly trend - Feb vs Jan showing decline in trips & distance
- **Slicers**: Filter by Vehicle Type - Van, Truck, Mini-Truck

## 📊 Dashboard Breakdown

1. **KPI Row**: Total Trips, Distance, Fuel, On-Time, Late - 5 critical numbers upfront
2. **Delivery Status**: Donut chart shows 60% on-time delivery rate
3. **Geographic View**: Treemap of trips by city - Mumbai & Delhi highest volume
4. **Fleet Analysis**: Van covers most distance, followed by Truck
5. **Trend Analysis**: Both trips and distance dropped from Feb to Jan - needs investigation

## 🔑 Key DAX Measures Used

```dax
On-Time Delivery % = 
DIVIDE(
    [On-Time Deliveries],
    [Total Trips],
    0
)

Fuel Efficiency (Km/L) = 
DIVIDE(
    [Total Distance],
    [Total Fuel],
    0
)
// Current: 53K / 4.59K = 11.55 Km/L

Late Delivery % = 
DIVIDE(
    [Late Deliveries],
    [Total Trips],
    0
)
// Current: 20/50 = 40%
