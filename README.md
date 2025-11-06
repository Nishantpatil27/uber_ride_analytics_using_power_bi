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

* Make sure your CSV files (ncr_ride_bookings) are download
* Keep them all in a single folder for quick access


---
### **Step 2: Create a Power Bi Report/Dashborad File**

1. Open your power bi tool.
2. Create a new Report/Dashborad File:


---

### **Step 3: Import CSV into File**

1. **Open the PBIX file** and then **click get data** then **select "text/csv"**.<br> <br> <img width="1920" height="1020" alt="Screenshot 2025-11-06 141712" src="https://github.com/user-attachments/assets/d144ce66-8c32-4495-a6da-78304d25ce51" />

2. **Select Your CSV/text file** (ncr_ride_bookings.csv).<br><br> <img width="908" height="592" alt="Screenshot 2025-11-06 141739" src="https://github.com/user-attachments/assets/86b3abc5-e063-4784-a2e0-ffd399ec61a0" />


3. **Click Transfrom data**.<br><br><img width="1102" height="827" alt="Screenshot 2025-11-06 141805" src="https://github.com/user-attachments/assets/215cde7e-bb4e-4d5e-aead-d3f5e0634315" />


4. **Replace null values** in the columns **Cancelled Rides by Customer, Cancelled Rides by Driver, and Incomplete Rides with** **‘No’**, and convert the **value 1 to ‘Yes’**.

---

### **Step 4: Repeat for All CSVs**

* Important measures will also be added.
```
Avg Revenue = AVERAGE(ncr_ride_bookings[Booking Value])
```
```
Avg_customer_rating = AVERAGE(ncr_ride_bookings[Customer Rating])
```
```
Avg_driving_rating = AVERAGE(ncr_ride_bookings[Driver Ratings])
```
```
cancellation rating = ([Cancelled Rides]/([Cancelled Rides]+[Total Completed Rides]))
```
```
Cancelled Rides = CALCULATE(CALCULATE(COUNT(ncr_ride_bookings[Booking ID]),FILTER(ncr_ride_bookings,OR(ncr_ride_bookings[Cancelled Rides by Customer] = "yes",ncr_ride_bookings[Cancelled Rides by Driver]="yes"))))
```
```
Total Completed Rides = CALCULATE(COUNT(ncr_ride_bookings[Booking Status]),FILTER(ncr_ride_bookings,ncr_ride_bookings[Booking Status] = "Completed"))
```
```
Total_booking = COUNT(ncr_ride_bookings[Booking ID])
```
```
total_revenue = SUM(ncr_ride_bookings[Booking Value])
```
---

### ✅ These steps apply only when using a new Power BI file. If you are using the project.pbit file, then these steps are not required.

---

 ---

## 📌 Dashborad & Report Overview
<img width="1920" height="1020" alt="Screenshot 2025-11-06 145404" src="https://github.com/user-attachments/assets/aa992805-c6e0-4cea-b9c3-5acfe03cd718" />

<img width="1920" height="1020" alt="Screenshot 2025-11-06 145417" src="https://github.com/user-attachments/assets/e6eac881-45c5-4580-8385-f9bac805e83a" />

<img width="1920" height="1020" alt="Screenshot 2025-11-06 145427" src="https://github.com/user-attachments/assets/83341d17-536f-4578-b3fb-4288678c79ab" />

<img width="1920" height="1020" alt="Screenshot 2025-11-06 145440" src="https://github.com/user-attachments/assets/4491cb23-6ffe-4a04-9481-302d6cff6693" />

---
