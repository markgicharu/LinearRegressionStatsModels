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
       
  X = realgovt <br>
  y = realinv <br>
  
#### What is the Correlation between this two variables?
<img src='https://raw.githubusercontent.com/markgicharu/LinearRegressionStatsModels/master/images/heatmap.jpg'>

<h5>From the high correlation of 0.79 we decide to perform a linear regression</h5>

### Results from the stats model OLS Regression as a summary table
<img src='https://raw.githubusercontent.com/markgicharu/LinearRegressionStatsModels/master/images/OLS_Results.jpg'>


#### Results from the plotted graph showing a summary of the final prediction
<img src='https://raw.githubusercontent.com/markgicharu/LinearRegressionStatsModels/master/images/final_plot_dpi.jpg'>


