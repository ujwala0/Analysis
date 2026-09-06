# 🛒 E-Commerce Sales & Customer Experience Analysis

## 📌 Project Overview

This project analyzes an e-commerce marketplace dataset to understand **sales performance, customer satisfaction, delivery performance, payment behavior, product categories, states, and seller performance**.

The analysis combines multiple datasets into a master dataset and uses Python, Pandas, Matplotlib, and data analysis techniques to identify important business trends and provide actionable recommendations.

---

## 🎯 Business Objectives

The main objectives of this project are to:

* Analyze overall sales and revenue performance
* Understand monthly order and revenue trends
* Measure delivery performance and late-delivery rates
* Analyze the relationship between delivery performance and customer reviews
* Identify high- and low-performing product categories
* Compare performance across customer states
* Analyze payment methods and installment behavior
* Identify high- and low-performing sellers
* Understand factors associated with customer satisfaction
* Provide actionable business recommendations

---

## 📂 Datasets Used

The project uses 9 related datasets:

| Dataset                | Description                               |
| ---------------------- | ----------------------------------------- |
| `orders`               | Order information and order status        |
| `order_items`          | Products purchased in each order          |
| `order_payments`       | Payment methods, values, and installments |
| `order_reviews`        | Customer review scores                    |
| `customers`            | Customer location and information         |
| `products`             | Product information and categories        |
| `sellers`              | Seller information                        |
| `geolocation`          | Geographic information                    |
| `category_translation` | Product category translations             |

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Matplotlib**
* **Jupyter Notebook / Google Colab**
* Data Cleaning
* Data Aggregation
* Exploratory Data Analysis (EDA)
* Data Visualization
* Business Analytics

---

## 🔄 Project Workflow

### 1. Data Loading

All 9 datasets were loaded from the Excel workbook and their available sheets were verified.

### 2. Data Understanding

The datasets were examined for:

* Number of rows and columns
* Missing values
* Duplicate records
* Order-status distribution
* Data types
* Key relationships between datasets

### 3. Data Cleaning

The analysis included:

* Checking duplicate rows
* Handling missing values
* Converting date columns
* Aggregating order items
* Aggregating payment information
* Handling multiple review records
* Ensuring one unique record per order in the master dataset

The final master dataset contains:

**99,441 unique orders**

### 4. Master Dataset Creation

Multiple datasets were joined to create a comprehensive order-level dataset containing:

* Order information
* Customer information
* Product/item metrics
* Payment metrics
* Review scores
* Delivery information
* Revenue and freight metrics

Final master dataset:

**99,441 rows × 21 columns**

---

# 📊 Key Business Metrics

| KPI                  |         Result |
| -------------------- | -------------: |
| Total Orders         |         99,441 |
| Total Revenue        | ₹13,591,643.70 |
| Average Order Value  |        ₹137.75 |
| Average Review Score |           4.07 |
| Late Delivery Rate   |            ~8% |
| Total Customers      |         99,441 |
| Total Sellers        |          3,095 |

---

# 📈 Key Analysis

## 1. Marketplace Trends

The analysis examined monthly:

* Order volume
* Revenue
* Average review score
* Average order value

### Best Month

**November 2017**

* Orders: **7,544**
* Revenue: **₹1,010,271.37**
* Average Order Value: **₹133.92**

This month recorded both the highest order volume and highest revenue in the analysis.

---

## 2. Delivery Performance

Delivery performance was one of the strongest areas of analysis.

### Delivery vs Customer Satisfaction

| Delivery Status | Average Review |
| --------------- | -------------: |
| Early           |           4.28 |
| Late            |           2.55 |

Late deliveries are associated with substantially lower customer review scores.

The review distribution also shows that late deliveries generate a much higher proportion of low ratings.

### Business Insight

Improving delivery reliability is likely to have a significant impact on customer satisfaction.

---

## 3. Freight Analysis

Orders were divided into freight groups based on freight cost.

The highest freight group had:

* Average freight: **45.44**
* Late-delivery rate: **9.25%**
* Average review: **3.93**

Compared with lower freight groups, expensive freight orders showed higher late-delivery rates and lower customer satisfaction.

### Business Insight

High-freight orders should be investigated for:

* Shipping routes
* Logistics partners
* Regional delivery costs
* Freight pricing
* Delivery efficiency

---

# 🛍️ 4. Product Category Analysis

### Top Categories by Revenue

| Category                |       Revenue |
| ----------------------- | ------------: |
| Health & Beauty         | ₹1,258,681.34 |
| Watches & Gifts         | ₹1,205,005.68 |
| Bed/Bath/Table          | ₹1,036,988.68 |
| Sports & Leisure        |   ₹988,048.97 |
| Computers & Accessories |   ₹911,954.32 |

### Lowest-Rated Category

**Office Furniture**

Average review score:

**3.48**

### Highest-Rated Categories

