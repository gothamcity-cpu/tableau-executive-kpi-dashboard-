# 🚗⚡ Electric Vehicle Population Analytics Dashboard (Tableau)

This project analyzes Washington State’s Electric Vehicle (EV) adoption using a rich dataset of registered vehicles. The Tableau dashboard visualizes geographic distribution, EV types, model trends, electric range performance, and clean-fuel eligibility to support insights for sustainability teams, policymakers, and EV infrastructure planning.

🔗 **Live Dashboard**  
(https://public.tableau.com/app/profile/goutham.thatipamula/viz/Book1_v2025_1_17646036077060/Dashboard1)

---

## 📘 1. Project Overview

Electric vehicles continue to expand rapidly across the U.S., and this dashboard provides an interactive lens into Washington State’s EV landscape.

The goal of the project is to transform raw state registration data into a powerful, intuitive visual analytics experience that allows users to:

- Explore EV adoption by **county, city, and census tract**
- Compare **BEV vs PHEV** penetration
- Identify top **EV makes and models**
- Understand **electric range trends** across vehicles
- Analyze **CAFV incentive eligibility**
- Investigate geographic EV clustering powered by actual coordinates
- View utility service areas tied to EV registrations

This dashboard showcases skills in **data preparation, geospatial analysis, Tableau design, KPI storytelling, and domain understanding** within transportation and clean-energy analytics.

---

## 🔍 2. Dataset Details

**Dataset:** `Electric_Vehicle_Population_Data.xlsx`  
**Source:** Washington State (EV Registration Data)  
**Grain:** Each row = one registered electric vehicle.  
**Rows:** ~ X,XXX  

The dataset includes:

- Vehicle characteristics (make, model, year, range)
- Vehicle type (BEV or PHEV)
- Geographic location (county, city, zip, geo coordinates)
- Electric utility provider
- Clean vehicle incentive eligibility (CAFV)
- Census tract information

For full field descriptions, see the **Data Dictionary** included below.

---

## 📊 3. Dashboard Features

### **✔ Executive KPIs**
- Total EV population  
- % BEV vs % PHEV  
- Average Electric Range  
- Total eligible CAFV vehicles  
- Top 5 EV manufacturers  

---

### **✔ Geographic Insights**
- Interactive **map of EV registrations** using longitude/latitude  
- County/city-level drilldown  
- Census tract clustering  
- Heatmap-style density visualization  

---

### **✔ Vehicle Insights**
- EV adoption by **model year**
- Breakdown of **Make → Model** popularity
- Range distribution histogram
- BEV vs PHEV performance differences  

---

### **✔ CAFV Eligibility Analysis**
- Eligible vs non-eligible distributions  
- Policy-related insights  
- Geographic eligibility trends  

---

### **✔ Utility Company Analytics**
- EV count per electric utility provider  
- Multi-utility service areas  
- Utility-level adoption patterns  

---

## 🧱 4. Repository Structure

```
.
├─ README.md
├─ data/
│  ├─ raw/
│  │  └─ Electric_Vehicle_Population_Data.xlsx
│  └─ processed/
│     └─ processed_ev_data.csv  # optional if cleaned
├─ tableau/
│  └─ EV_Population_Dashboard.twbx
├─ images/
│  ├─ dashboard_overview.png
│  ├─ geographic_view.png
│  └─ make_model_insights.png
└─ docs/
   └─ data_dictionary.md
```

---
## 🧠 5. Skills Demonstrated

**Technical Skills**
- Tableau Desktop / Tableau Public  
- Data cleaning & preprocessing  
- Geospatial visual analytics  
- Creating KPI dashboards  
- Exploratory Data Analysis (EDA)  
- BI storytelling  
- Categorical & numerical segmentation  
- Working with census & coordinate-based data  

**Domain Skills**
- Sustainability analytics  
- EV adoption analysis  
- Transportation planning  
- Policy & incentive evaluation  

---

## 🚀 6. Future Enhancements

- Build predictive models for EV adoption (Python + Tableau)  
- Integrate real-time utility usage data  
- Add charging infrastructure analysis (stations, availability, accessibility)  
- Create a second dashboard comparing **urban vs rural** EV penetration  

---

# 📚 7. Data Dictionary

## Table: electric_vehicle_population

| Column Name                                           | Type      | Description                                                                                 | Example                                  |
|------------------------------------------------------|-----------|---------------------------------------------------------------------------------------------|------------------------------------------|
| `VIN (1-10)`                                         | String    | First 10 characters of the Vehicle Identification Number; used as a de-identified vehicle key. | `5YJXCAE26J`                             |
| `County`                                             | String    | County where the vehicle is registered.                                                     | `King`                                   |
| `City`                                               | String    | City where the vehicle is registered.                                                       | `Seattle`                                |
| `State`                                              | String    | US state abbreviation where the vehicle is registered.                                      | `WA`                                     |
| `Postal Code`                                        | Numeric   | 5-digit ZIP code of the registration address (numeric, may need formatting).               | `98199`                                  |
| `Model Year`                                         | Integer   | Model year of the vehicle.                                                                  | `2019`                                   |
| `Make`                                               | String    | Manufacturer / brand of the vehicle.                                                        | `TESLA`, `NISSAN`, `HONDA`               |
| `Model`                                              | String    | Specific model name of the vehicle.                                                         | `MODEL 3`, `LEAF`, `CLARITY`             |
| `Electric Vehicle Type`                              | String    | Type of electric vehicle (BEV or PHEV).                                                     | `Battery Electric Vehicle (BEV)`         |
| `Clean Alternative Fuel Vehicle (CAFV) Eligibility`  | String    | Eligibility status for clean-fuel incentives.                                               | `Clean Alternative Fuel Vehicle Eligible`|
| `Electric Range`                                     | Integer   | Electric driving range in miles.                                                            | `238`                                    |
| `Base MSRP`                                          | Integer   | Manufacturer’s Suggested Retail Price when new.                                            | `35000`                                  |
| `Legislative District`                               | Numeric   | Legislative district code for the registration location.                                   | `36.0`                                   |
| `DOL Vehicle ID`                                     | Integer   | Unique identifier assigned by the Department of Licensing.                                 | `211807760`                              |
| `Vehicle Location`                                   | String    | Geospatial coordinates represented as “POINT (longitude latitude)”.                        | `POINT (-122.40092 47.65908)`           |
| `Electric Utility`                                   | String    | Utility provider serving the registration address.                                          | `CITY OF SEATTLE - (WA)`                 |
| `2020 Census Block Group`                              | Numeric   | Subdivision of census tract for finer geographic analysis.                                 | `530330001001`                            |
| `Latitude`                                             | Float     | Latitude coordinate of the vehicle registration location.                                  | `47.65908`                                |
| `Longitude`                                            | Float     | Longitude coordinate of the vehicle registration location.                                 | `-122.40092`                              |
| `Registration Date`                                    | Date      | Date when the vehicle was registered.                                                      | `2023-04-15`                              |
