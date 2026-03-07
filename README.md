# Route Profitability Analysis
## 1. Problem
A logistics company wants to identify underperforming transportation routes that are generating low or negative profit. The goal of this analysis is to evaluate revenue and operational costs across routes in order to identify opportunities to improve profitability.

## 2. DataSet

The dataset used in this analysis represents operational data from a logistics company. It contains multiple relational tables describing transportation activities, drivers, vehicles, and fuel purchases.

Key characteristics of the dataset:
- 14 relational tables
- Total Records: 361,799
- Date Range: 2022-2024
- Database Size: ~85,000+ unique operational records
- Core tables: drivers, trucks, trailers, customers, facilities, routes
- Transaction Tables: loads, trips, fuel_purchases, maintenance_records, Delivery events, safety_incidents
- Important fields include revenue, fuel cost, trip distance, and route identifiers
- Tables are linked using primary and foreign keys such as route_id, driver_id and Load_id



## 3. Data Quality Checks
The following validations were performed:
- Checked for duplicate records in fact tables such as loads, trips, and delivery_events
- Verified that key identifiers such as driver_id, truck_id, and route_id were not missing
- Validated cost fields in fuel_purchases and maintenance_records to ensure no negative values were present
- Confirmed primary key uniqueness in dimension tables such as drivers, trucks, and routes
The dataset was generally well-structured and required minimal preprocessing before performing the analysis.

