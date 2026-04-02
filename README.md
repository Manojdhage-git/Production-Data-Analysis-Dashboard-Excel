# 🏭 Production Data Analysis Dashboard — Excel

> End-to-end production data analysis on 120 manufacturing records using Excel — covers data cleaning, feature engineering, pivot table analysis, and an interactive production dashboard.

---

## 📁 Project Overview

**Production Data Analysis Dashboard** is a comprehensive Excel-based analytics project built on a dataset of **120 production records** spanning **September 2023 to September 2024**.

The project analyzes manufacturing performance across product types, regions, managers, and workforce demographics — delivering insights into total costs, units produced, and cost efficiency using **Pivot Tables**, **derived columns**, and an **interactive Dashboard**.

---

## 🗂️ Workbook Structure

| Sheet | Purpose |
|---|---|
| `Production Dataset` | Raw + processed data (120 rows, 11 columns) |
| `Pivote 1` | Total Cost by Product Type |
| `Pivote 2` | Production Count by Manager |
| `Pivote 3` | Units Produced by Year & Month |
| `Pivote 4` | Average Production Cost Per Unit by Product Type |
| `Dashboard` | Interactive visual summary dashboard |

---

## 📊 Dataset Overview

| Property | Value |
|---|---|
| Total Records | 120 production entries |
| Date Range | September 2023 – September 2024 |
| Total Cost | ₹33,71,078 |
| Total Units Produced | 34,727 units |
| Avg. Production Cost Per Unit | ₹132.39 |
| Cost Range Per Unit | ₹1.33 – ₹1,115.45 |
| Manager Age Range | 25 – 57 years |

**Product Types:** Automobiles · Furniture · Machinery · Electronics

**Regions:** West · North · South · East

**Managers:** Nancy Grey · Jane Smith · John Doe · Mike Brown · Andrew Blue · Laura Black · David White · Emily Davis · Chris Green · Sarah Lee

**Gender Categories:** Female · Male · Unknown

**Age Groups:** A1 (≤35 yrs) · A2 (36–45 yrs) · A3 (>45 yrs)

---

## 🔑 Column Descriptions

| # | Column | Description | Type |
|---|---|---|---|
| 1 | `ProductionID` | Unique identifier for each production record | Integer |
| 2 | `ProductionDate` | Date of the production run | Date |
| 3 | `Region` | Geographic region of production (North/South/East/West) | Text |
| 4 | `Manager` | Name of the production manager responsible | Text |
| 5 | `ProductType` | Category of product manufactured | Text |
| 6 | `UnitsProduced` | Number of units produced in that run | Integer |
| 7 | `TotalCost` | Total cost incurred for the production run | Integer |
| 8 | `Gender` | Gender of the manager (Female / Male / Unknown) | Text |
| 9 | `True Age` | Actual age of the manager | Integer |
| 10 | `Age Groups` | Derived age group classification (A1 / A2 / A3) | Text |
| 11 | `Production Cost Per Unit` | Derived cost efficiency metric | Decimal |

---

## 🛠️ Data Processing & Feature Engineering

### Derived Columns

**`Age Groups`** — Age bracket classification using nested `IF`:
```excel
=IF(I2<=35, "A1", IF(I2<=45, "A2", "A3"))
```
| Group | Age Range | Meaning |
|---|---|---|
| A1 | ≤ 35 years | Young workforce |
| A2 | 36 – 45 years | Mid-career workforce |
| A3 | > 45 years | Senior workforce |

**`Production Cost Per Unit`** — Cost efficiency per unit:
```excel
=G2/F2
```
(Total Cost ÷ Units Produced)

---

## 📋 Pivot Table Analysis

### Pivote 1 — Total Cost by Product Type

| Product Type | Total Cost |
|---|---|
| Automobiles | ₹11,52,805 |
| Machinery | ₹9,10,416 |
| Furniture | ₹7,03,282 |
| Electronics | ₹6,04,575 |
| **Grand Total** | **₹33,71,078** |

> **Automobiles** is the most cost-intensive product type, contributing ~34% of total cost.

---

### Pivote 2 — Production Count by Manager

| Manager | No. of Production Runs |
|---|---|
| Nancy Grey | 37 |
| Jane Smith | 18 |
| John Doe | 13 |
| Mike Brown | 11 |
| Andrew Blue | 10 |
| Laura Black | 8 |
| Emily Davis | 6 |
| Chris Green | 6 |
| David White | 6 |
| Sarah Lee | 5 |
| **Grand Total** | **120** |

> **Nancy Grey** leads with 37 production runs — nearly 31% of all records.

---

### Pivote 3 — Units Produced by Year & Month

