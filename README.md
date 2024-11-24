# Super Bowl Analytics: Web Scraping and Panel Data Analysis

## Overview

This project explores the impact of Super Bowl advertising on beer sales, with a specific focus on Budweiser. The analysis combines **web scraping**, **data cleaning**, **visualization**, and **regression modeling** to estimate the return on investment (ROI) of Super Bowl commercials. The study integrates data on Super Bowl television ratings, advertising costs, and post-Super Bowl beer sales.

---

## Objectives
1. Scrape and clean Super Bowl television ratings and advertising cost data from **Wikipedia**.
2. Analyze television ratings and advertising trends over time.
3. Use panel data on beer sales to estimate the effect of Super Bowl advertisements on weekly household beer expenditures.
4. Assess the ROI of Budweiser's Super Bowl advertising campaigns.

---

## Key Insights
- The average viewership for the Super Bowl has varied over time, with a significant spike in recent years.
- CBS has aired the most Super Bowls, while Fox has the highest average TV viewership.
- Budweiser's weekly beer revenue increases significantly in markets with high Super Bowl viewership, particularly when the local team is playing.
- Super Bowl commercials provide a **positive ROI** for Budweiser, with extra revenue far exceeding advertising costs.

---

## Features and Workflow

### 1. **Web Scraping**
- Scraped Super Bowl ratings and advertising data using the `rvest` library.
- Extracted and cleaned data from HTML tables on Wikipedia.

### 2. **Data Cleaning**
- Removed unnecessary rows and columns.
- Reformatted date variables, removed unwanted text, and converted strings to numeric types.
- Aggregated viewership data to account for Super Bowls aired on multiple networks.

### 3. **Data Visualization**
- **Line Plot:** Super Bowl viewership over time.
- **Bar Plot:** Average TV viewership by network.
- **Density Plot:** Nielsen ratings for Super Bowls with and without a local team.
- **Line Plot:** Beer expenditures by brand and year.

### 4. **Regression Modeling**
- Built regression models with fixed effects to isolate the impact of Super Bowl advertisements on Budweiser's beer sales:
  - Year fixed effects
  - Brand-Year fixed effects
  - Brand-DMA fixed effects
- Evaluated the statistical significance of the treatment variable (`AdXRating`).

---

## Key Findings
1. **Super Bowl Viewership:**
   - Highest total TV viewership occurred in 2024 (121.5 million viewers).
   - Fox has the highest average TV viewership among networks.

2. **30-Second Ad Costs:**
   - The average cost of a 30-second ad during the Super Bowl from 2006 to 2011 was **\$2,722,330**.

3. **Budweiser's Revenue Boost:**
   - Weekly household beer expenditures increase significantly in markets with higher Super Bowl viewership, particularly when the local team is playing.
   - The treatment effect (`AdXRating`) accounts for **35.5%** of Budweiser's weekly revenue per household.

4. **ROI Analysis:**
   - Budweiser's extra revenue from Super Bowl ads is estimated at **\$53.56 million**, assuming an 8-week impact period.
   - Annual advertising costs for 9 Super Bowl ads total **\$33.5 million**, resulting in a **positive ROI**.

---

## Tools and Libraries
- **R Libraries:** `tidyverse`, `rvest`, `stringr`, `jtools`, `gt`, `scales`, `grafify`
- **Visualization:** `ggplot2`
- **Web Scraping:** `rvest`
- **Statistical Modeling:** Linear regression with fixed effects

---

## How to Use This Repository

### **1. Clone the Repository**
```bash
git clone https://github.com/<username>/superbowl-beer-analysis.git
cd superbowl-beer-analysis
