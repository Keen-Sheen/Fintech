# Background

![An image of buildings](singapore_buildings.jpg)

You decided to start a FinTech consultancy firm, and you want to make a difference by working on projects with high social impact in local communities. You just won your first contract to help one of the biggest credit unions in your area. They want to create a tool that helps their members enhance their financial health. The Chief Technology Officer (CTO) of the credit union asked you to develop a prototype application to demo in the next credit union assembly.
The credit union board wants to allow the union's members to assess their monthly personal finances, and also be able to forecast a reasonably good retirement plan based on cryptocurrencies, stocks, and bonds.
In this homework activity, you will use all the skills you have learned until now - focusing on using APIs as part of the technical solution - to create two financial analysis tools.

The first will be a personal finance planner that will allow users to visualize their savings composed by investments in shares and cryptocurrencies to assess if they have enough money as an emergency fund.
The second tool will be a retirement planning tool that will use the Alpaca API to fetch historical closing prices for a retirement portfolio composed of stocks and bonds, then run Monte Carlo simulations to project the portfolio performance at 30 years. You will then use the Monte Carlo data to calculate the expected portfolio returns given a specific initial investment amount.

The second tool will be a retirement planning tool that will use the Alpaca API to fetch historical closing prices for a retirement portfolio composed of stocks and bonds, then run Monte Carlo simulations to project the portfolio performance at 30 years. You will then use the Monte Carlo data to calculate the expected portfolio returns given a specific initial investment amount.

---------------------------------------------------------------------------------------------------------

# Resources
This homework will utilize two APIs:


* The Alpaca Markets API will be used to pull historical stocks and bonds information.


* The Alternative Free Crypto API will be used to retrieve Bitcoin and Ethereum prices.


* The documentation for these APIs can be found via the following links:


[Free Crypto API Documentation](https://alternative.me/crypto/api/)


[AlpacaDOCS](https://alpaca.markets/docs/)

-----------------------------------------------------------------------------------------------------------

Instructions
-------------------------------------------------------------------------------------------------

# Part 1 - Personal Finance Planner

In this section of the challenge, you will create a personal finance planner application. To develop the personal finance planner prototype, you should take into account the following assumptions:


* The average household income for each member of the credit union is $12,000.


* Every union member has a savings portfolio composed of cryptocurrencies, stocks and bonds:


  * Assume the following amount of crypto assets: 1.2 BTC and 5.3 ETH.


   * Assume the following amount of shares in stocks and bonds: 50 SPY (stocks) and 200 AGG (bonds).




Use the starter Jupyter notebook to complete the following steps.

Collect Crypto Prices Using the` requests` Library


1. Create two variables called `my_btc` and `my_eth`. Set them equal to `1.2` and `5.3`, respectively.


2. Use the `requests` library to fetch the current price in US dollars of bitcoin (`BTC`) and ethereum (`ETH`) using the Alternative Free Crypto API endpoints provided in the starter notebook.


3. Parse the API JSON response to select only the crypto prices and store each price in a variable.

Hint: Be aware of the particular identifier for each cryptocurrency in the API JSON response - the bitcoin identifier is `1` whereas ethereum is `1027`.


4. Compute the portfolio value of cryptocurrencies and print the results.



Collect Investments Data Using Alpaca: SPY (stocks) and AGG (bonds)

Important: Remember to create a `.env` file in your working directory to store the values of your Alpaca API key and Alpaca secret key.


1. Create two variables named `my_agg` and `my_spy` and set them equal to 200 and 50, respectively.


2. Set the Alpaca API key and secret key variables, then create the Alpaca API object using the `tradeapi.REST` function from the Alpaca SDK.


3. Format the current date as ISO format. You may change the date set in the starter code to the current date.


4. Get the current closing prices for `SPY` and `AGG` using Alpaca's `get_barset()` function. Transform the function's response to a Pandas DataFrame and preview the data.


5. Pick the `SPY` and `AGG` close prices from the Alpaca's `get_barset()` DataFrame response and store them as Python variables. Print the closing values for validation.


6. Compute the value in dollars of the current amount of shares and print the results.

Savings Health Analysis

In this section, you will assess the financial health of the credit union's members.


1. Create a variable called monthly_income and set its value to 12000.


2. To analyze savings health, create a DataFrame called df_savings with two rows. Store the total value in dollars of the crypto assets in the first row and the total value of the shares in the second row.

Hint: The df_savings DataFrame should have one column named amount and two rows where crypto and shares are the index values:















