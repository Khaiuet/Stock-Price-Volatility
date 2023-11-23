[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
# Stock-Price-Trend-olatility

## Project Overview

The goal of this project is to develop a predictive model for stock price volatility across multiple stock tickers. Utilizing price and trading volume data for various stock symbols, the project aims to create models that can forecast stock price movements.

Our research question is: are Google Trends search interest volatility related to stock return volatility? Consider this project a screening exercise for whether Google Trends could be useful in volatility-based trading strategies.

In order to assess the association between stock return volatility and search trend volatility, we analyse the standard deviation of weekly search trends and weekly returns for over 300 stocks in the S&P 500 over a one-year period from July 2020 to July 2021. We conduct a simple linear regression with a confidence level of 0.95 with the return volatility as the dependent variable and search trends volatility as the independent variable. Our null hypothesis is that there is no association between the two volatilities, with the alternative being that there is an association.

Ultimately, we find a significant coefficient of trend volatility and reject the null hypothesis in favour of the alternative. The R\^2 value indicates that our simple model is explaining very little of the variation in return volatility. Moreover, the effect size seems to be fairly small in relation to the range of return volatility that we observe in the data. These caveats are to be expected considering we are using a very simple model to understand markets which contain lots of complexity. Nonetheless, this positive result is exciting and warrants future investigation into the use of Google Trends for Financial Analysis.

\*\*Note that in statistical terms, the volatility is simply the standard deviation of returns. <https://www.investopedia.com/terms/v/volatility.asp>

## Report

The final report can be found [here](https://ubc-mds.github.io/Stock-Price-Trend-Volatility-Analysis/doc/Stock_Price_Trend_Volatility_Analysis_report.html)

## Executing the Analysis

Reproducibility of results is of utmost importance in data science. In this section, we provide steps for executing our analysis.

### Dependencies

Firstly, please ensure that your python and R environments have installed the following dependencies:

python dependencies:
  - altair>=4.1.0
  - altair_data_server>=0.4.1
  - altair_saver>=0.5.0
  - pandas>=1.3.4
  - pandas-profiling>=3.1.0
  - requests>=2.26.0
  - selenium>=3.141.0
  - docopt>=0.6.2
  - pip

  R dependencies:
  - tidyverse 1.3.1
  - docopt 0.7.1
  - stargazer 5.2.2

  Additionally you could use the env.yaml and R_dependencies files.
  
### Dependency diagram

<img src="Makefile.png" alt="drawing" style="height:60px;"/>

Click [here](https://ubc-mds.github.io/Stock-Price-Trend-Volatility-Analysis/Makefile.png) for a bigger view.

### Process flow chart

The following figure may be helful to visualize the steps of the analysis

![Flow chart](doc/processing-flowchart.png)

### Execution of scripts

IMPORTANT NOTE

Downloading the data will take several hours to run. We suggest instead skipping to step 4 and using the pre-downloaded data in our repository.

#### Automated download of stock return and trend data

1.  Open your terminal and navigate to the src folder of the project that you have forked and cloned.

Execute the following .py files, noting that full download will take several hours.

As we are utilizing the Selenium library to automate the files download process, make sure you have the latest Google Chrome and Chrome Driver installed on your system. Please note the automation will run in a headless chrome browser and we strongly advise not to reduce the time.sleep in any of the files.

Stock tickers are extracted automatically from the `SP500.csv` file located in the data folder of this project.

for Yahoo Finance:

`yf-file-downloader-source.py`

Stock Price Volatility Analysis
License: MIT

Project Overview
The primary objective of this project is to construct a predictive model for stock price volatility across multiple stock tickers. Leveraging price and trading volume data for various stock symbols, the project aims to develop models capable of forecasting stock price movements.

The central research question explores the potential correlation between Google Trends search interest volatility and stock return volatility. This project serves as a preliminary investigation to determine whether Google Trends could be valuable in volatility-based trading strategies.

To assess the association between stock return volatility and search trend volatility, we analyze the standard deviation of weekly search trends and weekly returns for over 300 stocks in the S&P 500 over a one-year period from July 2020 to July 2021. A simple linear regression is conducted with a confidence level of 95%, treating return volatility as the dependent variable and search trends volatility as the independent variable. The null hypothesis posits no association between the two volatilities, with the alternative suggesting an association.

Our findings reveal a significant coefficient of trend volatility, leading us to reject the null hypothesis in favor of the alternative. However, the R² value indicates that our simple model explains only a small portion of the variation in return volatility. Furthermore, the effect size appears relatively modest compared to the observed range of return volatility in the data. These limitations are anticipated, given the simplicity of our model in the face of the inherent complexity of financial markets. Nonetheless, this positive result sparks excitement and prompts further exploration into the potential use of Google Trends for financial analysis.

Note: In statistical terms, volatility is simply the standard deviation of returns. Learn more

Report
The final report can be accessed here.

Executing the Analysis
Reproducibility of results is crucial in data science. In this section, we provide steps for executing our analysis.

Dependencies
Ensure that your Python environment has installed the following dependencies:

seaborn>=0.11.2
plotly>=5.3.1
pandas>=1.3.4
scikit-learn>=0.24.2
Additionally, you could use the requirements.txt file.
