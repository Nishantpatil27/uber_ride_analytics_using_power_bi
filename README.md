# Uber_ride_analytics_using_power_bi 🚚
---

## 📌 Project Overview
In order to identify **operational performance** and **behaviour patterns**, this dashboard examines **ride trends**, **revenue**, **cancellations**, and **user experience** across all **Uber reservations**.  
In order to **optimise platform efficiency** and **customer satisfaction**, it delivers **actionable insights** on **ride completion**, **demand patterns**, **payment usage**, and **rating trends**.

---

## 🔑 Key Features
**⭐ End-to-End Ride Funnel Tracking :–** evaluates operational efficiency by counting the number of reservations, rides that are completed, cancelled, and unfinished.<br>

**⭐ Cancellation Root-Cause Intelligence :–** Segments customer vs driver cancellations and identifies top cancellation reasons and high-risk routes.<br>

**⭐ Revenue & Utilization Performance :–** uses revenue-per-kilometer metrics to analyse fare trends by vehicle type, payment method, location, and trip distance.<br>

**⭐ Location-Based Ride Behavior Mapping :–** Highlights top pickup and drop zones, demand hotspots, and location-wise cancellation spikes.<br>

**⭐ Customer & Driver Experience Scoring :–** identifies low-rating ride factors, tracks rating trends, and identifies areas for service experience enhancement.<br>



# 🛠️ Setup 
---

### **Step 1: Prepare CSV Files**

* Make sure all your CSV files (orders, customers, restaurants, menu, reviews, etc.) are download
* Keep them all in a single folder for quick access



### **Step 2: Create a Database**

1. Open your SQL tool (e.g., **MySQL Workbench** or **SQL Server Management Studio**).
2. Create a new database:

```sql
create database zomato;
```

---

### **Step 3: Import CSV into Tables**

1. Right-click on the **database** in the left panel.<br> <br><img width="1915" height="707" alt="image" src="https://github.com/user-attachments/assets/ada48464-b9ac-4dcb-8a42-e70f65064e39" />
2. Select **Table Data Import Wizard** (or similar option depending on your tool).<br><br> <img width="1918" height="730" alt="image" src="https://github.com/user-attachments/assets/ce50a37e-1a52-4ee3-ab06-67a6d8e9982f" />

3. Browse and select the CSV file you want to import.<br><br><img width="1918" height="901" alt="image" src="https://github.com/user-attachments/assets/7caf521f-8d1d-45bb-84de-2e9daaed6bfd" />

4. Follow the wizard to create the table and map columns correctly and all next next click and then click finish.<img width="1919" height="786" alt="image" src="https://github.com/user-attachments/assets/f62267cd-9e20-45bf-bf65-19fde27fa7ad" />


---

### **Step 4: Repeat for All CSVs**

* Repeat **Step 3** for each CSV file (customers, orders, menu, reviews, delivery partners, etc.) until all data is imported.

---

### ✅ **Step 5: Verify Data**

* Run a simple query to check the data is imported correctly:

```sql
SELECT * FROM orders;
SELECT * FROM customers;
```
---

 
