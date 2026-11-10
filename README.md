# 🚗 Electric Vehicle (EV) Adoption & Market Share Analysis

## 📌 Executive Summary
This project analyzes 180,000+ Electric Vehicle (EV) and Plug-in Hybrid Electric Vehicle (PHEV) registration records from the Washington State Department of Licensing. Using Python for programmatic data cleaning and Power BI for interactive visualization, I transformed raw public dataset records into an executive-level dashboard to uncover key industry metrics: market share breakdown, battery range evolution across model years, vehicle category preferences, and regional adoption density.

---

## 🌐 Data Source & Attribution
- **Dataset Name:** Electric Vehicle Population Data
- **Source:** Official U.S. Government Open Data Portal (catalog.data.gov) / Washington State Department of Licensing (DOL)
- **Scope:** Public vehicle registration records across Washington State, United States

---

## 🎯 Key Business Questions Answered
1. **Brand Dominance:** Which manufacturers lead the EV market, and what percentage of market share does Tesla hold relative to traditional automakers?
2. **Category Split:** What is the ratio of pure Battery Electric Vehicles (BEVs) vs. Plug-in Hybrid Electric Vehicles (PHEVs)?
3. **Technology Advancement:** How has the average electric battery range evolved across vehicle model years?
4. **Geographic Distribution:** Which counties exhibit the highest concentration of EV registrations?

---

## 🧹 Data Cleaning & Preprocessing (Python / Jupyter Notebook)
Before loading the dataset into Power BI, initial data cleaning and audit were executed programmatically using Pandas in Python (`EV_Data_Cleaning.ipynb`):
- **Missing Value Handling:** Audited missing values in key columns (`County`, `Legislative District`, `Electric Range`) and applied standard missing-data treatments.
- **Deduplication Check:** Verified data integrity by checking uniqueness across `DOL Vehicle ID` to eliminate duplicate registration records.
- **Range Value Normalization:** Filtered out unresearched zero-range placeholder records to ensure accurate trendline reporting across model years.
- **Data Type Alignment:** Standardized numeric fields (`Model Year`, `Electric Range`) and text categorical variables (`Make`, `County`, `EV Type`) for efficient DAX calculations.

---

## 📊 Dashboard Features & Key Insights
- **Market Share Concentration:** Tesla dominates total registered electric vehicles in Washington State, followed by Chevrolet, Nissan, Ford, and BMW.
- **BEV vs. PHEV Preference:** Battery Electric Vehicles (BEVs) significantly outperform Plug-in Hybrids (PHEVs) in consumer adoption, accounting for the vast majority of total registrations.
- **Range Evolution:** Average electric battery range shows a clear upward trend across newer model years, reflecting significant advances in battery efficiency and infrastructure readiness.
- **Interactive Slicers:** Dynamic filtering by County (`Select County`) and Vehicle Type (`Select EV Type`) for targeted drill-down analysis.

---

## 🛠️ Tools & Technologies Used
- **Python (Pandas):** Data cleaning, missing value handling, deduplication, and initial exploratory data analysis (EDA).
- **Power BI Desktop:** DAX measures (`Total EVs`, `Tesla Share %`, `Avg Battery Range`), visual hierarchy customization, and interactive dashboard design.
- **Power Query:** Final model integration, column formatting, and schema validation.
- **GitHub:** Project hosting, version control, and documentation.

---

## 📂 Repository Structure
```plaintext
├── EV_Data_Cleaning.ipynb        # Jupyter Notebook (Data cleaning & EDA)
├── EV_Population_Analysis.pbix   # Interactive Power BI Dashboard file
├── Dashboard_Preview.png         # High-resolution screenshot of final dashboard
└── README.md                     # Project documentation & summary
