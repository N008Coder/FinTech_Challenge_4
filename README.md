# FinTech_Challenge_4
Analyzing hedge-fund performance relative to the S&P by using Sharpe Ratios and Beta

We start by using pandas read_csv to bring in the data we'll be working with
    We then use pandas pct_change to calculate daily returns and be able to compare across funds. We use dropna() to clean the data a bit and remove the N/A lines from the 1st row
We plot the daily returns to visualize them
    We can calculate and plot the cumulative returns to better visualize the total performance of the funds aross the given time period
We then can map the cumulative returns on a box plot to visualize the spread of the data
    We can also do this looking at just the 4 funds and excluding the S&P to better see the differences between funds. The S&P has a large spread, making it harder to see the differences between the other funds.
We then use Standard Deviation as a measure of risk of the portfolios
    Annualizing the standard deviation gives us info on how wide the spread is across a year-long time-span
    We then plot a 21-day rolling window (to smoothen out the data) of the standard deviations to visualize how the volatility changes over time
        We then do the same, excluding the S&P. This gives us a better comparison of the funds' volatility since the S&P's std is somewhat outsized relative to the funds
We then annualize the average daily returns and use that in conjunction with the annualized std to get a Sharpe Ratio for each fund. This measure of risk takes more factors into account.
    We can then plot the Sharpe ratios on bar plots for an easy visual comparison
Lastly, we calculate Variance and Covariance over a 60-day window so that we can then calculate a smoothed out Beta for each fund and use that as another measure of risk.
    We look at the Beta of the funds with the highest and lowest Sharpe Ratios. See the code for results!


Technologies: Python 3.7.11 pandas 1.3.4, mathplotlib 0.1.2, pathlib

Installation Guide: Make sure you have the dependencies installed

Contributors: Berkeley FinTech Extension Course for the starer code https://bootcamp.berkeley.edu/fintech/ Gabriel Paganin filled in the gaps gpaganin@berkeley.edu www.linkedin.com/in/gabriel-paganin