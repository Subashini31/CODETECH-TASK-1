# CODETECH-TASK-1
### Dataset Overview<br/>
The supermarket or online retail store, containing information about orders, products, departments, and aisles. Here’s a breakdown of the individual datasets used in task

**1. Aisles.csv:** <br/>
Contains information about different aisles in the store. An aisle refers to a specific category or section of the store where products are grouped.<br/>
Columns include: aisle_id, aisle.<br/>
**2. Departments.csv:** <br/>
Contains information about store departments. Each department contains multiple aisles and holds a category of products.<br/>
Columns include: department_id, department.<br/>
**3. Order_products__train.csv:** <br/>
Contains the relationship between orders and products. Specifically, which products were bought in each order.<br/>
Columns include: order_id, product_id, and additional columns like add_to_cart_order, reordered, which indicate whether a product was added to the cart and whether it was reordered. <br/>
**4. Orders.csv:** <br/>
Contains information about orders made by customers.
Columns include: order_id, user_id, eval_set (which indicates whether the order is part of training or evaluation), order_status, order_date, order_hour_of_day, and other temporal data.<br/>
**5. Products.csv:** <br/>
Contains information about products sold in the store.<br/>
Columns include: product_id, product_name, aisle_id, department_id, and other product attributes.<br/>

### ETL (Extract, Transform, Load) Process Explanation using Supermarket dataset

**1. Extract:** <br/>
**Purpose:** This is the first stage where raw data is extracted from various sources (e.g., CSV files, CSV, Excel, TSV, JSON, XML, etc). <br/>
**Process:**  <br/>
In the ETL pipeline, the pandas.read_csv() function is used to load the data from CSV files. For each dataset (aisles.csv, departments.csv, order_products_train.csv, orders.csv, products.csv), the data is read into pandas DataFrames. <br/>

**2. Transform:**  <br/>

**Purpose:** The raw data is cleaned, modified, and transformed into a more usable format for analysis. This includes handling missing values, encoding categorical variables, and aggregating data. <br/>
**Process:**  <br/>
**Missing Value Imputation:** Numerical columns with missing values are filled using mean or other strategies (SimpleImputer). <br/>
**Categorical Encoding:** Categorical variables are encoded into numerical values using techniques like LabelEncoder. <br/>
**Data Merging:** The datasets are merged into a single DataFrame. This is done using pd.merge() to join the data on common columns like order_id or product_id. <br/>
**Grouping and Aggregating:** For example, all the products bought in a particular order are grouped together. This is done by grouping data by order_id and concatenating the product IDs into a single string.  <br/>

**3.Load:** <br/>

**Purpose:** Once the data is transformed and cleaned, it is ready to be loaded for further use, like machine learning models, analysis, or visualization. <br/>
**Process:** In this case, instead of loading data into a database, output is  display the transformed data directly in the notebook. <br/>
The display() function from IPython is used to show the grouped data, where each row represents an order, and the corresponding products are shown as a space-separated string. <br/>

**This process ensures that data is in the right format, cleaned, and ready for decision-making or machine learning tasks.**

