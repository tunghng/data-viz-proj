# Big Tech Stock Prices Dataset Overview

## Dataset Description

The dataset, named **Big Tech Stock Prices**, was uploaded to the TidyTuesday repository on February 7th, 2023. It is sourced from Yahoo Finance via Kaggle, courtesy of Evan Gower. This dataset comprises daily stock prices and volume for 14 different tech companies.

## Data Dictionary

There are 2 main CSV files in this dataset:

### `big_tech_stock_prices.csv`

This file contains 15 samples mapping between stock symbol and companies' names, with the following variables:

| Variable    | Class     | Description                                                                                                                                                                                                                        |
|-------------|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| stock_symbol| character | The stock symbol of the company.                                                                                                                                                                                                   |
| date        | double    | The date on which the stock data was recorded.                                                                                                                                                                                     |
| open        | double    | The price of the stock at the market open.                                                                                                                                                                                         |
| high        | double    | The highest price of the stock on that day.                                                                                                                                                                                        |
| low         | double    | The lowest price of the stock on that day.                                                                                                                                                                                         |
| close       | double    | The closing price of the stock, adjusted for splits.                                                                                                                                                                               |
| adj_close   | double    | The closing price after adjustments for splits and dividend distributions, adhering to CRSP standards.                                                                                                                              |
| volume      | double    | The number of shares traded on that day.                                                                                                                                                                                           |

### `big_tech_companies.csv`

This file contains 45,089 samples, detailing stock prices (open price, close price, etc.) for each company, except for Tesla and Meta, which were not publicly traded for part of the period examined.

| Variable    | Class     | Description                  |
|-------------|-----------|------------------------------|
| stock_symbol| character | The stock symbol of the company. |
| company     | character | The full name of the company.    |

## Motivation

The dataset is highly valuable for several reasons:

- **Richness of Samples**: With approximately 45,000 samples, it meets all the requirements for project 1 (being new, containing both numerical and categorical features), and can generalize the distribution of features. It also offers insights into data preprocessing due to the large number of samples.
- **Interesting Patterns in Stock Prices**: Given the fluctuating nature of stock prices, visualizing this dataset can reveal patterns and rules in stock price changes.
- **Multiple Purposes**: This dataset has broad applications, such as predictive machine learning models, making it a versatile resource beyond just this project.

## Questions to Answer

### Detailed Trend Analysis for Individual Companies

**Question**: How have the stock prices of individual companies like Apple Inc. (AAPL), Amazon.com, Inc. (AMZN), and Microsoft Corp. (MSFT) trended over specific periods (e.g., the past decade)?

**Why**: This analysis offers insights into the performance of these tech giants, how product launches and global events have influenced their stock prices, and provides a historical perspective essential for predicting future trends.

**Plan for Question 1**:

- **Variables Involved**:
  - `stock_symbol` (character): To filter data for companies of interest.
  - `date`, `close`, `volume` (double): For selecting date ranges and analyzing closing prices and trade volume.

- **Variables to be Created**:
  - `percent_change`: To show daily or periodical stock price changes.
  - `moving_average`: For smoothing out short-term fluctuations.

- **External Data**:
  - Key event dates for each company.
  - Historical market indices for comparative performance.

- **Analysis Plan**:
  1. Filter data for targeted companies and date ranges.
  2. Create time-series data for closing prices.
  3. Calculate additional variables like percent changes.
  4. Merge key event dates and market indices.
  5. Use charts to visualize trends.

### Comparative Growth Analysis Since a Key Historical Event

**Question**: How have the stock prices of tech giants recovered and grown since the COVID-19 pandemic outbreak, and how do their recoveries compare?

**Why**: This analysis is pertinent due to the significant impact of recent global events on markets, providing insights into the resilience and growth potential of big tech companies.

**Plan for Question 2**:

- **Variables Involved**:
  - `stock_symbol`, `date`, `close` (double): For identifying companies and analyzing closing prices post-pandemic.

- **Variables to be Created**:
  - `indexed_price`: For direct comparison of stock prices indexed at the pandemic's start.
  - `time_to_recovery`: To measure the time for stock prices to return to pre-pandemic levels.

- **External Data**:
  - Major economic indicators and policy change dates.

- **Analysis Plan**:
  1. Filter for companies from the start of the pandemic.
  2. Normalize stock prices
