# ShopSmart — SQL Business Analysis

## Project Overview
ShopSmart is a fictional e-commerce business. This project uses SQL to analyze orders and delivered-order revenue so a business manager can review sales performance and identify operational follow-ups.

## Business Objectives
- Summarize orders by status.
- Calculate delivered revenue by product, city, customer, and month.
- Compare May and June 2026 performance.
- Identify pending and cancelled orders for follow-up.

## Database Structure
The project uses a MySQL database named `ShopSmart` with three related tables:
- **Customers** — customer name, city, and signup date.
- **Products** — product name, category, and price.
- **Orders** — order date, customer ID, product ID, quantity, and order status.

Relationships:
- `Orders.Customer_ID` references `Customers.Customer_ID`.
- `Orders.Product_ID` references `Products.Product_ID`.

## SQL Skills Demonstrated
- `SELECT`, `WHERE`, `ORDER BY`
- Aggregate functions: `COUNT()`, `SUM()`
- `GROUP BY`
- `INNER JOIN`
- Filtering with `IN`
- Date functions: `MONTH()`, `MONTHNAME()`
- Calculated revenue using `Quantity * Price`

## Verified Results

### Order status
| Order Status | Orders |
|---|---:|
| Delivered | 15 |
| Pending | 3 |
| Cancelled | 2 |
| **Total** | **20** |

### Delivered revenue by month
| Month | Delivered Revenue |
|---|---:|
| May 2026 | ₹1,07,500 |
| June 2026 | ₹1,48,100 |
| **Total** | **₹2,55,600** |

June's delivered revenue was **₹40,600 higher** than May's.

### Delivered revenue by product
| Product | Delivered Revenue |
|---|---:|
| Laptop | ₹1,10,000 |
| Smartphone | ₹90,000 |
| Office Chair | ₹22,500 |
| Monitor | ₹12,000 |
| Desk | ₹9,500 |
| Keyboard | ₹6,000 |
| Mouse | ₹5,600 |
| **Total** | **₹2,55,600** |

### Delivered revenue by city
| City | Delivered Revenue |
|---|---:|
| Bhopal | ₹1,07,500 |
| Indore | ₹56,600 |
| Delhi | ₹52,000 |
| Mumbai | ₹30,000 |
| Pune | ₹9,500 |
| **Total** | **₹2,55,600** |

### Delivered revenue by customer
| Customer | Delivered Revenue |
|---|---:|
| Rahul Sharma | ₹86,500 |
| Sneha Gupta | ₹55,000 |
| Amit Patel | ₹34,600 |
| Neha Singh | ₹30,000 |
| Karan Mehta | ₹21,000 |
| Pooja Das | ₹17,400 |
| Arjun Jain | ₹9,500 |
| Priya Verma | ₹1,600 |
| **Total** | **₹2,55,600** |

## Business Insights and Recommendations
1. **Product performance:** Laptops generated the highest delivered revenue at ₹1,10,000, followed by smartphones at ₹90,000. Together they contributed ₹2,00,000 of delivered revenue.
2. **City performance:** Bhopal generated the highest delivered revenue at ₹1,07,500. The business could examine which products are driving its performance.
3. **Customer performance:** Rahul Sharma generated the highest delivered revenue at ₹86,500. The business could review repeat-purchase patterns before designing retention offers.
4. **Monthly performance:** June delivered revenue was ₹40,600 higher than May. Smartphone revenue rose from ₹30,000 in May to ₹60,000 in June, while office-chair revenue also increased.
5. **Order follow-up:** There are 3 pending orders and 2 cancelled orders. The manager could investigate pending orders and review cancellation reasons.

These results describe the sample dataset. They do not, by themselves, establish why customer or city performance differs.

## Tools
- MySQL
- MySQL Workbench

## Project Files
- `ShopSmart_SQL_Analysis.sql` — SQL queries used for the analysis.
- `README.md` — project overview, methods, verified findings, and recommendations.

## Screenshots

### Order status
![Order status](https://github.com/Chaurasiya16/ShopSmart_SQL_Analysis/blob/main/order_status.png)

### Delivered revenue by month
![Delivered revenue by month](https://github.com/Chaurasiya16/ShopSmart_SQL_Analysis/blob/main/monthly_revenue.png)

### Delivered revenue by product
![Delivered revenue by product](https://github.com/Chaurasiya16/ShopSmart_SQL_Analysis/blob/main/product_revenue.png)

### Delivered revenue by city
![Delivered revenue by city](https://github.com/Chaurasiya16/ShopSmart_SQL_Analysis/blob/main/city_revenue.png)

### Delivered revenue by customer
![Delivered revenue by customer](https://github.com/Chaurasiya16/ShopSmart_SQL_Analysis/blob/main/customer_revenue.png)

## How to Run
1. Install MySQL and MySQL Workbench.
2. Open `ShopSmart_SQL_Analysis.sql` in MySQL Workbench.
3. Run the script from top to bottom. It creates the `ShopSmart` database, the three tables, and the sample data, and then runs the analysis queries.
4. Compare the query results with the tables in this README.

## Notes and Limitations
- This is a fictional practice dataset with 8 customers, 8 products, and 20 orders.
- Revenue is calculated as `Quantity * Price` and includes only orders with status `Delivered` in the analyses above.
- Revenue is not profit because product costs and operating expenses are not included.
- Findings apply only to this sample dataset and should not be generalized to a real business.
