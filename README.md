![Dashboard](https://github.com/user-attachments/assets/54878b10-d717-4fd5-b587-a4b7118b531e)
# Plato-s-pizza
This project analyzes a Plato's pizza's sales data using Power BI. It answers key business questions such as customer traffic patterns, bestselling pizzas, peak ordering hours, and sales performance.
# About the Data Set
A year's worth of sales from a fictitious pizza place, including the date and time of each order and the pizzas served, with additional details on the type, size, quantity, price, and ingredients.

# Key Business Questions Answered
How many customers do we have each day? Are there any peak hours?

Analyzed unique daily orders and hourly breakdowns to identify peak traffic periods (12–1 PM, 6–7 PM).

How many pizzas are typically in an order? Do we have any bestsellers?

Used quantity analysis and pizza-level aggregation to identify high-performing and underperforming menu items.

How much money did we make this year? Can we identify any seasonality in the sales?

Created revenue measures using quantity × price, with visuals for monthly and weekly trends (optional seasonal breakdown).

Are there any pizzas we should take off the menu, or any promotions we could leverage?

Ranked all pizzas by sales and frequency across peak hours to identify candidates for promotion or removal.

# Data Model Structure
Table	Description

orders:	Order ID, date, and time of each order
order_details:	Pizza quantity and associated order ID
pizzas:	Pizza ID, size, and price
pizza_types:	Pizza name and  category

# Relationships:

orders → order_details 

order_details → pizzas 

pizzas → pizza_types 

# DAX Measures & Features
Order Hour: Extracted using HOUR(orders[time]) for time-based analysis

Customers by Hour: Counts distinct orders per hour

Total Pizza Orders: SUM(order_details[quantity])

Top-Selling Pizza: Uses TOPN and RANKX to display highest-selling item dynamically

Revenue : SUMX(order_details, quantity * RELATED(price))

# Dashboard Highlights
KPI Cards for total revenue, top-selling pizza, and average orders

Bar Charts to show customer volume by hour and pizza popularity

Table Visuals to display pizza sales by name

# Tools Used
Power BI Desktop

DAX (Data Analysis Expressions)

Relational data modeling

Maven-provided dataset

# Dataset Source
This dataset was provided by Maven Analytics as part of their community challenge.

# Business Recommendations
Schedule more staff during peak lunch (12–1 PM) and dinner (6–7 PM) windows.

Promote top-performing pizzas during high-traffic periods.

Retire or rebrand low-selling pizzas to simplify the menu and reduce operational overhead.

Consider time-based promotions or bundles for mid-afternoon or late-night low-volume hours.

# Conclusion
This dashboard empowers Plato’s Pizza to make data-driven decisions around staffing, menu optimization, and marketing strategies — turning raw sales data into clear, actionable business insights.
