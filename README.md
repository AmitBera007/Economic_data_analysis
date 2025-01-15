# Economic Data Analysis on US Financial Data  

This project explores the relationships between key economic indicators such as interest rates, inflation, GDP, unemployment rates, industrial production, and the S&P 500 index. By employing advanced statistical methods and regression modeling, the analysis provides valuable insights into the dynamics of the U.S. economy and financial markets.  

## Key Features  

- **Exploratory Data Analysis:** Comprehensive analysis of economic indicators, including trends, descriptive statistics, and correlation matrices.  
- **Multiple Linear Regression:** Regression modeling to uncover dependencies between the S&P 500 index and economic indicators.  
- **Statistical Testing:** Includes heteroskedasticity testing, normality checks, and structural break analysis to ensure robust results.  
- **Actionable Insights:** Policy recommendations and investment implications based on findings.  

## Dataset Overview  

The analysis is based on time-series data of U.S. economic indicators, summarized below:  

| **Variable**         | **Description**                           |  
|-----------------------|-------------------------------------------|  
| `date`               | Date in YYYY-MM-DD format                |  
| `Interest Rate`      | Interest rate in percentage              |  
| `Inflation`          | Inflation rate in percentage             |  
| `GDP`                | Gross Domestic Product in millions       |  
| `Unemployment`       | Unemployment rate in percentage          |  
| `Ind Prod`           | Industrial production index              |  
| `sp500`              | S&P 500 index values                    |  

## Methodology  

1. **Exploratory Data Analysis (EDA):**  
   - Descriptive statistics for key variables.  
   - Correlation matrix to identify relationships between indicators.  
   - Time-series trend analysis for all indicators.  

2. **Multiple Linear Regression:**  
   - Dependent Variable: `sp500` (S&P 500 index).  
   - Independent Variables: Interest Rate, Inflation, GDP, Unemployment, and Industrial Production.  
   - Model explains 94.1% of the variance in `sp500` (R-squared = 0.941).  

3. **Statistical Testing:**  
   - **Heteroskedasticity Test:** Goldfeld-Quandt test indicates non-constant variance in residuals.  
   - **Normality Test:** Jarque-Bera test shows residuals are not normally distributed.  
   - **Structural Break Test:** Chow test confirms structural breaks in the data.  

## Results  

- **Key Findings:**  
   - Positive relationships: Interest Rate ↔ `sp500`, GDP ↔ `sp500`.  
   - Negative relationships: Inflation ↔ `sp500`, Unemployment ↔ `sp500`, Industrial Production ↔ `sp500`.  
   - Structural breaks highlight changing relationships over time.  

- **Regression Equation:**
 
$$
   sp500 = 56.88 + 39.30 \cdot (\text{Interest Rate}) - 5.30 \cdot (\text{Inflation}) + 0.55 \cdot (\text{GDP}) - 111.34 \cdot (\text{Unemployment}) - 62.94 \cdot (\text{Industrial Production})
$$

## Recommendations  

- Address heteroskedasticity and non-normality with robust standard errors or data transformations.  
- Investigate structural breaks using dynamic or piecewise regression models.  
- Utilize findings to inform policy decisions and investment strategies.  
