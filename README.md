## Project Overview  
**Corporate_Travel_Analytics** is a sophisticated Data Warehouse solution engineered to transform raw corporate travel data into high-level business intelligence. Developed in SQL Server, this project showcases a transition from standard flat modeling to a fully normalized Snowflake Schema.  

By optimizing the data architecture for Power BI, this repository demonstrates how to build a "Single Source of Truth" that supports complex hierarchical drill-downs and enterprise-scale reporting.  

---

## Data Architecture & Design  
This project highlights the technical evolution of a data model to meet modern analytical demands.  

### Dimensional Evolution:  
- **Phase 1**: Initial Star Schema designed for rapid OLAP querying.  
- **Phase 2**: Refined into a Snowflake Schema (3rd Normal Form) to eliminate data redundancy and manage complex hierarchies.  

**Database Engine**: SQL Server (T-SQL).  
**Data Strategy**: Engineered synthetic datasets that mirror real-world corporate travel workflows.  
**BI Layer**: Power BI semantic modeling using advanced DAX.  

---

## Schema & Tables (Corporate_Travel_Analytics)  

**Clients**  
- Client_ID  
- Client_Name  
- Industry  
- Account_Manager  

**Employees**  
- Employee_ID  
- Employee_Name  
- Department  
- Title  
- Region  

**Trips**  
- Trip_ID  
- Booking_Date  
- Travel_Date  
- Employee_ID  
- Client_ID  
- Vendor_ID  
- Travel_Type  
- Origin  
- Destination  
- Cost  
- Currency  
- Booking_Channel  

**Relationships**:  
- **Clients → Trips** via Client_ID  
- **Employees → Trips** via Employee_ID  

---

## Key Technical Features  
- **Advanced SQL Engineering**: Implementation of CTEs, Window Functions, and stored procedures for deep-dive analytics.  
- **Normalized Travel Hierarchy**: Granular mapping of trip details across employees, clients, and vendors.  
- **Unified Geography Model**: Shared dimensions for trip origins and destinations via city ➔ region normalization.  
- **Time Intelligence**: A robust Dim_Date dimension enabling YoY (Year-over-Year) and MTD (Month-to-Date) tracking.  
- **Data Integrity**: Enforced Referential Integrity through strict PK/FK constraint management.  

---

## Power BI Dashboards  
- **Executive KPI Tracker**: Real-time visibility into Travel Spend, Average Trip Cost, and Vendor Utilization.  
- **Regional Travel Analysis**: Geospatial insights into employee travel patterns across different territories.  
- **Client Engagement Intelligence**: Client-level travel spend and booking trends.  
- **Employee Travel Segmentation**: Behavioral trends based on department, title, and region.  

---

## File Structure  
- **Schema/** – SQL scripts to create and optimize tables, indexes, relationships  
- **Queries/** – Advanced SQL query scripts grouped by scenario or concept  
- **Data/** – Sample data insert scripts (insert_sample_data.sql)  
- **Indexes/** – Scripts for creating and maintaining database indexes to improve query performance  
- **Stored_Procedures/** – Parameterized SQL scripts encapsulating business logic for reusable operations  
- **Views/** – Predefined SQL views for simplified reporting and analytics  
- **Docs/** – Contains Corporate_Travel_Analytics_ERD.jpg (ER diagram)  
- **README.md** – Project overview and instructions  

---

## Bash  
```bash
git clone https://github.com/kajagopalas/Corporate_Travel_Analytics
```

---

## Deploy Database  
1. Run scripts in `/Schema` using SQL Server Management Studio (SSMS).  
2. Execute `Populate_Data.sql` to load the synthetic corporate travel dataset.  
3. Launch Analytics:  
   - Open the `.pbix` file in Power BI Desktop.  
   - Update Data Source Settings to link to your local SQL Server instance.  

---

## Technologies Used  
- **SQL Server**: Architecture, T-SQL Development, and Normalization.  
- **Power BI**: DAX Measures, Semantic Modeling, and Data Viz.  
- **Git**: Version Control and Documentation.  

---

## Contributions & License  
This is an Open Source learning resource.  

- **License**: MIT — Free to use, modify, and share.  
- **Contribute**: Fork the repo, add new analytical scenarios, and submit a PR!  

---

✅ Now the entire documentation consistently uses **Corporate_Travel_Analytics** and aligns with the schema from your diagram.  

Would you like me to also generate **SQL DDL scripts** for `Clients`, `Employees`, and `Trips` so you can deploy the schema directly in SQL Server?
