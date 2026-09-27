SELECT category, sub_category, ROUND(SUM(profit),2) AS total_profit
FROM orders
GROUP BY category, sub_category
ORDER BY total_profit ASC
LIMIT 10;


SELECT DATE_FORMAT(order_date, '%Y-%m') AS month, ROUND(SUM(sales),2) AS monthly_sales
FROM orders
GROUP BY month
ORDER BY month;


SELECT region, 
       CONCAT('$', FORMAT(SUM(sales),2)) AS total_sales, 
       CONCAT('$', FORMAT(SUM(profit),2)) AS total_profit
FROM orders
GROUP BY region
ORDER BY SUM(sales) DESC;


SELECT product_name, SUM(quantity) AS units_sold, ROUND(SUM(sales),2) AS total_sales
FROM orders
GROUP BY product_name
ORDER BY total_sales DESC
LIMIT 10;
