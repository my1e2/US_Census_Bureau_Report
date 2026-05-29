# The Truth About America — U.S. Census Data Analysis

**A visual exploration of economic, demographic, and social inequality across the United States using Census Bureau data.**

---

## Overview

This project uses publicly available U.S. Census Bureau data to visually investigate how key statistical outcomes — income, home ownership, poverty, education, and gender wage gaps — are distributed across different demographic groups and geographic regions at the national level. Rather than summarizing raw numbers, the goal was to produce visualizations that tell a story not easily captured by looking at the data alone, exposing systemic patterns of inequality across race, gender, age, and geography.

The central question driving the analysis: **How are general statistical observations of the United States distributed among different groups at a national level?**

---

## Visualizations & Findings

### Plot 1 — Home Ownership by Race (Faceted Bar Plot)
Compares owner-occupied housing rates across racial groups in all 50 states using 2020 Decennial Census data. White households consistently show the highest ownership rates (50–80%), while Black, American Indian/Alaska Native, and multiracial households fall significantly below 50% in most states, visually surfacing the socioeconomic and structural inequalities that shape housing access across the country.

**Data:** `DECENNIALDHC2020.H10`

---

### Plot 2 — Median Household Income by State (Geospatial Map)
A choropleth map using a diverging color gradient (dark blue = lower income, dark red = higher income) to show regional income disparities. Southeastern states cluster at the lower end (~$60,000), while Northeastern and West Coast states frequently exceed $100,000. The Midwest sits in a moderate mid-range. Geographic income patterns correlate with education levels, cost of living, and population density.

**Data:** `ACSST1Y2023.S1901`

---

### Plot 3 — Distribution of Median Household Income (Violin Plot)
Supplements the map by showing the full distributional shape of median incomes across states. Most states cluster between $65,000 and $80,000, reflecting a predominantly middle-class distribution. A handful of high-income outliers (Maryland, New Jersey) push toward $90,000+, while a smaller low-income tail falls below $60,000 (Louisiana, others). The distribution is roughly symmetric with clear high-end outliers consistent with income inequality in a capitalist economy.

**Data:** `ACSSPP1Y2023.S0201`

---

### Plot 4 — Median Gross Rent vs. Education Level (Faceted Scatter Plot)
Examines the relationship between educational attainment and rental costs across states. Bachelor's and Graduate degree panels show a clear positive correlation — higher educated populations tend to live in higher-rent areas, likely driven by urbanization and gentrification. The High School panel shows a much weaker and more scattered relationship, reflecting the unpredictable living outcomes that accompany lower educational attainment and income.

**Data:** `ACSSPP1Y2023.S0201`

---

### Plot 5 — Median Earnings by Gender and Occupation (Horizontal Bar Plot, Florida)
Displays side-by-side median earnings for males and females across a wide range of occupations in Florida. Male earnings (yellow) consistently exceed female earnings (purple) across nearly every occupation, with the largest gaps in high-earning fields — legal, health diagnosis/treatment, and math-related jobs. Food preparation and personal care show smaller gaps but also the lowest overall wages. The plot puts the systemic gender wage gap into direct visual relief.

**Data:** `ACSST1Y2023.S2411`

---

### Plot 6 — Poverty Rate by Age Group and State (Heatmap)
A clustered heatmap (white = low poverty, red = high poverty) showing poverty rates across four age groups for all 50 states. Southern states (Mississippi, Louisiana, New Mexico) show the highest rates across age groups, while Northeastern and Midwestern states (New Hampshire, Vermont, North Dakota) perform significantly better. States cluster by similar socioeconomic profiles, underscoring persistent regional economic disparities.

**Data:** `ACSST1Y2023.S1701`

---

### Plot 7 — Poverty Rates by Age Group Across Selected States (Line Plot)
Tracks poverty rates through four age brackets (Under 5, 5–17, 18–64, 65+) for Colorado, Connecticut, Delaware, and Maryland. Poverty is highest for children under 5 in all states and declines sharply with age, with the steepest drop occurring between the childhood and working-age brackets. The convergence of poverty rates in the 65+ group across states suggests that social safety nets (Social Security, Medicare, retirement programs) have been meaningfully effective at reducing poverty in older age groups.

**Data:** `ACSST1Y2023.S1701`

---

### Plot 8 — Education-Gender Network in Virginia (Network Plot)
A network visualization connecting Male and Female nodes to education level nodes, with edge thickness representing the proportion of the population in each pairing. The thickest edges connect both genders to "High school graduate or higher" and "Some college or associate's degree," confirming these as the modal education levels. The thinnest edges link to "Graduate or professional degree" and "Less than high school graduate," reflecting the smaller proportions at both extremes. Virginia's distribution likely mirrors national trends, with both genders concentrated in mid-level educational attainment.

**Data:** `ACSST1Y2023.S1501`

---

## Key Takeaways

Statistical outcomes in the United States — income, poverty, home ownership, education, and wages — are unevenly distributed along lines of race, gender, geography, and age. The patterns across these eight visualizations converge on a consistent theme: systemic inequality shapes life outcomes in ways that map clearly onto demographic and regional variables. Children face the highest poverty vulnerability. Southern states consistently underperform on economic indicators. Racial gaps in home ownership persist across all 50 states. Gender wage disparities are sharpest in the highest-paying fields. These findings underscore the importance of evidence-based policy interventions aimed at addressing the structural roots of these disparities.

---

## Libraries & Tools

- **Language:** R (R Markdown)
- **Visualization:** `ggplot2`, `ggraph`, `pheatmap`, `viridis`, `scales`, `ggthemes`
- **Data Wrangling:** `dplyr`, `tidyverse`, `tidygraph`, `igraph`
- **Mapping:** `maps`
- **Data Sources:** U.S. Census Bureau — American Community Survey (ACS) 1-Year Estimates (2023), 2020 Decennial Census

---

## Data Sources

| Dataset | Description |
|---------|-------------|
| `DECENNIALDHC2020.H10` | Home ownership by race, all states |
| `ACSST1Y2023.S1901` | Median household income by state |
| `ACSSPP1Y2023.S0201` | Demographic and housing estimates (income, rent, education) |
| `ACSST1Y2023.S2411` | Median earnings by occupation and sex (Florida) |
| `ACSST1Y2023.S1701` | Poverty status by age group and state |
| `ACSST1Y2023.S1501` | Educational attainment by gender (Virginia) |
