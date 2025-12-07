# Customer-Behavior-Purchase-Analysis
End-to-End Data Analytics Project using Python, SQL &amp; Power BI

**Key Features**

1. Data Cleaning & Feature Engineering (Python)
	1) Handled missing values and standardized 18+ columns
	2) Engineered:
		1) DiscountFlag, IsRepeat, PromoFlag
		2) age_group (quartile binning)
		3)freq_per_month, avg_review_rating, customer-level aggregates
	3) Exported cleaned & enriched files:
		1) edited_telco.csv
		2) cleaned_transactions.csv
		3) customer_segments.csv
		4) product_association_rules.csv

2. Customer Segmentation (KMeans)
	1) Segmentation on:
		1) Total spend
		2) Avg order value
		3) Number of transactions
		4) Previous purchases
		5) Frequency per month
		6)Avg review rating
	2) Selected k = 4 segments, providing:
		1) High-value cluster
		2) Loyalty-driven cluster
		3) Low-volume casual buyers
		4) Discount-sensitive shoppers

3. Market Basket Analysis (Apriori)
  Generated association rules from product combinations to identify cross-sell opportunities such as:
	1) Customers buying Blouse often buy Jewelry
	2) Pants → Belt
	3) Seasonal apparel → Accessories
  Exported to product_association_rules.csv.

4. PostgreSQL Database Layer
Created table telco_customers3 and loaded enriched dataset via SQLAlchemy.
SQL Components
	1) Optimized Indexes
	2) Dimension tables:
		1) dim_category, dim_location, dim_segment, dim_payment_method
	3) Analytical Views:
		1) vw_kpis_telco
		2) vw_revenue_by_location_category_segment
		3) vw_top_items
		4) vw_payment_distribution
		5) vw_top_items_by_category
	4) Materialized View:
		1) mv_revenue_by_location (for fast Power BI queries)

Enables seamless data refresh and BI integration.

5. Power BI Dashboard (Fully Interactive)
The dashboard includes:
	1) KPI cards
		1) Revenue
		2) Unique customers
		3) Avg order value
		4) Review rating

	2) Filters & Buttons
		1) Category, Age group, Segment, Location, Payment method
	3) Interactive Visuals
		1) Revenue by Location
		2) Revenue by Category
		3) Customer Segmentation Scatter Plot
		4) Top Products (Dynamic Top-N)
		5) Payment Method Distribution
		6) Product Recommendation Patterns (Association Rules)

Everything is interactive & supports drill-through.

6. Project Architecture:
	
	Python (Data Processing + Modeling) -> PostgreSQL (Structured Storage + Views/Indexes) -> Power BI (Visualization + Reporting)

7. Business Impact
This project helps optimize:
	1) Targeted marketing campaigns
	2) Product bundling strategies
	3) Customer retention initiatives
	4) Inventory planning
	5) Review rating improvements
