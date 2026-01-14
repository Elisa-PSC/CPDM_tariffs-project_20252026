# Global Tariff Analysis: Wealth and Trade Policy

## Overview

This project investigates the following question: **Do richer countries impose lower tariffs than poorer countries?** 
</br> 
Using comprehensive data from the World Bank's World Integrated Trade Solution (WITS) database spanning 2018-2022, we perform rigorous statistical analysis to understand the relationship between national wealth (GDP) and tariff policy.

## Research Question

**Primary Question:** Is there a significant relationship between a country's GDP and its tariff rates?

**Key Hypotheses:**
- $H_0$ (Null): There is no significant relationship between national wealth and tariff rates
- $H_1$ (Alternative): Wealthier countries impose significantly lower tariffs than poorer countries

## Key Findings

Our analysis reveals strong empirical evidence for the wealth-tariff relationship:

- **The Wealth-Tariff Gap:** Poorest 25% of countries maintain average tariffs of 8.89%, while the richest 25% average only 3.28%—a difference of 5.61 percentage points (171% higher)
- **Statistical Significance:** Correlation coefficient of -0.347 (p < 0.001) demonstrates a significant negative relationship
- **Explanatory Power:** GDP alone explains 12.1% of tariff variation ($R^2$ = 0.121), which is substantial in economic analysis
- **Temporal Consistency:** The pattern persisted consistently from 2018 to 2022, indicating a structural rather than temporary phenomenon

## Dataset

### Data Sources
All data obtained from the World Bank's World Integrated Trade Solution (WITS):
- **Source URL:** https://wits.worldbank.org/

### Files Required
1. `WITS-Product_bycountry_18-22.csv` - Tariff rates by country and year
2. `WITS-Country-GDP_USD.csv` - GDP data in USD
3. `WITS-Trade_percentage_of_GDP.csv` - Trade openness metrics
4. `WITS-Product_import_tariffs.csv` - Detailed product-level tariff data

### Data Coverage
- **Time Period:** 2018-2022 (5 years)
- **Countries:** 150+ nations across all income levels
- **Observations:** 10,000+ country-year pairs

## Methodology

### Statistical Techniques

1. **Descriptive Statistics**
   - Central tendency measures (mean, median)
   - Dispersion analysis (standard deviation, range)
   - Temporal trend analysis

2. **Correlation Analysis**
   - Pearson correlation coefficients
   - Logarithmic transformation for GDP normalization
   - Trade openness correlation assessment

3. **Regression Analysis**
   - Linear regression: Tariff Rate ~ $\text{log}_{10}$(GDP)
   - $R^2$ calculation for explanatory power
   - Statistical significance testing (p-values)

4. **Hypothesis Testing**
   - Two-sample t-tests (poorest vs. richest quartiles)
   - Trade openness comparison tests
   - Significance level: $\alpha$ = 0.05

5. **Exploratory Data Analysis**
   - Wealth quartile segmentation
   - Outlier identification (z-scores)
   - Volatility analysis across countries
   - Geographic visualization

### Key Variables

- **Dependent Variable:** Average applied tariff rate (%)
- **Independent Variables:**
  - GDP (USD) - raw and log-transformed
  - Wealth quartiles (categorical)
  - Trade as % of GDP (openness measure)

## Project Structure

```
tariff-wealth-analysis/
│
├── collab_reviewed_version.ipynb    # Main analysis script
├── README.md                        # This file
├── requirements.txt                 # Python dependencies
│
├── data/                           # Data directory
│   ├── WITS-Product_bycountry_18-22.csv
│   ├── WITS-Country-GDP_USD.csv
│   ├── WITS-Trade_percentage_of_GDP.csv
│   └── WITS-Product_import_tariffs.csv
│
├── figures/                        # Generated visualizations
│   ├── fig1_gdp_tariff_scatter.png
│   ├── fig2_wealth_quartile_bars.png
│   └── fig3_trade_openness_boxplot.png
│   └── ...
│
└── LICENSE                         # MIT License
```

## Visualizations

The analysis generates several key visualizations:

1. **Scatter Plot with Regression Line** - GDP vs. Tariff Rate relationship
2. **Wealth Quartile Bar Chart** - Average tariffs by income group
3. **Interactive Choropleth Map** - Global tariff rate distribution
4. **Time Series Comparison** - Temporal trends for poorest vs. richest countries
5. **Box Plot Analysis** - Trade openness comparison
6. .....

## Authors

- Alessia Barel
- Ceren Özgür
- Matteo Naccari
- Elisa Pascon

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Last Updated:** January 2026
