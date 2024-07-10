# Data Analyst Intern - Sportradar Challenge
# Sportradar Data Analysis Project

## Overview

This project is a comprehensive analysis of programmatic advertising data and the impact of the 2022 World Cup on advertising metrics. The work is divided into three main tasks: analyzing ad impressions and conversions, generating insights from the World Cup 2022 data, and preparing a presentation to summarize the findings.

## Table of Contents
1. [Introduction](#introduction)
2. [Data Description](#data-description)
3. [Task 1: Programmatic Advertising Analysis](#task-1-programmatic-advertising-analysis)
4. [Task 2: World Cup 2022 Analysis](#task-2-world-cup-2022-analysis)
5. [Task 3: Presentation](#task-3-presentation)
6. [Usage](#usage)
7. [Conclusion](#conclusion)

## Introduction

The goal of this project is to leverage data analysis to provide insights into programmatic advertising and understand the impact of major sporting events, specifically the World Cup 2022, on advertising metrics. The analysis aims to help stakeholders make informed decisions to optimize ad spend and improve conversion rates.

## Data Description

The project uses three primary datasets with the following schemas:

- **impressions**
  - impression_id: string
  - url_address: string
  - user_id: string
  - request_country: string
  - tracking_type: string (fingerprinted or cookie-based)
  - dynamic_display: boolean
  - dynamic_display_variables: string
  - request_browser_name: string
  - timestamp: date

- **clicks**
  - impression_id: int
  - user_id: int
  - timestamp: string

- **conversions**
  - conversion_id: string
  - user_id: string
  - dval: integer (deposit value)
  - curr: string (currency)
  - timestamp: date

## Task 1: Programmatic Advertising Analysis

1. **CTR Calculation for Austria:**
   - Calculate the Click-Through Rate (CTR) for impressions served in Austria.
   - Formula: `CTR (%) = (Number of Clicks / Number of Impressions) * 100`

2. **Impressions for Converted Users:**
   - For each user who converted, calculate the number of impressions served.
   - Capture the timestamps of the first and last impressions for each converted user.

3. **Additional Insights:**
   - Identify patterns or trends that might be of interest to stakeholders.
   - Consider factors like browser usage, dynamic display impact, and tracking types.

## Task 2: World Cup 2022 Analysis

1. **Largest Reduction in CPA:**
   - Identify countries with the largest reduction in Cost Per Acquisition (CPA) during the World Cup compared to other periods.
   - Metrics analyzed include CPC (Cost Per Click), CPV (Cost Per View), CTR (Click Through Rate), ROAS (Return on Ad Spend), and ROI (Return on Investment).

2. **Client Insights:**
   - Generate insights to encourage clients to invest more in advertising during major sporting events.
   - Highlight the potential increase in conversions and reduction in costs during these periods.

3. **Adapting Analysis for Euro 2024:**
   - Discuss how the analysis could be adapted for Euro 2024.
   - Identify relevant metrics and insights specific to this event.

## Task 3: Presentation

Prepare a presentation summarizing the findings from Tasks 1 and 2. The presentation should be structured to highlight key insights and actionable recommendations. Aim for a 10-minute duration, covering the following points:

- Overview of data and methodology
- Key findings from programmatic advertising analysis
- Insights from World Cup 2022 data
- Recommendations for future advertising strategies
- Adaptation plan for Euro 2024 analysis

## Usage

To run the analysis and generate the plots, follow these steps:

1. **Install Dependencies:**
   Ensure you have the required libraries installed. You can use the following command to install them:
   ```bash
   pip install numpy pandas matplotlib
Run the Analysis:
Execute the provided Python scripts to perform the analysis for each task. For example, to plot the top 10 comparisons:

python
Copy code
for df, metric in zip(comparisons_df, metrics):
    plot_top_10_comparison_absolute_change(df, metric)
