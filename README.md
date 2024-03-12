# 1 Dataset Description

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
