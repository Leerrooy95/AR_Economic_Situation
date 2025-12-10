# Data Dictionary

This document explains every field in the repository's datasets.

---

## Executive_Summary_Key_Gaps.csv

The quick-reference file for direct border comparisons.

| Field | Description | Example |
|-------|-------------|---------|
| `Border_Pair` | The two regions being compared | "West Memphis vs Southaven" |
| `Metric` | What's being measured | "Violent Crime Rate (per 100k)" |
| `AR_Value` | The Arkansas side's value | 1922.0 |
| `Neighbor_Value` | The comparison state's value | 228.0 |
| `Gap_Value` | Raw difference (AR minus Neighbor) | 1694.0 |
| `Gap_Percent` | Percentage difference relative to neighbor | 743.0 |
| `AR_Advantage` | Does Arkansas perform better? | "Yes" or "No" |

**Note on `AR_Advantage`:** "Yes" means the metric favors Arkansas only in the literal numeric sense. For crime rates and tax rates, "Yes" means Arkansas has a *higher* value—which is actually worse for residents.

---

## Full_Economic_Database.csv

The comprehensive dataset for longitudinal analysis.

| Field | Description | Values |
|-------|-------------|--------|
| `Year` | Data year | 2015-2025 |
| `Region` | Geographic area | County name, city name, or "Statewide" |
| `State` | Two-letter state code | AR, TX, TN, MS |
| `Metric` | What's being measured | See metric list below |
| `Value` | The numeric value | Varies by metric |
| `Unit` | Unit of measurement | Percent, Count, Incidents, Score |
| `Source_ID` | Data source identifier | See source key below |
| `Category` | Grouping for analysis | Economy, Demographics, Education, Safety, Tax |

### Metric Definitions

**Economy Metrics:**
- `Net Business Establishments Added` — New businesses minus closures (annual)
- `Total Employment` — Number of employed persons in the region
- `Employment Growth YoY` — Year-over-year employment change (percentage)

**Demographics Metrics:**
- `Population Change 2020-2024` — Percentage population change over four years
- `Net Migration 2023-2024` — Number of people who moved in minus moved out

**Education Metrics:**
- `Reading Proficiency Rate` — Percentage of students meeting reading standards
- `Math Proficiency Rate` — Percentage of students meeting math standards
- `High School Graduation Rate` — Percentage of students completing high school
- `Average ACT Score` — Mean ACT composite score for district

**Safety Metrics:**
- `Violent Crime Rate (per 100k)` — FBI UCR violent crimes per 100,000 residents
- `Homicide Count` — Total homicides in reporting period

**Tax Metrics:**
- `Combined Sales Tax Rate` — State rate plus all local rates (percentage)

### Source Key

| Source_ID | Full Source Name |
|-----------|-----------------|
| `SBA_2022` | U.S. Small Business Administration |
| `Census_CBP_2023` | Census Bureau County Business Patterns |
| `Census_CBP_2025` | Census Bureau County Business Patterns |
| `Census_2024` | U.S. Census Bureau Population Estimates |
| `AR_DESE_2024` | Arkansas Department of Education |
| `MS_DOE_2024` | Mississippi Department of Education |
| `TX_TEA_2024` | Texas Education Agency |
| `FBI_UCR_2024` | FBI Uniform Crime Reports |
| `West_Memphis_PD_2024` | West Memphis Police Department |
| `AR_DFA_2025` | Arkansas Dept. of Finance and Administration |
| `TX_Comptroller_2025` | Texas Comptroller of Public Accounts |
| `MS_DOR_2025` | Mississippi Department of Revenue |

---

## Disparity_Index_Rankings.csv

Statistical ranking of regional disadvantage.

| Field | Description |
|-------|-------------|
| `Region` | County name |
| `Median Household Income` | Annual household income (dollars) |
| `Poverty Rate` | Percentage of population below poverty line |
| `Z_Income` | Standardized income score (negative = below average) |
| `Z_Poverty` | Standardized poverty score (positive = above average poverty) |
| `Disparity_Score` | Combined disadvantage score (higher = more disadvantaged) |

### How to Interpret the Disparity Score

The score is calculated as: `Z_Poverty - Z_Income`

This means:
- **Positive scores** indicate disadvantage (high poverty and/or low income relative to the dataset)
- **Negative scores** indicate advantage (low poverty and/or high income)
- **Scores near zero** are close to the dataset average

Example: DeSoto County's score of -3.73 indicates it's significantly more advantaged than the comparison set. Miller County's score of +1.66 indicates significant relative disadvantage.

---

## Data Limitations

1. **Temporal coverage varies** — Most data is 2024-2025, but some economic metrics are from 2022-2023 due to reporting lag.

2. **Geographic granularity** — Some metrics are county-level, others are city-level or school-district-level. Border pairs were selected to maximize comparability.

3. **Crime reporting inconsistencies** — FBI UCR data relies on local agency reporting. Small jurisdictions may have reporting gaps.

4. **Education metrics aren't perfectly comparable** — Each state uses different proficiency standards. Cross-state comparisons should be interpreted as directional, not precise.

---

## Suggested Analyses

**For correlation analysis:**
```
Income Gap vs Education Gap (use Correlation_IncomeGap_vs_EduGap.png as reference)
Income Gap vs Poverty Gap
Tax Differential vs Population Change
Crime Rate vs Business Formation
```

**For temporal analysis:**
```
Filter Full_Economic_Database.csv by Year
Compare 2015 vs 2025 metrics where available
Identify inflection points after policy changes
```

---

*Questions about specific data points? Open an issue.*
