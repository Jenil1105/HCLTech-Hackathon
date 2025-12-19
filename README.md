##################### OVEARLL FLOW #####################

CSV Files ->Raw Data Ingestion ->Raw Data Ingestion ->Data Validation ->Clean Staging Data ->Analytics & Business Logic ->Customer Actions & Insights
 
-------------------------------------------------------------------------------------------------------------------------
##  Inputs
- Synthetic CSV files generated as per provided schemas

##  Outputs
- Clean staging tables
- Promotion performance rankings
- Updated customer loyalty balances
- Customer segments and notifications
- Inventory performance insights



---

## Data Inputs

Synthetic datasets generated as per the provided schemas:

- store_sales_header.csv  
- store_sales_line_items.csv  
- products.csv  
- stores.csv  
- promotion_details.csv  
- customer_details.csv  
- loyalty_rules.csv  
- store_inventory.csv  

---

##  Core Table Relationships

- **store_sales_header** → one row per transaction (linked to customers)
- **store_sales_line_items** → multiple products per transaction
- **promotion_details** → promotions applied at product level
- **customer_details** → customer info and loyalty balance
- **loyalty_rules** → rules for point calculation
- **store_inventory** → daily product stock per store

---

##  Task-wise Workflow (Input → Process → Output)

 





%3



S

SOURCE
Unstructured / Semi-Structured Data
(CSV Files)



R

RAW LAYER
As-Is Data Storage
(No Validation)



S->R





P

PROCESS
• Load to RAW tables
• Apply data quality rules
• Validate & filter records



R->P





O

OUTPUT
• Clean Staging Tables
• Ready for Analytics



P->O





