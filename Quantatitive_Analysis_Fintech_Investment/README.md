# Quantative_Analysis_Fintech_Investments
Evaluating four new investment options for inclusion in client portfolios


## Background:
In this evaluation, you'll assume the role of a quantitative analyst for a FinTech investing platform. This platform aims to offer clients a one-stop online investment solution for their retirement portfolios that’s both inexpensive and high quality. To keep the costs low, the firm uses algorithms to build each client's portfolio. The algorithms choose from various investment styles and options.

You've been tasked with evaluating four new investment options for inclusion in the client portfolios. Legendary fund and hedge-fund managers run all four selections. (People sometimes refer to these managers as whales because of the large amount of money that they manage). You’ll need to determine the fund with the most investment potential based on key risk-management metrics: the daily returns, standard deviations, Sharpe ratios, and betas.

## What you are creating:
1.  a Jupyter notebook that contains your data preparation, analysis, and visualizations for key risk and return metrics. Use text and comments to document your findings and demonstrate analysis. Specifically, this file should contain the following:
    1. A single DataFrame imported from a CSV file that has a DateTimeIndex.
    2. A risk analysis of the assets that the DataFrame contains vs. the S&P 500. This analysis should include risk-return metrics, including the daily returns, standard  deviation, Sharpe ratio, and beta.
    3. An evaluation of each asset that uses rolling statistics to track the risk-reward behavior over time.

## Instructions
To start off, import a CSV file and prepare your daily returns DataFrame for analysis. Then, do a quantitative analysis that includes the following:
1. Performance
2. Volatility
3. Risk
4. Risk-return profile
5. Portfolio diversification

## Step 1: Analyze the Performance
Analyze the data to determine if any of the portfolios outperform the broader stock market, which the S&P 500 represents. To do so, complete the following steps:
1. Use the default Pandas plot function to visualize the daily return data of the four fund portfolios and the S&P 500. Be sure to include the title parameter, and adjust the figure size if necessary.
2. Use the Pandas cumprod function to calculate the cumulative returns for the four fund portfolios and the S&P 500. Review the last five rows of the cumulative returns DataFrame by using the Pandas tail function.
3. Use the default Pandas plot to visualize the cumulative return values for the four funds and the S&P 500 over time. Be sure to include the title parameter, and adjust the figure size if necessary.
4. Answer the following question: Based on the cumulative return data and the visualization, do any of the four fund portfolios outperform the S&P 500 Index?

## Step 2: Analyze the Volatility

Analyze the volatility of each of the four fund portfolios and of the S&P 500 Index by using box plots. To do so, complete the following steps:
1. Use the Pandas plot function and the kind="box" parameter to visualize the daily return data for each of the four portfolios and for the S&P 500 in a box plot. Be sure to include the title parameter, and adjust the figure size if necessary.
2. Use the Pandas drop function to create a new DataFrame that contains the data for just the four fund portfolios by dropping the S&P 500 column. Visualize the daily return data for just the four fund portfolios by using another box plot. Be sure to include the title parameter, and adjust the figure size if necessary. (Save this new DataFrame—the one that contains the data for just the four fund portfolios. You’ll use it throughout the analysis.)
3. Answer the following question: Based on the box plot visualization of just the four fund portfolios, which fund was the most volatile (with the greatest spread) and which was the least volatile (with the smallest spread)?

## Step 3: Analyze the Risk
Evaluate the risk profile of each portfolio by using the standard deviation and the beta. To do so, complete the following steps:
1. Use the Pandas std function to calculate the standard deviation for each of the four portfolios and for the S&P 500. Review the standard deviation calculations, sorted from smallest to largest.
2. Calculate the annualized standard deviation for each of the four portfolios and for the S&P 500. To do that, multiply the standard deviation by the square root of the number of trading days. Use 252 for that number.
3. Use the daily returns DataFrame and a 21-day rolling window to plot the rolling standard deviations of the four fund portfolios and of the S&P 500 index. Be sure to include the title parameter, and adjust the figure size if necessary.
4. Use the daily returns DataFrame and a 21-day rolling window to plot the rolling standard deviations of only the four fund portfolios. Be sure to include the title parameter, and adjust the figure size if necessary.
5. Answer the following three questions:
    1. Based on the annualized standard deviation, which portfolios pose more risk than the S&P 500?
    2. Based on the rolling metrics, does the risk of each portfolio increase at the same time that the risk of the S&P 500 increases?
    3. Based on the rolling standard deviations of only the four fund portfolios, which portfolio poses the most risk? Does this change over time?

## Step 4: Analyze the Risk-Return Profile
To determine the overall risk of an asset or portfolio, quantitative analysts and investment managers consider not only its risk metrics but also its risk-return profile. To do so, complete the following steps:
1. Use the daily return DataFrame to calculate the annualized average return data for the four fund portfolios and for the S&P 500. Use 252 for the number of trading days. Review the annualized average returns, sorted from lowest to highest.
2. Calculate the Sharpe ratios for the four fund portfolios and for the S&P 500. To do that, divide the annualized average return by the annualized standard deviation for each. Review the resulting Sharpe ratios, sorted from lowest to highest.
3. Visualize the Sharpe ratios for the four funds and for the S&P 500 in a bar chart. Be sure to include the title parameter, and adjust the figure size if necessary.
4. Answer the following question: Which of the four portfolios offers the best risk-return profile? Which offers the worst?

## Step 5: Diversify the Portfolio
Your analysis is nearing completion. Now, evaluate how the portfolios react relative to the broader market. Based on your analysis so far, choose two portfolios that you’re most likely to recommend as investment options. To start your analysis, complete the following step:
1. Use the Pandas var function to calculate the variance of the S&P 500 by using a 60-day rolling window. Visualize the last five rows of the variance of the S&P 500.
2. Next, for each of the two portfolios that you chose, complete the following steps:
    1. Using the 60-day rolling window, the daily return data, and the S&P 500 returns, calculate the covariance. Review the last five rows of the covariance of the portfolio.
    2. Calculate the beta of the portfolio. To do that, divide the covariance of the portfolio by the variance of the S&P 500.
    3. Use the Pandas mean function to calculate the average value of the 60-day rolling beta of the portfolio.
    4. Plot the 60-day rolling beta. Be sure to include the title parameter, and adjust the figure size if necessary.
3. Answer the following two questions:
    1. Which of the two portfolios seem more sensitive to movements in the S&P 500?
    2. Which of the two portfolios do you recommend for inclusion in your firm’s suite of fund offerings?
    
Congratulations, you've completed the activity!

