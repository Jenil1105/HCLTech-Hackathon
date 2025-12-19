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



---

## 🗂️ Data Inputs

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

## 🔗 Core Table Relationships

- **store_sales_header** → one row per transaction (linked to customers)
- **store_sales_line_items** → multiple products per transaction
- **promotion_details** → promotions applied at product level
- **customer_details** → customer info and loyalty balance
- **loyalty_rules** → rules for point calculation
- **store_inventory** → daily product stock per store

---

## 🧩 Task-wise Workflow (Input → Process → Output)

### Task 1: Data Ingestion & Quality Validation
- **Input:** Raw sales CSV files  
- **Process:** Load into raw tables, apply data quality rules  
- **Output:** Clean staging tables and quarantine records  

---

### Task 2: Promotion Effectiveness Analysis
- **Input:** Clean sales data, promotion details  
- **Process:** Compare promoted vs non-promoted sales  
- **Output:** Ranked promotions with sales uplift percentage  

---

### Task 3: Loyalty Point Calculation
- **Input:** Transaction totals, loyalty rules, customer data  
- **Process:** Calculate earned points and update balances  
- **Output:** Updated customer loyalty point balances  

---

### Task 4: Customer Segmentation
- **Input:** Sales history, loyalty balances  
- **Process:** Compute RFM metrics and segment customers  
- **Output:** High-Value and At-Risk customer groups  

---

### Task 5: Loyalty Notification System
- **Input:** Updated loyalty balances, customer emails  
- **Process:** Generate personalized reward notifications  
- **Output:** Simulated email logs  

---

### Task 6: Inventory & Store Performance Analysis
- **Input:** Sales data, inventory levels  
- **Process:** Identify stock-outs and estimate lost sales  
- **Output:** Inventory performance and lost revenue insights  

---

## 📊 Flow Diagrams

Task-wise Input → Process → Output flowcharts are created using **Python (Graphviz)** and are available in the Jupyter Notebook:

👉 `Retail_Data_Pipeline_Flow.ipynb`

---

## 🛠️ Tech Stack

- Python (Data generation & processing)
- SQL (Validation & analytics)
- Pandas
- SQLite / PostgreSQL
- Jupyter Notebook

---

## ⚠️ Assumptions & Limitations

- Data is synthetically generated for demonstration purposes  
- Email notifications are simulated (no real emails sent)  
- Inventory loss is an estimated metric  

---

## 📄 Detailed Documentation

Detailed explanation, assumptions, and implementation notes are available here:  
👉 *Google Docs link*

---

### ⭐ Key Takeaway

This project focuses on building a **reliable, explainable data pipeline** rather than isolated ML models.

