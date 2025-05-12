---

# Driver & Fleet Behavior Analysis using Big Data Ecosystem

## Project Overview

This project demonstrates how to analyze truck fleet operations by integrating and transforming geolocation, vehicle, and mileage data using Hadoop (Hive and Pig), and visualizing the results in Power BI. The goal is to identify high-risk drivers, uncover patterns in abnormal driving events, predict fuel efficiency, analyze maintenance risks, and classify drivers into risk categories.

---

## Prerequisites

**To perform this project, you need:**
- A working Hadoop/Cloudera virtual machine (VM) set up in VMware (or a similar virtualization tool).
- Hive, Pig, and HDFS configured and running within your VM.
- Power BI Desktop installed on your local machine.

---

## Data Files Provided

- **trucks.csv**  
  Detailed truck-level data including driver, truck ID, model, and monthly mileage and fuel consumption from June 2013 to January 2009.

- **geolocation.csv**  
  Event-level geolocation data including truck ID, driver ID, event type, location, velocity, and event/idling indicators.

- **trucks_mg.csv**  
  Summarized or transformed truck metrics for further analysis.

- **DDL_risk_factor-UTD.docx**  
  Document containing all Hive DDL statements and instructions for creating, loading, and transforming tables.

- **Pigs-script-2.pptx**  
  PowerPoint file with the Pig script used to generate the `riskfactor` table.

---

## Data Processing Workflow

1. **Set Up Your Virtual Machine**
   - Install VMware (or similar) and set up a Hadoop/Cloudera VM.
   - Ensure Hive, Pig, and HDFS are running and accessible.

2. **Import Data & Create Tables**
   - Upload `trucks.csv`, `geolocation.csv`, and `trucks_mg.csv` to HDFS in your VM.
   - Use the DDL statements from `DDL_risk_factor-UTD.docx` to create required Hive tables.

3. **Risk Factor Calculation**
   - Use the provided Pig script (`Pigs-script-2.pptx`) to calculate a risk factor for each driver and store the results in the `riskfactor` table.

4. **Power BI Integration & Visualization**
   - Open Power BI Desktop.
   - Connect to your Hive server using your VM’s hostname.
   - Import tables and create visualizations to answer business questions.

---

## Business Questions Answered

1. **Which drivers have a risk factor ≥ 7.0?**
2. **Which cities report the highest number of abnormal driving events, and what types of events occur most frequently in each?**
3. **Can we predict a truck’s fuel efficiency (MPG) using its mileage and idling behaviour?**
4. **Which truck models are most likely to experience maintenance issues based on overspeeding, idling, and MPG behavior?**
5. **Can we classify drivers into risk categories (Low, Medium, High) using clustering based on events, mileage, and fuel efficiency?**

---

## Directory Structure

```
├── Data/
│   ├── trucks.csv
│   ├── geolocation.csv
│   └── trucks_mg.csv
├── Hive documentation/
│   ├── DDL_risk_factor-UTD.docx
│   └── Pigs-script-2.pptx
├── Powerbi/
│   ├── TruckFleetRiskAnalysis.pbix
│   └── Final_Presentation.pptx
└── README.md
```

---

## How to Run the Project

1. Set up the Hadoop/Cloudera VM with Hive, Pig, and HDFS.
2. Upload CSV files to HDFS.
3. Use the provided DDL statements to create and populate Hive tables.
4. Run the Pig script to generate the `riskfactor` table.
5. Open Power BI Desktop and connect to the Hive server.
6. Import tables and build visualizations.

---

## Acknowledgments

This project was completed as part of the Big Data Course curriculum at the University of Dallas at Texas, demonstrating the integration of big data tools and Power BI for actionable analytics in the trucking industry.

---

*For questions or contributions, please open an issue or submit a pull request.*
