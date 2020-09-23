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

<h5>The R2-squared of 0.63 means our data fits into the model about 63%. </h5>

#### Results from the plotted graph showing a summary of the final prediction
<img src='https://raw.githubusercontent.com/markgicharu/LinearRegressionStatsModels/master/images/final_plot_dpi.jpg'>

#### Summary plot guide<br>
realinv   - Real gross private domestic investment (Bil. of chained
                    2005 US$, seasonally adjusted annual rate)<br>
realgovt  - Real federal consumption expenditures & gross investment
                    (Bil. of chained 2005 US$, seasonally adjusted annual rate)<br>

## Project Summary
-We are trying to predict private domestic investment based on government expenditure and investment.<br>
-We can see the prediction values of private domestic investment **somewhat** matches the curve of the actual government expenditure.<br>
-There are varying **dips** in private domestic investments where there is a **spike** in actual government expenses.<br>
-From the **2002 Dot-Com Bubble and the  2008 financial crash,** there was a great dip in private domestic investment. However, Government Expenditure and Investments rallied on.<br>
-The prediction values **fail** to capture the **varying dips** as they are only considering the government investment and expenditure which had a subtle increase during that period.<br>
-The model is therefore **too Linear** in that it follows closely with its Independent X to predict the dependent Y inorder to get the values for the yhat.<br>
-The linear nature of the model cannot capture the **non-linear** nature of real-world events like the **2002 Dot-Com Bubble** and the **2008 Great Recession.**<br>

## Suggestions
-Try and explore a non-linear model to capture the subtleties of non-linearity.<br>
-We will explore time-series analysis as an alternative.<br>

# THANK YOU
Feel Free to follow me:<br>
[<img src="https://img.shields.io/badge/linkedin-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" />](https://www.linkedin.com/in/mark-gicharu-05908837/)<br>
[<img src="https://img.shields.io/badge/twitter-%231DA1F2.svg?&style=for-the-badge&logo=twitter&logoColor=white" />](https://twitter.com/markgicharu)
