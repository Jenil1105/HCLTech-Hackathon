##################### OVEARLL FLOW #####################

CSV Files
  ↓
Raw Data Ingestion
  ↓
Data Validation
  ↓
Clean Staging Data
  ↓
Analytics & Business Logic
  ↓
Customer Actions & Insights
-------------------------------------------------------------------------------------------------------------------------
##  Inputs
- Synthetic CSV files generated as per provided schemas

##  Outputs
- Clean staging tables
- Promotion performance rankings
- Updated customer loyalty balances
- Customer segments and notifications
- Inventory performance insights

########################## Data Input #####################

Generating data based on the given schemas.

1)store_sales_header.csv

2)store_sales_line_items.csv

3)products.csv

4)stores.csv

5)promotion_details.csv

6)customer_details.csv

7)loyalty_rules.csv

8)store_inventory.csv

################# Table Relationships ################ 

->store_sales_header

  . Linked to customer_details via customer_id

  . Represents one transaction per bill

->store_sales_line_items

  . Linked to store_sales_header via transaction_id

  . Linked to products via product_id

  . Contains individual product-level sales

->promotion_details

  . Linked to store_sales_line_items via promotion_id

  . Used to analyze promotion effectiveness

->customer_details

  . Stores customer info and loyalty balance

  . Updated by loyalty calculation logic

->loyalty_rules

  . Defines how points are calculated per transaction

->store_inventory

  . Linked to products and stores

  . Used to analyze out-of-stock impact
