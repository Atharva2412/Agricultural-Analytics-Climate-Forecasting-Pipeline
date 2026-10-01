# Agricultural Data & Climate Insights Dashboard
### 1. 🌾 Agriculture Analytics & Climate Forecasting
An interactive Power BI and SQL‑Snowflake workflow analyzing **South India agriculture data (2004–2019)** to uncover rainfall, temperature, humidity, and crop yield trends across seasons, crops, and locations.

### 2. Purpose
This project simulates a **real‑world agricultural analytics pipeline**, transforming raw climate and crop datasets into actionable insights. The dashboard helps stakeholders identify **high‑yield crops, optimal seasons, and climate impacts on agriculture** for better resource planning and policy decisions.

### 3.	Tech Stack
The dashboard was built using the following tools and technologies:<br>
•	☁️ **AWS S3** – Cloud storage for raw CSV datasets.<br>
•	🗄️ **Snowflake SQL** – Data warehousing, queries, transformations.<br>
•	📊 **Power BI** – Interactive dashboards and KPI visualization.<br>
•	📝 **Data Modeling** – Year groups, rainfall segmentation, crop yield categories.<br>
•	📁 File Formats – `.sql` for queries, `.pbix` for dashboards, `.pdf/.pptx` for reports.

### 4.	Data Source
- **Dataset:** Agriculture data for South India (2004–2019)  
- **Columns:** 12 (Year, Location, Season, Crop, Area, Rainfall, Temperature, Humidity, Soil Type, Irrigation, Yield, Price)  
- **Locations:** Bangalore, Mysuru, Kodagu, Hassan, Mangalore, Raichur, Gulbarga, Kasaragodu, etc.  
- **Seasons:** Rabi, Kharif, Zaid  
- **Crops:** Paddy, Cotton, Coconut, Tea, Coffee, Ginger, Pepper, Arecanut, Cardamom, Cashew, Cocoa, Groundnut, Blackgram  
- **Rainfall Range:** 255–4103 mm   .


### 5.	Features 
•	Business Problem :
Farmers and policymakers struggle to **predict crop yields and plan resources** without structured analytics on rainfall and climate trends. 

• Key questions such as:
- 🌧️ What is the relationship between rainfall and crop yield?  
- 📊 Which regions produce the highest yield under varying climate conditions?  
- 📈 How have crop yields changed year‑over‑year?  
- 🌱 Which soil types are most productive?  
- 🚜 How can irrigation resources be allocated more effectively?  
- 🌍 Which regions are most vulnerable to climate change impacts?  
- 🔄 How do seasons (Rabi, Kharif, Zaid) affect yield outcomes?  
- 💰 Which crops deliver the highest economic value across years? .

•	Goal of the Dashboard  
- Analyzes **rainfall vs. crop yield correlations**  
- Segments regions by **rainfall groups and soil quality**  
- Highlights **year‑wise agricultural performance trends**  
- Provides **climate insights for resource allocation and policy planning**
  
•	Walkthrough of Key Visuals
- **Rainfall Analysis:** Bangalore had the highest average rainfall (3.8K); Paddy crops showed 3.5K rainfall. Seasons were nearly identical (~3,070–3,105).  
- **Temperature Analysis:** Rabi was cooler (61) vs. Kharif/Zaid (72). Ginger (79) was the hottest crop.  
- **Humidity Analysis:** Constant across all groups (~55–56), offering little differentiation.  
- **Yield Analysis:** Cotton (51K) and Coconut (34K) had the highest yields; Rabi season led with 24.9K. Kodagu (29K) and Mysuru (28K) topped by location. 


•	Business Impact & Insights
- 🌱 **High‑Yield Crops:** Cotton and Coconut stand out, followed by Ginger and Tea.  
- 🌧️ **Seasonal Impact:** Rabi season consistently delivers higher yields.  
- 📍 **Location Insights:** Kodagu and Mysuru lead in yield, while Bangalore has highest rainfall but lower yield.  
- 🌍 **Climate Forecasting:** Rainfall alone does not explain yield — other factors like soil and irrigation matter.  
- 💡 **Policy Planning:** Helps allocate irrigation resources and guide crop selection. 
### 6.	AWS Integration  
- ☁️ **AWS S3** – Raw datasets stored securely in cloud buckets  
- 🗄️ **Snowflake External Stage** – Connected Snowflake to S3 for seamless ingestion  
  ```sql
  CREATE STAGE agriculture_stage
  URL='s3://agriculture-data-bucket/'
  STORAGE_INTEGRATION = aws_integration;
  ```  
- 🔄 **Pipeline Workflow:** Data uploaded to S3 → ingested into Snowflake → transformed with SQL → visualized in Power BI  
- 🔐 **Security Note:** All credentials managed via Snowflake storage integrations; no secrets exposed in this report.
### 7.	Screenshots 
 ![Dashboard Preview](https://github.com/Atharva2412/Ola-Booking-Data-Analysis/blob/main/ola_dashboard.png)