| Period | Units Produced |
|---|---|
| **2023 Total** | **11,171** |
| Sep 2023 | 771 |
| Oct 2023 | 3,103 |
| Nov 2023 | 4,803 |
| Dec 2023 | 2,494 |
| **2024 Total** | **23,556** |
| Jan 2024 | 3,026 |
| Feb 2024 | 4,127 |
| Mar 2024 | 3,875 |
| Apr 2024 | 1,528 |
| May 2024 | 1,684 |
| Jun 2024 | 3,537 |
| Jul 2024 | 1,536 |
| Aug 2024 | 2,864 |
| Sep 2024 | 1,379 |
| **Grand Total** | **34,727** |

> **November 2023** had the highest monthly output (4,803 units). **2024 outperformed 2023** with 23,556 units vs 11,171 units.

---

### Pivote 4 — Average Production Cost Per Unit by Product Type

| Product Type | Avg. Cost Per Unit |
|---|---|
| Furniture | ₹180.44 |
| Automobiles | ₹140.87 |
| Machinery | ₹108.98 |
| Electronics | ₹108.37 |
| **Overall Average** | **₹132.39** |

> **Furniture** has the highest cost per unit despite the lowest total units produced. **Electronics** is the most cost-efficient product type per unit.

---

## 📈 Additional Insights

### Total Cost by Region
| Region | Total Cost |
|---|---|
| West | ₹16,44,662 |
| North | ₹8,90,472 |
| South | ₹5,06,450 |
| East | ₹3,29,494 |

> **West region** dominates with nearly 49% of all production costs.

### Units Produced by Product Type
| Product Type | Units Produced |
|---|---|
| Automobiles | 13,137 |
| Machinery | 9,409 |
| Electronics | 6,907 |
| Furniture | 5,274 |

### Total Cost by Manager
| Manager | Total Cost |
|---|---|
| Nancy Grey | ₹10,55,406 |
| Jane Smith | ₹4,37,373 |
| John Doe | ₹3,21,969 |
| Mike Brown | ₹3,17,664 |
| Andrew Blue | ₹3,06,363 |

### Workforce Demographics
| Gender | Count |
|---|---|
| Female | 56 (46.7%) |
| Male | 53 (44.2%) |
| Unknown | 11 (9.2%) |

| Age Group | Count |
|---|---|
| A1 (≤35 yrs) | 53 (44.2%) |
| A2 (36–45 yrs) | 42 (35.0%) |
| A3 (>45 yrs) | 25 (20.8%) |

---

## 🧰 Tools & Techniques Used

- **Microsoft Excel** (2016 or later)
- Pivot Tables (4 pivot analyses)
- Nested `IF` formulas for age group classification
- Arithmetic formula for cost-per-unit calculation
- Interactive Dashboard design
- Data aggregation by Region, Manager, Product Type, and Time

---

## 🚀 How to Use

1. **Download** and open `Production_Data_Analysis.xlsx` in Microsoft Excel
2. Navigate to the **Dashboard** sheet for the visual summary
3. Explore individual **Pivote** sheets for detailed breakdowns:
   - **Pivote 1** → Cost by Product Type
   - **Pivote 2** → Production runs by Manager
   - **Pivote 3** → Monthly and Yearly units output
   - **Pivote 4** → Cost efficiency by Product Type
4. Go to **Production Dataset** to explore the raw data with derived columns

---

## ❓ Business Questions Answered

1. Which **product type** incurs the highest total production cost?
2. Which **manager** handles the most production runs?
3. Which **month and year** saw the highest units produced?
4. Which **product type** is most cost-efficient (lowest cost per unit)?
5. Which **region** contributes the most to total cost?
6. How is the **workforce distributed** by gender and age group?
7. How does **production volume** trend month-over-month?
8. Who are the **top 5 managers** by total cost managed?

---

## 💡 Key Insights

- **Automobiles** dominate both total cost (₹11.5L) and units produced (13,137 units)
- **Furniture** is the least-produced product type but most expensive per unit (₹180.44)
- **West region** accounts for ~49% of total production cost
- **Nancy Grey** is the most active manager with 37 runs and ₹10.55L in total cost
- **November 2023** was the single highest-output month (4,803 units)
- **2024 production** (23,556 units) more than doubled 2023 (11,171 units)
- **Majority of managers** fall in the A1 age group (≤35 years), indicating a young workforce
- Higher discount does not always mean lower cost — **Electronics** is cheapest per unit despite mid-range total cost

---

## 📂 File Structure

```
Production_Data_Analysis.xlsx
├── Production Dataset     → Core data (120 rows, 11 columns)
├── Pivote 1               → Total Cost by Product Type
├── Pivote 2               → Production Count by Manager
├── Pivote 3               → Units Produced by Year & Month
├── Pivote 4               → Avg Cost Per Unit by Product Type
└── Dashboard              → Visual summary dashboard
```


## 📃 License

This project is open for educational and non-commercial use. Feel free to fork, modify, and build upon it.
