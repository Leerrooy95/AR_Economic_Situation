# The Arkansas Border Economic Crisis

**A Data-Driven Analysis of the "Border City Paradox"**

---

## The Problem in One Sentence

Arkansas border cities are systematically losing population, capital, and talent to Mississippi and Texas—not because of geography, but because of measurable policy gaps in taxation, education, and public safety.

---

## Why This Matters

Drive five minutes across State Line Avenue in Texarkana, or cross the I-40 bridge from West Memphis to Southaven, and you'll find yourself in a different economic reality. Same labor market. Same infrastructure. Dramatically different outcomes.

This repository contains the data proving that divergence isn't accidental.

---

## Key Findings

### The Numbers That Should Alarm Policymakers

| Comparison | Metric | Arkansas | Neighbor | The Gap |
|------------|--------|----------|----------|---------|
| West Memphis vs Southaven | Violent Crime Rate | 1,922/100k | 228/100k | **AR is 8.4× higher** |
| West Memphis vs Southaven | Math Proficiency | 17.5% | 71.0% | **-53.5 points** |
| West Memphis vs Southaven | Sales Tax | 11.25% | 7.00% | **+4.25% penalty** |
| Crittenden vs DeSoto County | Poverty Rate | 20.7% | 9.2% | **+124% higher in AR** |
| Crittenden vs DeSoto County | Population Change (2020-24) | -1.7% | +5.7% | **-7.4 point swing** |
| Texarkana AR vs TX | High School Graduation | 79.5% | 91.9% | **-12.4 points** |

### The "Retail Leakage" Problem

When your sales tax is 4.25 percentage points higher than the county across the river, rational consumers do exactly what you'd expect: they shop across the border. Arkansas border residents effectively subsidize Mississippi and Texas infrastructure every time they buy groceries, clothes, or electronics in neighboring states.

### The Crime-Driven Exodus

West Memphis's violent crime rate isn't just a public safety issue—it's an economic one. Families and businesses don't relocate to high-crime areas. The 8.4× crime disparity with Southaven creates a self-reinforcing cycle: crime drives out investment, lack of investment reduces opportunities, reduced opportunities correlate with crime.

---

## What's in This Repository

### Data Files

**`Executive_Summary_Key_Gaps.csv`**  
The quick-reference file. Contains the 12 direct comparisons (crime, tax, education) that drive the core argument. Start here if you're on deadline.

**`Full_Economic_Database.csv`**  
The complete dataset spanning 2015-2025. Includes historic teacher pay, employment figures, demographics, and infrastructure metrics. 34 rows across multiple categories: Economy, Demographics, Education, Safety, and Tax.

**`Disparity_Index_Rankings.csv`**  
A statistical model ranking regional disadvantage using Z-score methodology across income and poverty metrics. Higher scores indicate greater relative disadvantage.

### Visualizations

**`Poverty_Rate_Gap.png`**  
The headline chart. Shows Crittenden County's poverty rate is 124% higher than DeSoto County's—communities separated by a single river crossing.

**`Median_Household_Income_Gap.png`**  
Income disparities across all three border pairs. Crittenden County households earn $29,000 less than DeSoto County counterparts.

**`Correlation_IncomeGap_vs_EduGap.png`**  
Demonstrates the relationship between education investment and economic outcomes. Counties with larger education gaps show correspondingly larger income gaps.

**`Disparity_Index_Ranking.png`**  
Summary visualization of the Z-score disparity model.

---

## Methodology

### Data Sources

All data comes from official government sources:

- **Census Bureau** — Population, income, poverty, demographics (ACS 2024)
- **FBI Uniform Crime Reports** — Violent crime rates (UCR 2024)
- **Arkansas Department of Education (DESE)** — Test scores, graduation rates
- **Mississippi Department of Education** — Comparative education metrics
- **Texas Education Agency** — Texarkana ISD performance data
- **State Revenue Departments** — Sales tax rates (AR DFA, TX Comptroller, MS DOR)

### Border Pairs Analyzed

| Arkansas County/City | Comparison Neighbor | Why This Pairing |
|---------------------|---------------------|------------------|
| Crittenden County (West Memphis) | DeSoto County, MS (Southaven) | Same Memphis metro, different states |
| Crittenden County (West Memphis) | Shelby County, TN (Memphis) | Direct cross-river neighbor |
| Miller County (Texarkana AR) | Bowie County, TX (Texarkana TX) | Literally the same city, split by state line |

### Disparity Index Calculation

The Disparity Score uses Z-score normalization:
1. Calculate Z-scores for median household income (inverted: lower income = higher disadvantage)
2. Calculate Z-scores for poverty rate (higher poverty = higher disadvantage)
3. Sum the two Z-scores for composite ranking

---

## The Policy Argument

### This Is Not Geographic Destiny

Northwest Arkansas proves the state can compete. Fayetteville-Bentonville is one of America's fastest-growing metros. The difference? Concentrated corporate investment (Walmart, Tyson, J.B. Hunt), university presence, and deliberate infrastructure development.

Border cities have none of those advantages—and they're actively penalized by:

1. **Regressive tax structure** — High sales taxes drive retail dollars across state lines
2. **Education funding that meets adequacy standards but fails outcomes** — Lake View compliance doesn't equal competitive schools
3. **Public safety crisis** — Crime rates that make the area uninsurable for businesses

### Recent Bright Spots

- **Google Data Center ($4B)** — Validates West Memphis's power infrastructure
- **Buc-ee's Travel Center** — Captures interstate traffic rather than relying on local tax base

These wins prove the geography still has value. The question is whether policy will catch up.

---

## Suggested Actions

**For Journalists:**  
The `Executive_Summary_Key_Gaps.csv` file contains every comparison cited in this README with source attribution. The story isn't "Arkansas is poor"—it's "Arkansas border policy creates measurable, avoidable disadvantage."

**For Policymakers:**  
Consider sales tax stabilization zones that match neighboring states' rates in border municipalities. The revenue loss is real but finite; the retail leakage is ongoing and compounding.

**For Researchers:**  
The `Full_Economic_Database.csv` file is structured for correlation analysis. The temporal data (2015-2025) allows for policy-change impact assessment.

---

## Citation

If you use this data, please cite:

> Mid-South Economic Research Bureau. (2025). *The Arkansas Border Economic Crisis: A Data-Driven Analysis of the Border City Paradox.* [GitHub Repository]

---

## Contact

For questions about methodology or data sources, open an issue in this repository.

---

## License

Data compiled from public government sources. Analysis and documentation released under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/).

---

*Last updated: December 2025*
