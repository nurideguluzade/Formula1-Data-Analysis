#Formula 1 Data Analytics Portfolio (1950–2024)

This repository contains a comprehensive data analytics project on Formula 1 racing history, combining statistical analysis in R with an interactive business intelligence dashboard in Power BI. The dataset is sourced from Kaggle – Formula 1 World Championship (1950–2024) and spans 12 interconnected tables covering races, drivers, constructors, circuits, lap times, pit stops, qualifying sessions, and standin

#R Markdown Analysis (F1yekunanaliz.Rmd)
A full exploratory data analysis covering 74 years of Formula 1 history. The report is structured into five main sections:

1. Driver Performance Analysis
- Top 10 race winners of all time — Lewis Hamilton leads with 105 wins
- Drivers with exactly one career victory
- DNF (Did Not Finish) analysis: both raw counts and normalized rates (min. 50 starts), revealing that early-era drivers (1950s–60s) suffered far higher mechanical failure rates than modern competitors
- Nationality breakdown of F1 drivers (top 10 countries)
- Longest active careers in the sport

2. Constructor Performance Analysis
- Top 10 most successful constructors by race wins
- Season-by-season points comparison: McLaren vs. Ferrari vs. Red Bull
- Team-level DNF analysis (normalized by starts)


3. Historical Trends (1950–2024)
- Growth in race calendar size over the decades, including the COVID-19 impact in 2020
- Country-level distribution of Grand Prix host nations
- Deep dive on the Azerbaijan (Baku City Circuit): lap statistics, fastest lap holders, and race outcome patterns


4. Strategic Analysis
- Pole position effect: conversion rate of pole to race win
- Grid vs. final position correlation: how much starting position predicts finishing position
- Circuit-level scoring patterns: which tracks generate the most and fewest points
- Pit stop strategy: impact of number of stops and stop duration on final race result


5. Additional Insights
- World Champions ranking: most titles by driver
- Driver age and performance: relationship between age group and average finishing position; records for youngest and oldest race winners
- Fastest lap analysis: which drivers set the most fastest laps, and whether fastest lap predicts race victory
- Qualifying → Race result relationship: correlation between qualifying time/position and race outcome; Q1/Q2/Q3 speed as a race performance predictor



#Power BI Dashboard (F1analysis.pbix)
An interactive multi-page dashboard built on the same Kaggle dataset, designed for business intelligence exploration.

Dashboard pages:

- Overview / Home — Key KPIs: total races, drivers, constructors, seasons covered
- Driver Analysis — Wins, podiums, pole positions, fastest laps; driver photo cards via dynamic image URLs
- Team Analysis — Constructor wins, points trends, logo cards
- Circuit Analysis — Race counts by country, circuit lengths, average speeds


Technical highlights:
- \N null handling fixed in Power Query via Replace Values
- DAX measures for Wins, Podiums, Poles, Fastest Laps, Position Groups, Top Driver/Constructor
- Image tables using GitHub raw URLs with bidirectional cross-filter
- Custom circuit_lengths.csv (49 circuits) joined via circuitRef



#Tools & Libraries
- R: tidyverse, ggplot2, plotly, dplyr, lubridate, kableExtra, patchwork, corrplot, scales, countrycode
- Power BI: Power Query (M), DAX, custom visuals
- Data: Kaggle F1 Dataset


#Key Findings

- Lewis Hamilton (105 wins) and Michael Schumacher (91 wins) are the sport's all-time top winners, but Max Verstappen's rise into the top 3 signals a dominant new era
- Pole position converts to a race win roughly 40% of the time — a significant but far from guaranteed advantage
- Starting grid position and final race position show a moderate positive correlation, with front-row starters finishing in the top 3 at a much higher rate than midfield starters
- Mechanical reliability has improved dramatically: DNF rates for 1950s–60s drivers exceeded 60%, versus under 15% in the modern hybrid era
- The Baku City Circuit stands out as one of the most unpredictable tracks on the calendar, with a high safety car rate and non-pole winners dominating results
- Drivers aged 25–30 show the best average finishing positions, with performance declining gradually after 33


#Notes
- The .pbix file requires Power BI Desktop to open
- The HTML report can be viewed directly in any browser without R installed
- All local file paths in the .Rmd have been replaced with relative paths in the published version




