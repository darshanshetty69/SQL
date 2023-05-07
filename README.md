## Prologue
- Company X is one of the world’s most recognized brands and one of America’s leading retailers. It makes itself a preferred shopping destination by offering outstanding value, inspiration, innovation and an exceptional guest experience that no other retailer can deliver.

- This business case has information of 100k orders from 2016 to 2018 made at Target in Brazil. Its features allows viewing an order from multiple dimensions: from order status, price, payment and freight performance to customer location, product attributes and finally reviews written by customers.

- <b>Task at hand is, given this data, analyze and provide some insights and recommendations from it</b>

## Data
Data is available in 8 csv files:
1. customers.csv
2. geolocation.csv
3. order_items.csv
4. payments.csv
5. reviews.csv
6. orders.csv
7. products.csv
8. sellers.csv

## Activities performed

Import the dataset and do usual exploratory analysis steps like checking the structure & characteristics of the dataset

- Data type of columns in a table
- Time period for which the data is given
- Cities and States of customers ordered during the given period

In-depth Exploration:

- Is there a growing trend on e-commerce in Brazil? How can we describe a complete scenario? Can we see some seasonality with peaks at specific months?
- What time do Brazilian customers tend to buy (Dawn, Morning, Afternoon or Night)?

Evolution of E-commerce orders in the Brazil region:

- Get month on month orders by states
- Distribution of customers across the states in Brazil

Impact on Economy: Analyze the money movement by e-commerce by looking at order prices, freight and others.

- Get % increase in cost of orders from 2017 to 2018 (include months between Jan to Aug only) - You can use “payment_value” column in payments table
- Mean & Sum of price and freight value by customer state

Analysis on sales, freight and delivery time

- Calculate days between purchasing, delivering and estimated delivery
- Find time_to_delivery & diff_estimated_delivery. Formula for the same given below:

time_to_delivery = order_purchase_timestamp-order_delivered_customer_date

diff_estimated_delivery = order_estimated_delivery_date-order_delivered_customer_date

- Group data by state, take mean of freight_value, time_to_delivery, diff_estimated_delivery
- Sort the data to get the following:
- Top 5 states with highest/lowest average freight value - sort in desc/asc limit 5
- Top 5 states with highest/lowest average time to delivery
- Top 5 states where delivery is really fast/ not so fast compared to estimated date

Payment type analysis:

- Month over Month count of orders for different payment types
- Count of orders based on the no. of payment installments
