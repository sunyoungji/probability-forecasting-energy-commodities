# Forecasting Energy Prices and Measuring Uncertainty with Copula-GARCH Models

This repository contains R code and analysis for modeling and forecasting the volatility of commodity prices.

---

## Overview

This project evaluates and compares the forecasting performance of ARMA-GARCH and Copula-GARCH models using daily futures prices of natural gas, oil, and coal (2010–2020). Forecast accuracy is assessed using the Continuous Ranked Probability Score (CRPS) and Energy Score to determine whether incorporating multivariate dependencies improves predictions compared to simpler univariate models.

Key findings:

Natural gas and coal exhibited similar volatility patterns and strong correlation, 89.7% higher than that between oil and coal.

However, incorporating multivariate dependencies (Copula models) did not significantly improve forecast accuracy.

This project was completed as part of the Case Study course at TU Dortmund.

---

## Tools & Packages

- **Language**: R

- **Key Libraries**:

  - `rugarch` – For estimation and forecasting of ARMA-GARCH models

  - `copula` – For model selection and fitting Copula models 

  - `scoringRules` – CRPS and Energy Score evaluation

---

## Data

- **Variables**: Natural Gas (EUR), Oil (USD), Coal (USD)

- **Time Frame**: March 16, 2010 – October 27, 2020

- **processing**:

  - Computed first differences of daily prices.
  - Split dataset at observation 2500:
  - First 2500 data for model training, 200 points for evaluation.

