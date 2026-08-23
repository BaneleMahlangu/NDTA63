# NDTA63 — Data Analysis and Visualization

## Overview

This repository contains the data analysis and visualization work completed for the **NDTA63 Data Analysis and Visualization** course.

The project focuses on analysing selected health and development indicators for **South Africa** using data obtained from the World Bank. The datasets were cleaned, processed, combined and analysed to identify trends over time.

## Source Datasets

The analysis uses datasets obtained from **World Bank Open Data**:

- **WB_HNP_ZAF.csv** — Health, Nutrition & Population data
- **WB_WDI_SN_ITK_DEFC_ZS.csv** — World Development Indicators: Prevalence of Undernourishment

## Data Cleaning

The following cleaning procedures were applied to the source datasets:

- Exact duplicate rows were removed.
- Rows with missing `OBS_VALUE` (the measurement itself) were removed rather than imputed. This was done because replacing a genuinely unmeasured observation with a statistical value could introduce information that was not present in the original data.
- The WDI dataset was filtered to include **South Africa only** (`REF_AREA = ZAF`).
- The relevant indicators were extracted and prepared for analysis.
- The cleaned datasets were organised by year to support comparison and time-series analysis.

## Indicators Analysed

The project analyses the following four indicators for South Africa:

1. **Prevalence of Undernourishment**
2. **Human Capital Index**
3. **Under-5 Mortality**
4. **Access to Water**

## Workbook Structure

The Excel workbook contains the following sheets:

- `Cleaned_Undernourishment_ZAF` — Cleaned Prevalence of Undernourishment data
- `Cleaned_HCI_ZAF` — Cleaned Human Capital Index data
- `Cleaned_Under5Mortality_ZAF` — Cleaned Under-5 Mortality data
- `Cleaned_WaterAccess_ZAF` — Cleaned Water Access data
- `Combined_SA_Timeseries` — All four indicators combined by year for comparative analysis

## Assumption: Three Values per Year

The **Human Capital Index, Under-5 Mortality and Water Access** datasets contain three observations for certain years in the source extract.

The supplied data does not retain a breakdown label that explains the reason for the three observations, such as sex, location or urban/rural classification.

Rather than discarding these observations, all three raw values were retained. The values were treated as a range and a **median** was calculated to provide one representative value for each year.

The median value was then used in:

- `Combined_SA_Timeseries`
- The group's analysis and report

This approach ensures that the original observations remain available while providing a consistent representative value for comparison across indicators.

## Undernourishment Data

The **Prevalence of Undernourishment** dataset contains one clean observation per year from **2001 to 2023**.

Because there is only one observation per year, no median-based assumption was required for this indicator.

## Calculations and Formulas

The workbook contains live Excel formulas for calculated measures, including:

- **Median**
- **Mean**
- **Year-on-Year (YoY) Change**

These formulas use functions such as `MEDIAN` and `AVERAGE`, together with cell references.

Because the calculations are formula-based, they will automatically recalculate if the underlying data is edited.

## Analysis

The cleaned and combined data is used to examine changes in South Africa's health and development indicators over time.

The analysis supports comparisons between indicators and helps identify patterns, trends and changes across the period covered by the datasets.

## Group & Lecturer

### Group Members

- Banele Mahlangu
- Ohnothabiso
- Thabang84399

### Lecturer

**Melvin Kisten**

[LinkedIn](https://www.linkedin.com/in/iammelvink)

## Acknowledgments

We would like to acknowledge and thank our lecturer, **Melvin Kisten**, for his guidance, support and instruction throughout the NDTA63 Data Analysis and Visualization course.

We also acknowledge the **World Bank Open Data** platform for providing the datasets used in this analysis.
