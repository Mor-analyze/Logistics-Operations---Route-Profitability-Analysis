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
Before conducting the analysis, several data quality checks were performed to ensure the reliability and accuracy of the dataset. The validation focused on the tables that are directly relevant to the route profitability business case.

The following tables were reviewed:
- Trips
- Loads
- Routes
- Fuel_Purchases
- Maintenance_Records

Key data quality checks included:
- Identifying missing values in critical fields
- Checking for duplicate records using primary keys
- Validating data types and logical values (e.g., non-negative cost and distance values)
- During this process, missing values were identified in the Trips and Fuel_Purchases tables. Since these fields are essential for operational and cost analysis, records containing null values were removed to maintain data integrity and ensure accurate profitability calculations.


## 4. SQL Analysis
- profit = revenue - costs(fuel and maintenance)
- Data existed at different levels (truck vs trip vs route). Direct joins caused row duplication and inflated maintenance costs.
Used CTEs to structure the analysis step-by-step
Aggregated data before joining
Applied cost allocation:
maintenance_per_mile × route_miles
Ensured accurate and consistent totals



## 5. Dashboard

## 6. Insights

## 7. Recommendation
