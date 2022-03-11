#### Data Cleaning

##### Harold's company has been investing in algorithmic trading strategies. Some of the investment managers love them, some hate them, but they all think their way is best.

#### I have created a tool (an analysis notebook) that analyzes and visualizes the major metrics of the portfolios across all of these areas, and determine which portfolio outperformed the others. The firm's algorithmic portfolios, some that represent the portfolios of famous "whale" investors like Warren Buffett, and some from the big hedge and mutual funds. I will then use this analysis to create a custom portfolio of stocks and compare its performance to that of the other portfolios, as well as the larger market (S&P 500 Index).

#### Prepare the Data

##### First, I read and cleand several CSV files for analysis. The CSV files include whale portfolio returns, algorithmic trading portfolio returns, and S&P 500 historical prices. Here is an analysis starter Code to complete the following steps:


##### 1 Use Pandas to read the following CSV files as a DataFrame. Be sure to convert the dates to a DateTimeIndex.


   ##### whale_returns.csv: Contains returns of some famous "whale" investors' portfolios.


   ##### algo_returns.csv: Contains returns from the in-house trading algorithms from Harold's company.


   ##### sp500_history.csv: Contains historical closing prices of the S&P 500 Index.




##### 2 I Detectd and removed null values.


##### 3 If any columns havd dollar signs or characters other than numeric values, I have removed those characters and convert the data types as needed.


##### 4 The whale portfolios and algorithmic portfolio CSV files contain daily returns, but the S&P 500 CSV file contains closing prices. I converted the S&P 500 closing prices to daily returns.


##### 5 I joined Whale Returns, Algorithmic Returns, and the S&P 500 Returns into a single DataFrame with columns for each portfolio's returns.

#### 6 From the financial analysis done on the Whale, Algorithmic, and S&P 500 Returns using the Sharpe Ratio and Box Plot. The S&P 500 out preforms the Whale and Algorithmic portfolios.