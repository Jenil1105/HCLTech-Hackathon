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

┌──────────────────────┐                     
│        INPUT         │ 
│  Sales CSV Files     │
│  (Header & Line)     │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│       PROCESS        │
│ • Load into RAW      │
│ • Validate data      │
│ • Apply rules        │
└──────────┬───────────┘
           ↓
┌──────────────────────┐
│        OUTPUT        │
│ • Clean Staging Data │
└──────────────────────┘ 
      Task 1
