# 📊 Deloitte Australia — Data Analytics Job Simulation   

A virtual job simulation completed on Deloitte Australia's program, covering two real-world data analytics tasks: building an interactive Tableau dashboard to analyze factory machine downtime, and classifying gender pay equality scores across job roles using Excel formula logic.   

---

## 📌 Simulation Overview   

| Detail | Info |
|--------|------|
| Program | Deloitte Australia — Data Analytics Job Simulation |
| Platform | Forage |
| Difficulty | Intermediate |
| Tasks Completed | 2 |
| Tools Used | Tableau, Excel |
| Status | ✅ Completed — Certificate Earned |

---

## 📁 Files in This Repository   

| File | Description |
|------|-------------|
| `daikibo-telemetry-data.json` | Raw telemetry data from 4 Daikibo factories |
| `Deloitte_Simulation_-_Tableau_File.twb` | Tableau workbook with both dashboard sheets |
| `Task_5_Equality_Table.xlsx` | Completed equality classification table |
| `Dashboard.png` | Screenshot of the final Tableau dashboard |
| `Equality_Table_Screenshot.png` | Screenshot of the completed equality table |

---

## 🏭 Task One — Data Analysis (Tableau)   

### Background   
Client Daikibo Industrials operates 4 factories globally:    
- Daikibo Factory Meiyo (Tokyo, Japan)   
- Daikibo Factory Seiko (Osaka, Japan)   
- Daikibo Berlin (Berlin, Germany)   
- Daikibo Shenzhen (Shenzhen, China)   

Each factory has 9 machine types sending a telemetry status message every 10 minutes throughout May 2021. The data was unified into a single JSON file. Daikibo needed answers to two questions:   

1. **In which location did machines break the most?**   
2. **What are the machines that broke most often in that location?**   

### What I Did   
- Imported the `daikibo-telemetry-data.json` file into Tableau, checking all Schema levels during import   
- Created a calculated measure field called **"Unhealthy"** — assigning a value of 10 for every unhealthy machine status (representing 10 minutes of potential downtime since the previous message)   
- Built a bar chart: **"Down Time per Factory"** showing total unhealthy time per location   
- Built a second bar chart: **"Down Time per Device Type"** showing which machine types broke most often   
- Combined both charts into a single **interactive dashboard** where clicking a factory bar filters the device chart to show only that factory's machine breakdown data   
- Selected the factory with the highest downtime and submitted a filtered dashboard screenshot as the task deliverable   

### Key Finding   
**Daikibo Factory Seiko** recorded the highest machine downtime (~480 units), significantly ahead of Daikibo Shenzhen (~420), Daikibo Factory Meiyo (~110), and Daikibo Berlin (~15).    

Within Seiko, **LaserWelder** was the most frequently broken device type — dominating the right-hand chart when Seiko is selected as the active filter.   

---

## ⚖️ Task Two — Forensic Technology (Excel)   

### Background   
Following internal complaints about gender inequality in salary, Daikibo Industrials asked Deloitte's Forensic Tech team to investigate. An algorithm was built to quantify a **"level of gender pay equality"** score for each job role across all factory locations.   

The score is an integer ranging from **-100 to +100**, where **0 is ideal**. My task was to classify each score into one of three equality categories.   

### Classification Logic   

| Equality Score Range | Equality Class |
|----------------------|----------------|
| -10 to +10 | 🟢 Fair |
| -20 to -11 OR +11 to +20 | 🟡 Unfair |
| Below -20 OR Above +20 | 🔴 Highly Discriminative |

**Examples from the task brief:**   
- 10 → Fair   
- -9 → Unfair   
- -30 → Highly Discriminative   

### What I Did   
- Opened the provided `Equality Table.xlsx` containing 3 columns: Factory, Job Role, and Equality Score   
- Added a 4th column: **"Equality class"**   
- Wrote a nested `IF` formula to classify each score automatically based on the three thresholds above   
- Applied color coding: green for Fair, yellow/orange for Unfair, red for Highly Discriminative   
- Submitted the completed file as the task deliverable   

### Key Finding   
Across all 4 factories and 9–10 job roles each, the majority of senior roles (C-Level, VP, Director, Sr. Manager) were classified as **Highly Discriminative or Unfair** — indicating a consistent pattern of gender pay inequality concentrated at the top of the organizational hierarchy. Engineer-level roles generally scored within the **Fair** range across all locations.   

---

## 🛠️ Tools Used   

| Tool | Purpose |
|------|---------|
| Tableau | Dashboard building, calculated fields, interactive filters |
| Microsoft Excel | Equality classification formula (nested IF logic) |
| JSON | Raw telemetry data format |

---

## 💡 Key Learnings   

- How to import and parse a real-world JSON telemetry dataset in Tableau and handle schema-level data correctly   
- Creating calculated measure fields in Tableau to convert raw status flags into quantifiable downtime values   
- Building interactive dashboards where one chart filters another — a core pattern in business intelligence reporting   
- Writing nested IF formulas to classify numerical scores into categorical labels — directly applicable to real HR analytics   
- Reading data critically to identify patterns across locations and hierarchy levels rather than just surface-level numbers   

---

## 🏆 Certificate   

This simulation was completed as part of the **Deloitte Australia Data Analytics Job Simulation** on the Forage platform.   

---

## 👤 Author   

**Md. Sirajul Islam**   
- [linkedin.com/in/md-sirajul-islam57](https://linkedin.com/in/md-sirajul-islam57)   
- [github.com/sirajul-islam5](https://github.com/sirajul-islam5)   

---

## 📄 License   

This repository is open source and available under the [MIT License](LICENSE).   

---

> *This project was completed as part of a virtual job simulation program offered by Deloitte Australia via Forage. All data, tasks, and client scenarios are provided by the simulation program for educational purposes.*   
