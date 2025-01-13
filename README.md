# CODETECH-TASK-1
### Dataset Overview<br/>
The supermarket or online retail store, containing information about orders, products, departments, and aisles. Here’s a breakdown of the individual datasets used in task

**1. aisles.csv:**
Contains information about different aisles in the store. An aisle refers to a specific category or section of the store where products are grouped.
Columns may include: aisle_id, aisle.
**2. departments.csv:**
Contains information about store departments. Each department contains multiple aisles and holds a category of products.
Columns may include: department_id, department.
**3. order_products__train.csv:**
Contains the relationship between orders and products. Specifically, which products were bought in each order.
Columns include: order_id, product_id, and additional columns like add_to_cart_order, reordered, which indicate whether a product was added to the cart and whether it was reordered.
**4. orders.csv:**
Contains information about orders made by customers.
Columns include: order_id, user_id, eval_set (which indicates whether the order is part of training or evaluation), order_status, order_date, order_hour_of_day, and other temporal data.
**5. products.csv:**
Contains information about products sold in the store.
Columns include: product_id, product_name, aisle_id, department_id, and other product attributes.
