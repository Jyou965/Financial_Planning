# Financial_Planning

This is a prototype application for financial planning purposes.  It accomplishes two things: 
1. Evaluating a person's emergency funding level. 
2. Assessing a person's retirement-readiness.
With this application, the financial planner can produce conclusions speedily for his/her clients.

---

## Libraries and Dependancies

This application leverages python 3.7 with the following packages:

* [os](https://docs.python.org/3/library/os.html) - provides a portable way of using operating system dependent functionality.

* [requests](https://docs.python-requests.org/en/master/) - an elegant and simple HTTP library for Python, built for human beings.

* [json](https://docs.python.org/3/library/json.html?highlight=json#module-json) - stands for JavaScript Object Notation. It is a lightweight data interchange format inspired by JavaScript object literal syntax.

* [pandas](https://pandas.pydata.org/docs/) - an open source, BSD-licensed library providing high-performance, easy-to-use data structures and data analysis tools for the Python programming language.

* [dotenv](https://pypi.org/project/python-dotenv/) - reads key-value pairs from a .env file and can set them as environment variables.

* [alpaca_trade_api](https://github.com/alpacahq/alpaca-trade-api-python/) - a python library for the Alpaca Commission Free Trading API. It allows rapid trading algo development easily, with support for both REST and streaming data interfaces.

* [MCForecastTools](https://pbpython.com/monte-carlo.html) - a set of forecasting tools under the Monte Python approach that can produce a better understanding of the range of potential outcomes and help avoid the “flaw of averages”.

* [%matplotlib](https://matplotlib.org/) - a comprehensive library for creating static, animated, and interactive visualizations in Python.

---

## Usage

The application evaluates a sample personal portfolio that consists of the traditional stock/bond component and the relatively new asset class of crypto currencies.  It assesses how well a person is position in terms of covering emergencies and evaluates whether the position will be able to retire in ten years.  The evaluation is done in the following steps: 

1. Evaluate the Emergency Funding Level
    
    a. Use API to pull the closing prices on a specified day of each of the crypto asset holdings and calculate the market value of each crypto asset holding;

    b. Use SDK to pull the closing prices on a specified day of each of the bond holding(s) and stock holding(s). Then calculate the market value of each holding;

    c. Use a pie chart to display the total portfolio breakdown between crypto assets and the traditional stock/bond assets:

    ![portfolio_pie_chart](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/pie_chart.png)

    d. Consider emergency funding threshold as three months of income.  Assess if the total portfolio market value is greater than, equal to or less than the threashold.  Advise the client accordingly.

2. Assessing Retirement-readiness

    Due to the high volatility of crypto assets, retirement planning analysis based on the traditional stock/bond portion of the total portfolio only.

    a. Set the traditional portfolio mix to 60% in stocks and 40% in bonds.  Use the past ten years of pricing data to forecast the value of the traditional portfolio in 30 years with Monte Carlo simulation.  Display the simulation results in the following manners:

![line_30](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/line_30.png)

![hist_30](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/hist_30.png)

![stats_30](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/stats_30.png)

    b. Set the portfolio mix to 80% in stocks and 20% in bonds, forecast the value of the traditional portfolio in 10 years in the same approach.  Display the simulation results in the following manners:

![line_10](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/line_10.png)

![hist_10](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/hist_10.png)

![stats_10](https://github.com/Jyou965/Financial_Planning/blob/main/Code/Images/stats_10.png)

    c. Assess if the client can retire in ten years under the more aggressive portfolio mix and advise accordingly.

With this application, the financial advisor can get straight to the conclusions of these critical assessments for clients speedily.

---

## Contributors

Jackie You with the support of FinTech Boot Camp Staff

---

## License

Berkeley