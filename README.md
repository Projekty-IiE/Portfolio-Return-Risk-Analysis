# Portfolio Return Risk Analysis

**Stock Return Analysis, Permutation Testing, and Portfolio Risk (VaR)**

## Overview
This repository contains a university project focused on the analysis of stock returns, statistical inference, and portfolio risk assessment. The project combines econometric methods with practical financial data analysis.

## Objectives
- Collect historical price data for two stocks or indices (minimum 3 years)  
- Compute daily returns  
- Analyze dependence between returns using permutation tests  
- Test:
  - Significance of covariance  
  - Equality of variances  
  - Equality of expected values  

## Portfolio Strategy
A simple trading strategy is implemented:
- Each day, purchase 100 shares of both assets  
- Sell them after 100 trading days  
- Ignore transaction costs  

Based on this strategy:
- Portfolio profits are calculated  
- Distribution of profits is analyzed  

## Risk Analysis
- Plot histogram of portfolio returns  
- Compare empirical distribution with normal distribution  
- Estimate Value at Risk (VaR):
  - 5%  
  - 1%  
  - 0.1%  
- Compare empirical VaR with parametric VaR assuming normality (same mean and variance)  

## Technologies
- R 

**Statistical methods:**
- Permutation tests  
- Hypothesis testing  
- Distribution fitting  

## Project Type
This is a **university (course) project** developed as part of studies in computer science and econometrics.
