# Portfolio Return Risk Analysis

**Stock Return Analysis, Permutation Testing, and Portfolio Risk (VaR)**

## Overview
This repository contains a quantitative finance project focused on the analysis of stock returns, non-parametric inference, and portfolio risk assessment. The report specifically examines **Apple Inc. (AAPL)** and **Microsoft Corp. (MSFT)** over a 4-year trading period (2021–2024).

## Objectives
- Extract and process adjusted closing prices for AAPL and MSFT to compute daily logarithmic returns.
- Apply **Permutation Tests** (10,000 iterations) to evaluate:
  - Significance of covariance between the two stocks.
  - Equality of their variances (volatility).
  - Equality of their expected daily returns.
- Evaluate the statistical properties of a specific holding-period strategy.

## Portfolio Strategy
A simple trading strategy is implemented:
- Each day, purchase 100 shares of both assets  
- Sell them after 100 trading days  
- Ignore transaction costs
- **Note:** Due to the overlapping nature of the 100-day windows, the resulting profit series exhibits high autocorrelation (analyzed via ACF), which is accounted for in the statistical evaluation.

Based on this strategy:
- Portfolio profits are calculated  
- Distribution of profits is analyzed  

## Risk Analysis
The project evaluates the tail risk of the strategy's empirical profit distribution:
- Visual and formal normality checks (Q-Q plots, Shapiro-Wilk test).
- Calculation of **Value at Risk (VaR)** and **Expected Shortfall (ES)** at deep tail levels: 5%, 1%, and 0.1%.
- A comparative analysis evaluating the accuracy of parametric normal VaR vs. empirical VaR. Results show that assuming normality underestimates risk at the 5% and 1% levels, but overestimates the extreme tail loss at the 0.1% level for this specific dataset.

## Key Findings
- **Dependence:** AAPL and MSFT show a statistically significant positive covariance.
- **Volatility:** AAPL exhibited significantly higher daily return variance than MSFT during the 2021-2024 period.
- **Returns:** No statistically significant difference in mean daily returns was found between the two stocks.
- **Risk Estimation:** The portfolio profits deviate from a normal distribution. While parametric normal VaR underestimates tail risk at the 5% and 1% levels (a common fat-tail effect), it overestimates the risk at the 0.1% level, highlighting the limitations of empirical deep-tail estimation.

<img width="1920" height="960" alt="image" src="https://github.com/user-attachments/assets/30522482-e5aa-4c20-932d-815609f761ea" />


## Technologies & Packages
- **Language:** R
- **Data Retrieval:** `quantmod`
- **Visualization:** `ggplot2`, `gridExtra`, `qqplot2`
- **Time Series & Stats:** `zoo`, `moments`
- **Reporting:** RMarkdown, `knitr`, `kableExtra`

## How to View

📊 **[Click here to view the full HTML report](https://Projekty-IiE.github.io/Portfolio-Return-Risk-Analysis/Portfolio-Return-Risk-Analysis.html)**

## Project Type
This is a university course project developed for a Computer Science and Econometrics degree program, bridging the gap between statistical theory and computational finance.
