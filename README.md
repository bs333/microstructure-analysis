# Empirical Analysis of AMZN Microstructure Data

## Overview
This project conducts an empirical analysis of **AMZN's** market microstructure using tick-level data (TAQ) from January 4, 2023. The analysis encompasses liquidity measures, volatility estimation, and the probability of informed trading (PIN), employing statistical and financial modeling techniques.

## Key Objectives
1. **Liquidity Dynamics**:
   - Compute liquidity measures such as the quoted spread, effective spread, and realized spread.
   - Analyze intra-day liquidity patterns using hourly time buckets.

2. **Volatility Estimation**:
   - Estimate intra-day volatility using statistical measures and Roll's model.
   - Evaluate realized volatility across varying sampling frequencies.

3. **Probability of Informed Trading (PIN)**:
   - Quantify the likelihood of informed trading using a PIN model based on trade imbalances.

## Methodology
1. **Data Preprocessing**:
   - Imported TAQ data, removed missing values, and transformed the dataset into an `xts` object for time-series analysis.
   - Reorganized columns to match financial conventions (e.g., bid, ask, and trade prices).

2. **Liquidity Measures**:
   - Computed the following metrics:
     - **Quoted Spread**: A proxy for market liquidity.
     - **Effective Spread**: The realized cost of executing trades.
     - **Realized Spread**: A measure of the dealer's realized profit.
   - Analyzed liquidity within hourly intervals to detect temporal trends.

3. **Volatility Analysis**:
   - Estimated volatility using:
     - Price autocorrelation.
     - Roll's model to separate bid-ask spreads from price dynamics.
     - Realized volatility metrics over intra-day intervals.

4. **PIN Model**:
   - Modeled the probability of informed trading using the **Easley, Kiefer, O’Hara (EKO)** framework.
   - Applied optimization techniques to estimate parameters and derive PIN values.

## Tools and Techniques
- **Languages**: R
- **Libraries**: `highfrequency`, `tidyverse`, `xts`, `InfoTrad`
- **Metrics**: Liquidity measures, Roll’s model parameters, and PIN likelihood.

## Results
- Liquidity measures revealed intra-day dynamics with higher spreads during less active trading hours.
- Roll’s model indicated the significant role of the bid-ask spread in observed price variations.
- The PIN value suggested a moderate probability of informed trading on January 4, 2023.

## Visualizations
- Trade and mid-price dynamics.
- Hourly trends in liquidity measures.
- Volatility signature plots and autocorrelation functions.

## Conclusion
This study provides insights into **AMZN's** market microstructure, highlighting liquidity, volatility, and informed trading characteristics. The findings can aid market participants in understanding price formation and trading costs. Future work may extend this analysis to cross-sectional comparisons or multi-day studies.
