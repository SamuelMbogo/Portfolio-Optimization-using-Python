# Portfolio-Optimization-using-Python
### Author: Sam Mbogo

## Business Understanding
An investor in the stock market is after two things, which unfortunately, are mutually exclusive. High returns and low risk. Most stocks that yield high returns have an equally high volatility that scares away potential investors. Investment managers offer their services and encourage their clients to trust their judgement skills derived from industry experience.

In numerous cases, this works. However, what if a tool is developed that can aid investment managers and investors who are hands-on to manage their risk using already available historical stock prices to guide their decision making.

When working on this, I had just the thought in mind. Removing the tedious and repetitive tasks that overwhelm a trader and sometimes pushes him to guess. Using python to automate retrieving stock prices and leveraging on sharpe's ratio,  I built a simple analysis tool that can help any trader or investment manager to determine which stock is worth investing and how much to invest in each stock given a fixed amount of capital to start with.

Investors in the stock market are in need of a means to optimize their portfolios to maximize their returns while at the same time, taking on as little risk as possible.
## Data Understanding
Stock price data is imported from YahooFinance.
The analysis covered the period from 01/01/2019 to 17/10/2022. This is 956 rows of daily historical stock prices.
Our main interest is in the Adjusted Closing Price.
## Data Analysis
 Of the $10,000 used, the initial assumption is all 4 stocks are allocated an equal share, i.e., $2,500.
 ![image](https://user-images.githubusercontent.com/65402834/197453144-b59d0177-8b23-460c-8cbf-72700398506f.png)
As noted in the image above, the total value of our portfolio grows from 2019 and peaks at the beginning of 2022, at approximately $45,000. However the vaue drops sharply as we near the present.
![image](https://user-images.githubusercontent.com/65402834/197452740-866e329c-619f-4d15-9ab8-9c2a2a95a2ab.png)
Individually, we notice returns from Advanced Micro Devices rakes in the highest returns in the beginning of 2022, but also records the sharpest decline as at the most recent date in our analysis.

### Sharpe Ratio
This is a a risk-adjusted return metric. The sharpe ratio helps us quantify how much return we are getting by a given level of risk. When comparing two different investments against the same benchmark, the asset with the higher Sharpe ratio provides a higher return for the same amount of risk or the same return for a lower risk than the other asset. It is calculated by the average return of the portfolio minus a risk free rate (such as government bonds), divided by the standard deviation of the return. In this case, we assume the risk-free rate is close to zero, so we won't add it to the formula.

The average daily return is 0.1281 % while that of the standard deviation is  2.1738 %.

The annualized Sharpe ratio of our portfolio is 0.93. This means investors can reasonably expect 0.93 units of return for every 1 unit of volatility. 

## Conclusion
As of 18/10/2022, after running 10,000 simulations the optimal Sharpe Ratio is 1.18975 and Optimal Portfolio Allocation is:

| Stock  | Allocation |
| ------------- | ------------- |
| Apple  | 88.952%  |
| Advanced Micro Devices  | 5.024%  |
| Microsoft  | 4.857%  |
| Amazon  | 1.165%  |


## Recommendations
Investors in the stock market are in need of a means to optimize their portfolios to maximize their returns while at the same time, taking on as little risk as possible.
 I would recommend to substitute Amazon shares to something more profitable.
## Limitations
This portfolio optimization notebook analyzed 4 US stocks: Apple, AMD, Microsoft and Amazon. The annualized Sharpe ratio was 0.93. This is an inadequate risk/return profile.
### Drawbacks of using Sharpe's Ratio
Statistical analysis is never perfect and investors should be cautious when using the Sharpe Ratio to make investment decisions.

First, although the Sharpe Ratio is often defined as measuring “risk-adjusted returns”, the Sharpe Ratio actually measures volatility of returns, not necessarily “risk”. For example, an investment with no drawdowns might have a lower Sharpe Ratio than another investment that has had several losing months. The reason is that the Sharpe Ratio calculation penalizes volatility; if the first investment has never had loss but returns are volatile, the Sharpe Ratio will be lower than an investment with more consistent returns.

Second, past performance does not guarantee future results. Even though an investment may have a high Sharpe Ratio, that does not guarantee consistent returns (low volatility) going forward. The Sharpe Ratio analyzes past performance and historical volatility. The Sharpe Ratio provides a reasonable expectation of what to expect going forward, but the future will always be uncertain and future performance can be (and often is) different than past performance.


