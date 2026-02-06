---
layout: projects/projects-individual
title: "Analyzing Regulatory Price Distortions and Systematic Inefficiencies in DISCOM Power Procurement: Evidence from ARR-IEX Price Divergence"
advisor: "Professor Partha Pratim Das, Professor Anandjit Goswami"
students: "Diya Tripathi, Jyotirmay Zamre"
abstract: "This project investigates systematic price distortions faced by Indian electricity Distribution Companies (DISCOMs) arising from divergences between regulated Average Revenue Requirement (ARR) and real-time market prices on the Indian Energy Exchange (IEX). Using granular hourly data from Delhi’s power distribution system, the study demonstrates how regulatory pricing frameworks generate predictable inefficiencies and financial stress. By constructing time-varying ARR estimates and applying LSTM-based forecasting models, the research provides quantitative evidence that regulatory-market price gaps are systematic, persistent, and forecastable."
categories: ["Energy Systems", "Machine Learning"]
---

## Project Description

Distribution Companies (DISCOMs) play a critical role in India’s electricity sector by procuring power from generators and markets and supplying it to end consumers. Despite this central role, most DISCOMs face persistent financial distress. A major contributor to this problem is the mismatch between regulated retail tariffs, determined through the Average Revenue Requirement (ARR), and volatile wholesale electricity prices discovered in short-term markets such as the Indian Energy Exchange (IEX). This project examines these mismatches in depth and argues that they are not random anomalies but systematic outcomes of the regulatory framework itself.

Focusing on Delhi as a representative case study, the project constructs an hourly, load-weighted version of ARR using publicly available demand data. This granular ARR is then aligned with hourly real-time market prices from IEX for the years 2022 and 2023. The resulting price gap series reveals persistent and sizeable divergences, particularly during peak demand periods. Statistical analysis shows low correlation between ARR and market prices, high average deviations, and strong seasonal patterns, indicating that regulated prices fail to track real market dynamics.

Beyond descriptive analysis, the project employs Long Short-Term Memory (LSTM) neural networks to predict the ARR–IEX price gap directly. By forecasting the gap rather than individual prices, the model demonstrates that these inefficiencies are highly predictable, achieving a high coefficient of determination over a 24-hour forecast horizon. This predictability serves as quantitative evidence of systemic regulatory distortion rather than market randomness.

Overall, the project contributes to the understanding of how static regulatory mechanisms interact poorly with dynamic electricity markets. It highlights the structural exposure of DISCOMs to foreseeable yet unmanageable losses and underscores the need for reforms toward more market-linked pricing, improved cost recovery mechanisms, and data-driven policy design in the Indian power sector.

## Objectives

- Quantify the hourly divergence between regulated ARR and real-time IEX prices  
- Develop a methodology to granularize annual ARR into time-varying hourly estimates  
- Analyze temporal and seasonal patterns in regulatory-market price gaps  
- Predict price gaps using LSTM-based deep learning models  
- Assess implications of predictability for market efficiency and policy reform  

## Methodology

The study follows a two-phase approach. First, annual ARR values are converted into hourly figures using load-weighted allocation based on Delhi DISCOM demand profiles. These hourly ARR values are aligned with IEX real-time market prices to compute price gaps and evaluate statistical properties such as mean absolute deviation, variance, and correlation.

In the second phase, a deep learning framework based on Long Short-Term Memory (LSTM) networks is implemented to forecast the price gap directly. The model uses temporal features such as hour of day, day of week, month, peak indicators, and historical price information. A multi-step, 24-hour forecasting setup is adopted to reflect operational planning horizons. Model performance is evaluated using RMSE, MAE, and R² metrics on a strictly chronological train-test split.

## Results and Contributions

- Evidence of persistent, large, and seasonal ARR–IEX price gaps  
- Very low correlation between regulated and market prices  
- High predictability of price gaps (R² > 0.86) using LSTM models  
- Quantitative demonstration of systematic regulatory inefficiency  
- Policy-relevant insights into DISCOM financial risk and market design  

## References

- Indian Energy Exchange (IEX) Real-Time Market Data  
- NITI Aayog India Climate & Energy Dashboard  
