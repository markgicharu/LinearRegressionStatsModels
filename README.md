# LinearRegressionStatsModels
##### Use Linear Regression to predict gross private domestic investment from an independent variable X of federal consumption expenditures & gross investment.

Data Description Below

Number of Observations - 203
### Macro Data

    Number of Variables - 14

    Variable name definitions::

        year      - 1959q1 - 2009q3
        quarter   - 1-4
        realgdp   - Real gross domestic product (Bil. of chained 2005 US$,
                    seasonally adjusted annual rate)
        realcons  - Real personal consumption expenditures (Bil. of chained
                    2005 US$, seasonally adjusted annual rate)
        realinv   - Real gross private domestic investment (Bil. of chained
                    2005 US$, seasonally adjusted annual rate)
        realgovt  - Real federal consumption expenditures & gross investment
                    (Bil. of chained 2005 US$, seasonally adjusted annual rate)
        realdpi   - Real private disposable income (Bil. of chained 2005
                    US$, seasonally adjusted annual rate)
        cpi       - End of the quarter consumer price index for all urban
                    consumers: all items (1982-84 = 100, seasonally adjusted).
        m1        - End of the quarter M1 nominal money stock (Seasonally
                    adjusted)
        tbilrate  - Quarterly monthly average of the monthly 3-month
                    treasury bill: secondary market rate
        unemp     - Seasonally adjusted unemployment rate (%)
        pop       - End of the quarter total population: all ages incl. armed
                    forces over seas
        infl      - Inflation rate (ln(cpi_{t}/cpi_{t-1}) * 400)
        realint   - Real interest rate (tbilrate - infl)
       
  X = realgovt
  y = realinv
  
#### What is the Correlation between this two variables?
<img src='https://raw.githubusercontent.com/markgicharu/LinearRegressionStatsModels/master/images/heatmap.jpg'>

From the high correlation of 0.79 we decide to perform a linear regression

 Results from the stats model OLS Regression as a summary table
 OLS Regression Results                            
==============================================================================

Dep. Variable:                realinv
R-squared:                       0.632
Model:                            OLS  
Adj. R-squared:                  0.630
Method:                 Least Squares
F-statistic:                     344.8
Date:                Wed, 23 Sep 2020
Prob (F-statistic):           1.78e-45
Time:                        12:48:40  
Log-Likelihood:                -1479.6
No. Observations:                 203  
AIC:                             2963
Df Residuals:                     201   
BIC:                             2970
Df Model:                           1 
Covariance Type:            nonrobust

==============================================================================
                 coef    std err          t      P>|t|      [0.025      0.975]
------------------------------------------------------------------------------
const      -1177.0037    120.558     -9.763      0.000   -1414.724    -939.284
realgovt       3.3013      0.178     18.568      0.000       2.951       3.652

==============================================================================
Omnibus:                        8.118   Durbin-Watson:                   0.032
Prob(Omnibus):                  0.017   Jarque-Bera (JB):                6.521
Skew:                           0.342   Prob(JB):                       0.0384
Kurtosis:                       2.449   Cond. No.                     3.27e+03

==============================================================================

Notes:
[1] Standard Errors assume that the covariance matrix of the errors is correctly specified.<br>
[2] The condition number is large, 3.27e+03. This might indicate that there are strong multicollinearity or other numerical problems.<br>


