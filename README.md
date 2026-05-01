# HR Analytics Dashboard – Power BI

## Overview

This project presents a comprehensive **HR Analytics Dashboard** built in **Microsoft Power BI**, designed to provide full workforce insights at a glance. The dashboard enables HR managers and business leaders to monitor employee demographics, service tenure, promotion eligibility, job levels, and retrenchment status — all from a single interactive view.

---

## Dashboard Highlights

| Metric | Value |
|---|---|
| Total Employees | 1,470 |
| Female Employees | 588 (40%) |
| Male Employees | 882 (60%) |
| Due for Promotion | 72 (5%) |
| Not Due for Promotion | 1,398 (95%) |
| On Service | 1,353 |
| Will be Retrenched | 117 |

---

## Key Visuals

### 1. Workforce Summary (KPI Cards)
- Total headcount with gender breakdown (male vs female split)
- Promotion eligibility status across the workforce
- Retrenchment status — active employees vs those flagged for retrenchment

### 2. Employees vs Years of Service (Bar Chart)
- Horizontal bar chart showing employee distribution across service tenures
- Ranges from 0 to 22+ years of service
- Highlights that the highest concentration is at 5 years of service, followed by 1 and 3 years

### 3. Total Employees by Job Level (Column Chart)
- Vertical bar chart comparing headcount across 5 job levels
- Level 1 has the highest number of employees (~500), tapering toward Level 5
- Supports workforce planning and career progression analysis

### 4. Total Employees by Distance from Work (Pie Chart)
- Segments employees by commute distance:
  - **Very Close** — 940 employees (63.95%)
  - **Very Far** — 229 employees (15.58%)
  - **Close** — 301 employees (remaining %)
- Useful for remote work policy and transport benefit decisions

### 5. Interactive Filters (Slicers)
- **Department:** Human Resources, Research & Development, Sales
- **Education Field:** Human Resources, Life Sciences, Marketing, Medical, Other, Technical Degree
- All visuals update dynamically based on slicer selection

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| Microsoft Power BI | Dashboard development & data visualisation |
| DAX | Calculated measures and KPI logic |
| Power Query | Data transformation and cleaning |
| Excel / CSV | Source data |

---

## Key DAX Measures Used

```dax
-- Promotion Eligibility
Due for Promotion = CALCULATE(COUNTROWS('HR Data'), 'HR Data'[PromotionStatus] = "Due")

-- Retrenchment Count
Will be Retrenched = CALCULATE(COUNTROWS('HR Data'), 'HR Data'[RetrenchmentStatus] = "Yes")

-- Gender Split %
Female % = DIVIDE([Female Count], [Total Employees], 0)
```

---

## Insights & Business Value

- **60% male, 40% female** workforce — useful for diversity and inclusion reporting
- **95% of employees are not due for promotion** — indicates either a recently promoted workforce or potential stagnation risk worth investigating
- **117 employees flagged for retrenchment** — critical for HR planning, severance budgeting, and talent backfill strategy
- **63.95% of employees live very close to work** — supports decisions on office-based vs hybrid work policies
- **Level 1 dominates headcount** — suggests a bottom-heavy org structure; may warrant succession planning review

---

## How to Use

1. Clone or download this repository
2. Open the `.pbix` file in **Microsoft Power BI Desktop**
3. Use the **Department** and **Education Field** slicers to filter all visuals dynamically
4. Hover over charts for detailed tooltips
5. Export individual visuals or the full report as PDF for stakeholder sharing

---

## Project Structure

```
hr-analytics-powerbi/
│
├── HR_Analytics_Dashboard.pbix   # Power BI report file
├── HR_Data.csv                   # Source dataset
├── dashboard.png                 # Dashboard screenshot
└── README.md                     # Project documentation
```

---

## Author

**Bryan Kamanda**
Data Analyst | Business Intelligence | Machine Learning Enthusiast
📍 Nairobi, Kenya
✉ kamandamulwa@gmail.com
🔗 [LinkedIn](https://www.linkedin.com/in/kamanda-bryan-m-2567b7103)
🐙 [GitHub](https://github.com/Bryankamanda)

---

⭐ *If you find this project useful, feel free to star the repo!*
