## 1. Dataset Description

-   The dataset Big Tech Stock Prices, which is upload tidytuesday repository on Feb 7th 2023, comes from Yahoo Finance via Kaggle (by Evan Gower). This dataset consists of the daily stock prices and volume of 14 different tech companies

## Data Dictionary

-   There are 2 main csv file:

### `big_tech_stock_prices.csv`

-   The file includes 15 samples mapping between stock symbol and companies' names

| variable     | class     | description                                                                                                                                                                                                                       |
|:-------------------------|:-------------------|:-------------------------|
| stock_symbol | character | stock_symbol                                                                                                                                                                                                                      |
| date         | double    | date                                                                                                                                                                                                                              |
| open         | double    | The price at market open.                                                                                                                                                                                                         |
| high         | double    | The highest price for that day.                                                                                                                                                                                                   |
| low          | double    | The lowest price for that day.                                                                                                                                                                                                    |
| close        | double    | The price at market close, adjusted for splits.                                                                                                                                                                                   |
| adj_close    | double    | The closing price after adjustments for all applicable splits and dividend distributions. Data is adjusted using appropriate split and dividend multipliers, adhering to Center for Research in Security Prices (CRSP) standards. |
| volume       | double    | The number of shares traded on that day.                                                                                                                                                                                          |

### `big_tech_companies.csv`

-   The file includes 45,089 samples (3721 for each company except Tesla and Meta because they were not publicly traded for part of the period examined) containing details of stock prices ( open price, close price, etc.)

| variable     | class     | description               |
|:-------------|:----------|:--------------------------|
| stock_symbol | character | stock_symbol              |
| company      | character | Full name of the company. |

## 2. Motivation

-   **Rich of samples** : This dataset not only meet all requirements of the project 1 (new, contain both numerical and categorical features) but also includes a large number (\~45,000) of samples for stock prices which can generalize the distribution of features. Moreover, we can also learn about data preprocessing through this dataset because that number of samples might requires some modification for better visualization.
-   **Interesting pattern in stock price**: Because stock price is famous for its fluctuation, visualizing this dataset may help us acknowledge many interesting patterns as well as rules in stock price change.
-   **This dataset can be used for multiple purposes**: We agree that there are many application of this dataset, for example, used for **predictive machine learning model projects**. It means that the knowledge of this dataset is not limited in this project, so that it has a wider functionality.

## 3. 

- **Detailed Trend Analysis for Individual Companies** :  How has each company's stock price trended over a specific period (e.g., the past decade), and how do these trends vary among companies like Apple Inc. (AAPL), Amazon.com, Inc. (AMZN), and Microsoft Corp. (MSFT)?

  Why: This question allows us to dive deep into the performance of individual tech giants, uncovering how product launches, global events, and market trends have impacted their stock prices over time. It provides a historical perspective that can be crucial for understanding future potential.

- **Comparative Growth Analysis Since a Key Historical Event** : Since a significant market event (e.g., the COVID-19 pandemic outbreak in early 2020), how have the stock prices of these tech giants recovered and grown, and how does their recovery and growth compare?

Why: This question is particularly relevant given the recent global events that have significantly impacted markets. It provides insight into the resilience and growth potential of big tech companies in the face of adversity, offering a comparative analysis of how different companies withstand and thrive following market shocks.
