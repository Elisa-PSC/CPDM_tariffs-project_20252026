# Global Tariff Analysis: Wealth and Trade Policy

## Overview

This project investigates the following question: *do richer countries impose lower tariffs than poorer countries?*
</br> 
Using comprehensive data from the World Bank's World Integrated Trade Solution (WITS) database spanning 2000-2022, we perform rigorous statistical analysis to understand the relationship between national wealth (GDP) and tariff policy.

## Research Question

**Primary Question:** is there a significant relationship between a country's GDP and its tariff rates?

**Key Hypotheses:**
- $H_0$ (Null): There is no significant relationship between national wealth and tariff rates
- $H_1$ (Alternative): Wealthier countries impose significantly lower tariffs than poorer countries

## Key Findings

Our analysis reveals strong empirical evidence for the wealth-tariff relationship:

- **The Wealth-Tariff Gap:** poorest 25% of countries maintain average tariffs of 10.40%, while the richest 25% average only 3.65% — a difference of 6.74 percentage points (184.5% higher);
- **Statistical Significance:** correlation coefficient of -0.3284 ($p$ < 0.001) demonstrates a significant negative relationship;
- **Explanatory Power:** GDP alone explains 10.8% of tariff variation ($R^2$ = 0.1079), which is substantial in economic analysis;
- **Temporal Consistency:** the pattern persisted consistently from 2000 to 2022, indicating a structural rather than temporary phenomenon.

## Dataset

### Data Sources
All data obtained from the World Bank's World Integrated Trade Solution (WITS):
- **Source URL:** https://wits.worldbank.org/

### Files Required
1. `WITS-Product_bycountry_all.csv` - Tariff rates by country and year
2. `WITS-Country-GDP_USD_all.csv` - GDP data in USD
3. `WITS-Trade_percentage_of_GDP_all.csv` - Trade openness metrics

### Data Coverage
- **Time Period:** 2000-2022 (23 years)
- **Countries:** 150+ nations across all income levels
- **Observations:** 10,000+ country-year pairs

## Methodology
### Statistical Techniques

1. **Descriptive Statistics** </br>
   We summarized the data using measures of central tendency (mean and median) and dispersion (standard deviation and range), while also examining temporal trends over time.

2. **Correlation Analysis** </br>
   Relationships between variables were assessed using Pearson correlation coefficients. GDP values were log-transformed to normalize the distribution, and correlations with trade openness were specifically evaluated.

3. **Regression Analysis** </br>
   Linear regression models were fitted to explore the relationship between tariff rates and log-transformed GDP ( $\text{Tariff Rate} \sim \log_{10}(\text{GDP})$ ). Model fit was evaluated using $R^2$, and statistical significance was tested through p-values.

4. **Hypothesis Testing** </br>
   Differences between groups were tested using two-sample t-tests, focusing on the poorest versus richest quartiles and variations in trade openness. All tests used a significance threshold of $\alpha = 0.05$.

5. **Exploratory Data Analysis** </br>
   The dataset was further explored by segmenting countries into wealth quartiles, identifying outliers via z-scores, analyzing volatility across nations, and visualizing geographic patterns.

### Key Variables

- **Dependent Variable:** Average applied tariff rate (%);
- **Independent Variables:**
  - GDP (USD) (raw and log-transformed);
  - Wealth quartiles (categorical);
  - Trade as % of GDP (openness measure).

## Project Structure

```
tariff-wealth-analysis/
│
├── collab_file_name.ipynb          # Main analysis script
├── README.md                       # This file
│
├── data/                           # Data directory
│   ├── WITS-Product_bycountry_all.csv
│   ├── WITS-Country-GDP_USD_all.csv
│   └── WITS-Trade_percentage_of_GDP_all.csv
│
├── figures/                        # Generated visualizations
│   ├── fig_evolution_by_wealth.png
│   ├── fig_map.png
│   ├── fig_top_10_bottom.png
│   ├── fig_wealth_quartile_bars.png
│   ├── fig_avg_tariff_years.png
│   ├── fig_gdp_tariff_scatter.png
│   ├── fig_trade_openness_boxplot.png
│   └── fig_trade_openness_boxplot_no_extreme.png
│
└── LICENSE                         # MIT License
```

## Visualizations

The analysis generates eight key visualizations:

1. **Evolution of Tariff Rates by Wealth Level (2000-2022)**: time series comparing tariff trends across wealth quartiles;
2. **Global Tariff Distribution Map (2022)**: choropleth map of worldwide tariff rates;
3. **Policy Gap: Top 10 vs. Bottom 10 Countries (2022)** : horizontal bar chart with reference means;
4. **Average Tariff Rates by Wealth Level** : bar chart showing the inverse relationship between wealth and tariffs;
5. **Poorest vs. Richest Countries: Tariff Trends** : dual-axis comparison of absolute rates and percentage changes;
6. **GDP vs. Tariff Rate Relationship**: scatter plot with regression demonstrating negative correlation;
7. **High vs Low Trade Openness (Full)** : box plot with complete distribution including extreme outliers;
8. **High vs Low Trade Openness (Capped)**: box plot comparison excluding outliers above 100%.

## Authors

- Alessia Barel
- Ceren Özgür
- Matteo Naccari
- Elisa Pascon

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Last Updated:** January 2026
