### How does stock price movement in particular sectors relate to company fundamentals, economic factors, and other market indicators

**Sanjay Kumar Hooda**

#### Executive summary
This project make investment intelligence accessible to everyone by giving everyday investors access to analytical tools traditionally reserved for professionals and research teams only. Using open-source, data-driven models, it provides risk-return profiles for 300+ stocks across major sectors including technology, healtcare, industrial, finacials, and customer discretionary. It uncovers sector-level patterns that help individuals make smarter portfolio decisions. The integrated economic analysis quantifies how factors such as interest rates, money supply, and market volatility influence sector performance—for example, how rate hikes affect financial stocks—empowering users to anticipate market movements rather than react to them. Sector-specific insights deepen this understanding by showing how industries like technology, financials, and consumer discretionary respond to different macroeconomic conditions. Predictive, time-lagged models enable proactive planning by estimating stock performance 1, 3, and 6 months ahead, while volatility and clustering analysis strengthen risk management by clarifying diversification needs, drawdown potential, and risk-tolerance alignment. By making all research transparent and open source, the project not only levels the playing field for retail investors but also educates them, allowing users to verify methods, reproduce results, and customize analyses to fit their individual financial goals.
#### Rationale
Why should anyone care about this question?
People should care about this question because  everyday investors are expected to take important financial decisions without the tools or knowledge that professional investors use. Most people managing their financial accounts don’t understand how to analyze stocks and how economic changes—like interest rates or market volatility—affect their investments. This project gives them easy-to-use, transparent analysis that helps them understand what’s happening in the market, make smarter choices, and avoid unnecessary losses. In a fast-moving financial world, giving regular people better information isn’t just helpful—it can make a real difference in their long-term financial security.
#### Research Question
What are you trying to answer?
 I am trying to answer a very simple but important question that is how does stock price movement in particular sectors relate to sales growth, company fundamentals, and macroeconomic factors
#### Data Sources
What data will you use to answer you question?
yahoo finance has been my source of the data
In progress - Integration of the economic data to the analysis and how they impact the price of the stocks.
#### Methodology
What methods are you using to answer the question?
The following steps have been used 
**1. Data Collection & Processing**
Historical Price Data: Yahoo Finance API (yfinance) for 2-year daily stock prices across 303 stocks
Economic Indicators: FRED API (Federal Reserve Economic Data) for macroeconomic time series (M2, Fed Funds Rate, GDP, CPI, Unemployment, Treasury Yields)
Market Volatility: VIX index from Yahoo Finance
Data Cleaning: Forward-fill for missing values, outlier detection, handling of delisted/acquired stocks
**2. Feature Engineering** - Following  indicators have been used including
**Technical**
Momentum indicators (RSI, MACD)
Moving averages (20-day, 50-day, 200-day)
Volatility measures ( standard deviation)
Volume-based metrics
**Economic**
Year-over-year growth rates (M2, CPI, GDP)
Rate of change (Fed Funds, unemployment)
Derived indicators (Yield Curve Slope)
**Fundamental**
Returns calculations (daily, monthly, cumulative)
Risk metrics (annualized volatility, Sharpe Ratio)
Sector aggregations
**3. Exploratory Data Analysis (EDA)**
Visualization: Correlation heatmaps, time series plots, risk-return scatter plots
Descriptive Statistics: Mean, median, standard deviation, skewness by sector
Distribution Analysis: Identifying patterns in returns across sectors and time periods
**4. Machine Learning Models**
Linear Regression: Baseline model for return prediction
Ridge Regression: Regularized linear model to handle multicollinearity (alpha=1.0)
Random Forest Regressor: Ensemble method for capturing non-linear relationships 
Train-Test Split: 80/20 time-series split (respects temporal ordering)
**5. Model Evaluation**
Performance Metrics:
R² Score (coefficient of determination)
RMSE (Root Mean Squared Error)
MAE (Mean Absolute Error)
Cross-Validation: Time-series aware validation to prevent data leakage
Visualization: Actual vs. Predicted plots, residual analysis
**6. Sector-Specific Analysis**
Comparative Analysis: How each sector responds to economic changes
Sensitivity Testing: Correlation of sector returns with specific economic indicators
Scatter Plot Analysis: Risk-return profiles by sector
**7. Data Persistence**
Caching Strategy: Pickle files for large datasets (price_data, economic_data, fundamentals)
Version Control: Structured notebooks (EDA → Advanced → Economic)
Output Artifacts: CSV exports 

#### Results
What did your research find?
The analysis shows that economic factors account some of the variance in stock returns, suggesting that while they play a major role, predictability has a  ceiling, this shows that the  markets remain partly efficient. The time horizon also matters: three-month predictions provide the best balance between accuracy and practical usefulness. In addition to broad economic influences, sector-specific dynamics contribute a part of the variance in returns, highlighting the importance of understanding both macro conditions and industry-level effects when evaluating stock performance.
#### Next steps
What suggestions do you have for next steps?
I am not fully satisfied with the economic factors and how they are impacting fully. In the next couple of weeks I am going to find way to improve on that.
#### Outline of project

- [Basic Data Analysis](https://github.com/sanjayhooda19/CapstoneAIMLEDA/blob/main/StockAnalysis_EDA.ipynb)
- [Advanced Data Analysis](https://github.com/sanjayhooda19/CapstoneAIMLEDA/blob/main/StockAnalysis_Advanced.ipynb)
- [Update Sector stocks](https://github.com/sanjayhooda19/CapstoneAIMLEDA/blob/main/update_sector_stocks.ipynb)
- [Economic Factors](https://github.com/sanjayhooda19/CapstoneAIMLEDA/blob/main/EconomicFactors_Analysis.ipynb)


##### Contact and Further Information
#### Further extension
Economic factor integration is still in progress and will be added to the project in the coming weeks.
