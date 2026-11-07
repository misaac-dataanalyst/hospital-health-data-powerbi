# Hospital Health Data Analysis | Power BI

An interactive Power BI dashboard built on a deliberately messy health dataset (1,500 patient records, 25 columns). The project covers data cleaning in Power Query, DAX measures and visual analysis, with findings and recommendations for hospital decision-makers.

> **Tool:** Power BI (Power Query, DAX)

---

## Table of Contents
- [Project Overview](#project-overview)
- [Business Questions](#business-questions)
- [Dataset](#dataset)
- [Data Cleaning](#data-cleaning)
- [Data Model and Measures](#data-model-and-measures)
- [Dashboard](#dashboard)
- [Key Insights](#key-insights)
- [Recommendations](#recommendations)
- [Repository Structure](#repository-structure)
- [How to Use](#how-to-use)
- [Limitations](#limitations)
- [Roadmap](#roadmap)
- [Author](#author)

---

## Project Overview

Hospital administrators need a clear view of patient volume, length of stay, patient satisfaction and health risk indicators across facilities and departments. This project simulates that scenario: starting from raw, inconsistent data, I cleaned and standardised it in Power Query and built an interactive report to surface insights and recommendations.

## Business Questions

1. How many patients does each hospital and department attend to, and how long do they stay?
2. Which departments have the longest average stay and the lowest patient satisfaction?
3. How do health indicators (BMI, cholesterol, alcohol use) vary across hospitals and patient groups?
4. How are patients discharged across departments?
5. What actions could improve efficiency and patient outcomes?

## Dataset

| Item | Detail |
|---|---|
| File | `messy_health_data_1500` |
| Rows | 1,500 |
| Columns | 25 |
| Facilities | Abeokuta Federal Hospital, Abuja National Clinic, Enugu Regional Hospital, Garki Hospital, Ibadan University Hospital, Ikeja Medical Centre |

**Fields used in the dashboard include:** `Hospital_Name`, `Department`, `Length_of_Stay_Days`, `Patient_Satisfaction_1_10`, `Cholesterol_mg_dL`, `Alcohol_Use`, `Discharge_Disposition`, BMI.

The data is synthetic and intentionally messy to practise real-world cleaning (inconsistent text casing and spelling, missing values, mixed formats).

## Data Cleaning

Steps applied in Power Query:

- [ ] Standardised text fields (e.g. `ibadan university hospital` → `Ibadan University Hospital`) and trimmed whitespace
- [ ] Handled missing values (document the approach per column)
- [ ] Fixed data types
- [ ] Removed duplicates
- [ ] Validated ranges (satisfaction 1–10, plausible BMI and cholesterol values)
- [ ] Renamed unclear columns for readability

> Tick only what you actually did, and add before/after row counts.

## Data Model and Measures

| Measure | Purpose |
|---|---|
| `TOTAL ATTENDANCE` | Total patient visits |
| `TOTAL STAY` | Total length of stay (days) |
| `AVG BMI` | Average body mass index |

Average length of stay, average satisfaction and average cholesterol are calculated with Average aggregations in the visuals.

## Dashboard

The report has three pages:

| Page | Contents |
|---|---|
| **Overview** | KPI cards (attendance, total stay, average BMI), department slicer, alcohol use by hospital, discharge disposition by department, average cholesterol, department summary table |
| **Charts** | Focused chart view with department slicer |
| **Department Table** | Average length of stay and average satisfaction by department |

![Dashboard overview](./images/dashboard-overview.png)

## Key Insights

> Fill these in with your actual numbers. Examples of the format:

1. **[Department]** has the longest average stay at **[X] days**, versus **[Y] days** overall.
2. **[Hospital]** has the highest alcohol-use count, with **[X]** patients.
3. **[Group]** has the highest average cholesterol at **[X] mg/dL**.
4. The most common discharge disposition is **[type]**, highest in **[department]**.

## Recommendations

> Tie each recommendation to an insight above.

1. **Reduce length of stay in [department]** by reviewing discharge planning and bed turnover.
2. **Target preventive screening and lifestyle programmes** at the groups with elevated cholesterol, BMI or alcohol use.
3. **Standardise data entry** across facilities (naming, formats) to improve reporting quality.

## Repository Structure

```
├── README.md
├── data/
│   └── messy_health_data_1500.csv
├── powerbi/
│   └── Health_Data.pbix
└── images/
    └── dashboard-overview.png
```

## How to Use

1. Clone the repository: `git clone https://github.com/<your-username>/<repo-name>.git`
2. Open `powerbi/Health_Data.pbix` in **Power BI Desktop** (free from Microsoft).
3. If prompted, point the data source to the file in `data/` and refresh.

## Limitations

- The dataset is synthetic, so findings illustrate the analysis process and do not represent real hospitals.
- Results depend on the cleaning decisions documented above.
- Patterns shown in the dashboard do not imply causation.

## Roadmap

- [ ] Add SQL queries to validate the dashboard figures
- [ ] Add an Excel summary workbook

## Author

**[Your Name]**
Aspiring Data Analyst
[LinkedIn](https://linkedin.com/in/your-profile) · [Email](mailto:your.email@example.com)