Some of the highest-rated categories include:

* Books – General Interest: **4.44**
* Books – Technical: **4.33**
* Luggage & Accessories: **4.31**
* Food & Drink: **4.30**
* Fashion Shoes: **4.20**

---

# 🌎 5. State Performance

Customer states were analyzed using:

* Number of orders
* Average review score
* Late-delivery rate
* Average freight
* Average order value

### States with High Late-Delivery Rates

| State | Late Rate |
| ----- | --------: |
| AL    |    23.93% |
| MA    |    19.67% |
| PI    |    15.97% |
| CE    |    15.32% |
| SE    |    15.22% |

### Business Insight

These regions should receive additional investigation into:

* Delivery infrastructure
* Shipping routes
* Logistics partners
* Distance from sellers
* Freight costs

---

# 💳 6. Payment Analysis

The most common payment methods were:

| Payment Type          | Orders |
| --------------------- | -----: |
| Credit Card           | 74,259 |
| Boleto                | 19,784 |
| Credit Card + Voucher |  2,245 |
| Voucher               |  1,621 |
| Debit Card            |  1,527 |

### Payment Performance

Credit-card orders represented the largest payment segment and had an average payment value of approximately **₹163.32**.

---

# 💰 7. Installment Analysis

The analysis examined:

* Number of installments
* Average order value
* Average review score
* Late-delivery rate

Higher installment counts generally corresponded with higher average order values, although some high-installment groups had relatively few orders and should therefore be interpreted cautiously.

---

# ⭐ 8. Review Group Analysis

Orders were divided into three customer-satisfaction groups:

| Review Group | Orders | Avg Review | Late Rate |
| ------------ | -----: | ---------: | --------: |
| Low (1–2)    | 14,963 |       1.21 |    28.54% |
| Medium (3)   |  8,241 |       3.00 |    10.75% |
| High (4–5)   | 76,173 |       4.75 |     3.49% |

### Key Finding

There is a strong relationship between delivery performance and customer satisfaction.

Orders receiving low reviews have a much higher late-delivery rate than orders receiving high reviews.

---

# 🏪 9. Seller Performance

Sellers were evaluated using:

* Number of orders
* Review scores
* Late-delivery rates
* Revenue
* Freight

The analysis identified both high-performing and low-performing sellers.

### Business Insight

Seller performance should not be evaluated using review score alone.

A better seller-performance framework should combine:

**Customer Satisfaction + Delivery Reliability + Revenue**

---

# 💡 Business Recommendations

## 1. Improve Delivery Performance

Late deliveries have a strong negative relationship with customer reviews.

**Recommendation:**
Prioritize reducing delivery delays, especially in regions with high late-delivery rates.

---

## 2. Investigate High-Freight Orders

High-freight orders show higher late-delivery rates.

**Recommendation:**
Review shipping routes, logistics providers, freight pricing, and regional distribution.

---

## 3. Invest in High-Revenue Categories

Health & Beauty, Watches & Gifts, and Bed/Bath/Table are among the strongest revenue-generating categories.

**Recommendation:**
Maintain inventory availability and targeted marketing for high-performing categories.

---

## 4. Improve Low-Rated Categories

Office Furniture has the lowest average review among categories with sufficient order volume.

**Recommendation:**
Investigate:

* Product quality
* Seller performance
* Delivery delays
* Product descriptions
* Customer expectations

---

## 5. Monitor High-Risk States

States such as AL, MA, PI, CE, and SE have relatively high late-delivery rates.

**Recommendation:**
Develop regional logistics strategies to improve delivery reliability.

---

## 6. Monitor Seller Quality

Some sellers have substantially lower customer ratings.

**Recommendation:**
Create a seller-performance monitoring system based on:

* Review score
* Late-delivery rate
* Order volume
* Revenue
* Freight performance

---

# 📊 Dashboard

The project includes dashboard charts covering:

* Marketplace trends
* Revenue and order performance
* Product category performance
* State performance
* Delivery performance
* Freight analysis
* Payment performance
* Installment performance
* Seller performance
* Review-group performance

---

# 🏁 Final Conclusion

The analysis shows that the marketplace performs strongly overall, with approximately **99K orders**, more than **₹13.5M in revenue**, and an overall customer review score above **4.0**.

The most important business issue identified is **delivery performance**.

Orders delivered late receive substantially lower customer ratings than orders delivered early. High-freight orders and certain geographic regions also show higher delivery risk.

Therefore, the biggest opportunity for the marketplace is to improve **logistics reliability while maintaining investment in high-performing categories and sellers**.

---

## 📌 Project Outcome

This project demonstrates an end-to-end data analytics workflow:

**Raw Data → Data Cleaning → Data Integration → Exploratory Analysis → Visualization → Business Insights → Recommendations**

It can be used as a portfolio project to demonstrate practical skills in **Python, Pandas, data analysis, visualization, and business intelligence**.
