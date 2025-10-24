# Trader Behavior & Market Sentiment Analysis

A data science project analyzing cryptocurrency trading performance across market sentiment regimes using statistical methods and machine learning.

---

## Overview

This project analyzes 211,224 trades from 32 accounts paired with daily Fear & Greed Index data to identify quantifiable patterns between trader behavior and market sentiment. The analysis uncovers predictive signals, behavioral archetypes, and actionable trading strategies backed by statistical validation.

---

## Dataset

**Trading Data:**
- 211,224 trades across 246 cryptocurrencies
- 32 unique trader accounts
- $1.19 billion total trading volume
- Period: May 2023 - May 2025

**Sentiment Data:**
- 2,644 daily Fear & Greed Index readings
- Five categories: Extreme Fear, Fear, Neutral, Greed, Extreme Greed
- Period: 2018 - 2025


---

## Quick Start

**Google Colab (Recommended):**
1. Open `notebook_1.ipynb`  in Google Colab
2. Ensure data files are in `csv_files/` directory
3. Run all cells sequentially
4. Outputs will generate in `outputs/` and `csv_files/`


---

## Key Findings

1. **Fear Premium**: Fear periods generate 3.3x higher daily PnL vs Greed ($36,892 vs $11,141, p=0.0074)

2. **Volume Signal**: Trading volume increases 3.8x in the 3 days before sentiment shifts

3. **Predictive Lag**: Sentiment changes predict PnL with 2-day lag (Granger causality p=0.0372)

4. **Lead-Lag Pattern**: Profitability leads sentiment by 7 days (cross-correlation analysis)

5. **Trader Archetypes**: Three clusters identified - Balanced, Whale, High-Frequency Scalpers (ANOVA p<0.001)

6. **Contrarian Behavior**: Profitable traders scale positions during Fear and reduce during Greed

---

## Methodology

**Statistical Analysis:**
- T-tests, Mann-Whitney U, Chi-square, ANOVA
- Granger causality testing for temporal relationships
- Cross-correlation for lead-lag patterns

**Machine Learning:**
- K-Means clustering (k=3) for trader segmentation
- DBSCAN for outlier detection
- PCA for dimensionality reduction

**Data Processing:**
- Type standardization and missing value handling
- Timestamp alignment across datasets
- Outlier treatment for visualization clarity

---

## Generated Outputs

**CSV Files (9):**
- Cleaned datasets, trader metrics, sentiment correlations, clustering results, behavioral patterns

**Visualizations (12 PNG files):**
- Sentiment distributions, trader rankings, profitability comparisons
- Time series analysis, clustering visualization, volume patterns

**Documentation:**
- `ds_report.pdf` with detailed insights and trading strategies

---

## Notebooks

**notebook_1.ipynb**

**Data Preparation & EDA:**
- Loads and cleans raw data
- Standardizes data types and handles missing values
- Calculates trader-level metrics
- Generates visualizations 1-8

**Advanced Analysis:**
- Runs statistical hypothesis tests
- Performs Granger causality and cross-correlation analysis
- Executes clustering algorithms (K-Means, DBSCAN)
- Generates visualizations 9-12

---

## Reproducibility

- All analyses use fixed random seeds
- Package versions pinned in requirements.txt
- Complete code available in notebooks
- All results generated programmatically

---

## Troubleshooting

**Date Alignment Issues:**
- Verify date columns are timezone-normalized
- Ensure daily granularity for both datasets

**Missing Values:**
- Zero PnL rows represent open positions
- Filter to closed positions for win rate calculations

**Granger Test Failures:**
- Check stationarity with ADF test
- Apply differencing if p-value > 0.05

**DBSCAN Empty Clusters:**
- Adjust eps and min_samples parameters
- Ensure proper feature scaling

---

## Contact

**Name:** Ankush Saini  
**Email:** ankushsaini04361@gmail.com  

---

## Note on AI Assistance

AI tools were used for documentation formatting and organizing presentation structure. All analytical methodology, statistical testing, code implementation, result interpretation, and trading insights are original work and fully reproducible from the provided notebooks and data.




