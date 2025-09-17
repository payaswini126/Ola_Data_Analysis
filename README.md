🚖 Ola Ride Booking Analytics Dashboard 
📌 Project Overview

An end-to-end analytics solution analyzing 1,03,024 simulated Ola bookings in Bengaluru (July 2024). Using SQL for backend querying and Power BI for visualization, this project uncovers insights on ride volume, cancellations, customer loyalty, revenue flows, and satisfaction trends, enabling data-driven decisions for ride-hailing operations.

🎯 Objectives & Business Problem

Ride-hailing platforms face challenges like high cancellation rates, fluctuating demand, and driver-customer experience gaps.
This project aims to:

Track ride booking performance (success vs cancellations).

Analyze customer and driver behavior patterns.

Identify revenue leakage points and growth opportunities.

Provide business-ready dashboards to support strategy teams.

🛠️ Tech Stack

SQL (MySQL): Data querying, views, aggregations.

Power BI Desktop: Interactive dashboards & data storytelling.

Power Query + DAX: Data cleaning, transformations, and KPI creation.

Data Modeling: Relationships across booking, customer, and metrics tables.

📊 Key Dashboard Features

Booking Status Breakdown: Success (62.09%), Cancelled (28.08%) split by driver/customer.

Revenue Analysis: ₹35M total booking value, broken down by Cash, UPI, Cards.

Customer Loyalty: Top 5 customers generated ₹30K+ revenue.

Cancellation Trends: Driver-related (17.89%) vs Customer-related (10.19%).

Ratings Monitoring: Both driver & customer ratings ~4.0, indicating stable satisfaction.

Ride Volume Over Time: Day-wise booking patterns for July 2024.

📷 Dashboard Preview:


🗄️ SQL Queries & Analytical Views
-- Successful bookings
create view successful_bookings as 
select * from bookings where Booking_Status = 'Success';

-- Top 5 most frequent customers
create view top_5_customers as 
select Customer_ID, count(Booking_Id) as total_rides 
from bookings 
group by Customer_ID 
order by total_rides desc limit 5;

-- Average ride distance per vehicle type
create view avg_distance_per_vehicle_type as 
select Vehicle_Type, avg(Ride_Distance) as Avg_Ride_Distance 
from bookings group by Vehicle_Type;

-- Total successful booking value
create view total_successful_booking_value as 
select sum(Booking_Value) as total_booking_value 
from bookings where Booking_Status = 'Success';

📈 Business Impact & Insights

Revenue Optimization: ₹35M in booking value analyzed, with UPI leading as a preferred mode → scope for fintech partnerships.

Operational Efficiency: 28% cancellations highlight driver allocation issues, requiring better fleet planning.

Customer Retention: Power-users contribute disproportionate value → potential for loyalty programs.

Fleet Strategy: Vehicle-type demand mapped to ride distances for optimized resource allocation.

Satisfaction Insights: Consistent ~4.0 ratings signal stable but improvable experience.

📂 Deliverables

Interactive Power BI Dashboard (.pbix)

SQL Scripts (.sql)

Project Documentation (.pdf)

✅ Takeaway: This project demonstrates my ability to design end-to-end analytics workflows, combining data engineering (SQL), data visualization (Power BI), and business insight generation — the same skills critical for real-world data analyst roles.
