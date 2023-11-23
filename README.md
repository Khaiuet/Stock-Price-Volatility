# Stock Price Volatility Analysis

## Project Overview

The primary objective of this project is to construct a predictive model for stock price volatility across multiple stock tickers. Leveraging price and trading volume data for various stock symbols, the project aims to develop models capable of forecasting stock price movements.

The central research question explores the potential correlation between Google Trends search interest volatility and stock return volatility. This project serves as a preliminary investigation to determine whether Google Trends could be valuable in volatility-based trading strategies.

To assess the association between stock return volatility and search trend volatility, we analyze the standard deviation of weekly search trends and weekly returns for over 300 stocks in the S&P 500 over a one-year period from July 2020 to July 2021. A simple linear regression is conducted with a confidence level of 95%, treating return volatility as the dependent variable and search trends volatility as the independent variable. The null hypothesis posits no association between the two volatilities, with the alternative suggesting an association.

Our findings reveal a significant coefficient of trend volatility, leading us to reject the null hypothesis in favor of the alternative. However, the R² value indicates that our simple model explains only a small portion of the variation in return volatility. Furthermore, the effect size appears relatively modest compared to the observed range of return volatility in the data. These limitations are anticipated, given the simplicity of our model in the face of the inherent complexity of financial markets. Nonetheless, this positive result sparks excitement and prompts further exploration into the potential use of Google Trends for financial analysis.

# Note: In statistical terms, volatility is simply the standard deviation of returns. Learn more

# Report
The final report can be accessed here.

Executing the Analysis
Reproducibility of results is crucial in data science. In this section, we provide steps for executing our analysis.

# Dependencies
Ensure that your Python environment has installed the following dependencies:

seaborn>=0.11.2
plotly>=5.3.1
pandas>=1.3.4
scikit-learn>=0.24.2


## Authors

  - **Khai** -
    [Khaiuet](https://github.com/Khaiuet)


## License

This project is licensed under the [MIT License](LICENSE.md)
Creative Commons License - see the [LICENSE.md](LICENSE.md) file for
details

