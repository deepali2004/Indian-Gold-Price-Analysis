# Indian Gold Price Analysis (2016–2025)

An exploratory data analysis project investigating historical gold price trends, monthly seasonality and festival-period price deviations in India using **Python, Pandas and Power BI**.

## Project Overview

Gold prices fluctuate over time due to several market and economic factors. For jewellers, understanding historical price movements can help provide context when planning inventory and stock purchases.

**GoldScope** explores ten years of historical monthly gold price data to identify whether certain calendar months have consistently recorded prices below or above their estimated long-term trend.

The project also examines broad calendar windows associated with Akshaya Tritiya, Dhanteras and the wedding season.

## Business Objective

The primary objective is to help a jewellery business understand:

- How Indian gold prices have changed between 2016 and 2025.
- Whether particular months tend to record prices below or above the estimated trend.
- How frequently each month records a below-trend price.
- Whether broad festival and wedding-season windows show noticeable deviations from the estimated trend.

**Key question:** Are there recurring calendar-month patterns that could provide useful historical context for gold stocking decisions?

## Tools & Technologies

- **Python:** Data cleaning, transformation and exploratory analysis.
- **Pandas & NumPy:** Data manipulation and calculations.
- **Matplotlib & Seaborn:** Data visualization and heatmaps.
- **Power BI:** Interactive dashboard development.
- **Microsoft Excel:** Source data inspection.

## Dataset

The analysis uses monthly historical gold price data covering **January 2016 to December 2025**, comprising 120 monthly observations.

| Attribute | Description |
|---|---|
| Gold Price | Monthly average standard gold price in Mumbai |
| Unit | INR per 10 grams |
| Frequency | Monthly |
| Analysis Period | January 2016 – December 2025 |
| Original Data Source | Bombay Bullion Association Ltd. |

*Note: The dataset represents monthly average standard gold prices in Mumbai. It should not be interpreted as daily retail jewellery prices or a national spot-price benchmark.*

## Project Workflow

### 1. Data Cleaning & Preparation

- Imported and inspected the historical dataset using Pandas.
- Converted date and price columns into appropriate data types.
- Handled missing and invalid records.
- Checked for duplicate dates and missing values.
- Filtered the dataset to the ten-year analysis period.
- Extracted year, month number and month name for further analysis.

### 2. Trend Analysis

- Examined historical gold price movements from 2016 to 2025.
- Calculated yearly average gold prices.
- Used a centred 12-month moving average to estimate the underlying trend.
- Calculated monthly deviations from the estimated trend.

**Seasonal deviation formula:**

\[
\text{Deviation (\%)} =
\frac{\text{Actual Price} - \text{Estimated Trend}}
{\text{Estimated Trend}} \times 100
\]

A negative deviation indicates that the observed price was below the estimated trend, while a positive deviation indicates that it was above the estimated trend.

### 3. Monthly Seasonality Analysis

Grouped the trend deviations by calendar month and calculated:

- Average deviation from trend.
- Median deviation from trend.
- Standard deviation.
- Number of observations.
- Number and percentage of observations below trend.

### 4. Festival & Wedding Season Analysis

Compared broad calendar-month windows associated with:

- **Akshaya Tritiya:** April–May
- **Dhanteras:** October–November
- **Wedding Season:** November–February and April–May

The comparison examines average deviation, median deviation and the frequency of below-trend observations.

These are broad calendar windows rather than exact festival-date event studies.

## Key Findings

### Historical Gold Price Movement

- The average monthly gold price across the analysis period was approximately **₹50,066 per 10 grams**.
- The lowest recorded monthly average was **₹25,998**.
- The highest recorded monthly average was **₹131,172**.
- The yearly averages show a substantial upward movement over the ten-year period.

### Monthly Seasonality

- **December** recorded the lowest average deviation from trend at approximately **-2.62%**.
- December recorded below-trend prices in 8 out of 9 observations.
- **November** recorded below-trend prices in 7 out of 9 observations.
- **April** recorded the highest average deviation at approximately **+1.49%**.

### Festival & Wedding Season Windows

| Period | Average Deviation |
|---|---:|
| Akshaya Tritiya | +1.08% |
| Dhanteras | -0.63% |
| Wedding Season | -0.52% |

Dhanteras and the wedding-season window recorded modest negative average deviations, while the Akshaya Tritiya window recorded a positive average deviation.

These findings describe historical relationships in the selected dataset and do not establish that festivals cause gold price movements.

## Power BI Dashboard

The interactive dashboard presents:

- Gold price KPIs and historical price trends.
- Monthly average deviation analysis.
- Frequency of below-trend observations.
- Year-wise and month-wise seasonality heatmap.
- Festival and wedding-season comparisons.

![GoldScope Dashboard Preview](dashboard/dashboard-preview.png)

## Repository Contents

| Folder / File | Description |
|---|---|
| `data/` | Cleaned dataset and analysis output CSV files |
| `notebooks/` | Python notebook containing data preparation and analysis |
| `dashboard/` | Power BI dashboard and preview image |
| `README.md` | Project documentation |
| `requirements.txt` | Python library dependencies |

## Conclusion

The analysis identifies some recurring differences in monthly deviations from the estimated gold price trend, particularly in November and December. However, these patterns should be interpreted cautiously because the monthly observations are limited and historical patterns may not persist.

The project demonstrates how historical data can be cleaned, analysed and transformed into meaningful business insights using Python and Power BI.

**Disclaimer:** This project is for educational and exploratory data analysis purposes only. It does not provide gold price predictions, investment recommendations or guaranteed stocking strategies.
