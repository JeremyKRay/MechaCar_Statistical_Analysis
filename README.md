# MechaCar_Statistical_Analysis

## Introduction
The purpose of this project was to analyze a fictitious auto manufacturing company's production problems. There are troubles that are blocking the manufacturing team's progress. R is used to perform the analysis and it is separated into 3 main components. 
  A) A multiple linear regression analysis is performed to identify which variables in the dataset predict the mpg of MechCar prototypes.
  B) Summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots.
  C) T-tests are run to determine if manufacturing lots are statistically different from the mean population. 
  
Finally, a statistical study is designed to compare vehicle performance against vehicles from other manufacturers. A summary interpretation of the findings for each statistical analysis is included.

## Linear Regression to Predict MPG
Using R script, I created a linear regression model with summary statistics to determine what variables affect mpg. The dataset I analyzed is a production dataset for AutosRUs' newest prototype, MechaCar.  
The results are shown below.


![Linear Regression.png](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/d8298876238e1068df1db1b2cb7894e753fb15e9/Linear%20Regression.png)


![Linear Regression and Summary.png](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/33132bae122ac66c3498323fb817d23d4d1f07aa/Linear%20Regression%20and%20Summary.png)

The statistical analysis provided 3 main findings.

1.) According to our results, vehicle length and ground clearance (as well as intercept) are statistically likely to provide non random amounts of variance to the linear regression model. In other words the vehicle length and ground clearance have a significant impact on mpg. Conversely, according to our results, vehicle weight, spoiler angle and AWD are likely to provide random amounts of variance to our model and therefore do not have a significant impact on mpg. There is one possible caveat. When an intercept is statistically significant, it means that the intercept term explains a significant amount of variability in the dependent variable when all independent vairables are equal to zero. Depending on our dataset, a significant intercept could mean that the significant features (such as vehicle length and ground clearance) may need scaling or transforming to help improve the predictive power of the model. Alternatively, it may mean that there are other variables that can help explain the variability of our dependent variable that have not been included in our model. Depending on the dataset and desired performance of the model, we may want to change our independent variables and/or transform them and then re-evaluate your coefficients and significance. 

2.) The slope of the linear model is not considered to be zero. Assuming a significance level of 0.05, a p-value of 5.35e-11 is much much lower than this. This means we can reject the null Hypothesis, which also means that the slope of our linear model is not zero. 

3.) Despite the number of significant variables, this multiple linear regression model does predict mpg of MechaCar prototypes effectively. According to the summary output, the r-squared value of the model is 0.71, meaning there is a strong positive correlation between our variables, and the p-value remained significant, well below the .05 significance level. I still have reservations about having a statistically significant intercept however.

## Summary Statistics on Suspension Coils
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. According to the statistics shown for the Total Summary, the variance across the suspension coils is 62.29 psi, which is below the 100 psi standard, even with a standard deviation of 7.9. This meets the design specification when looking at all lots. However, when examining the lot summary, it becomes apparent that Lot 3 should be further investigated. Its variance of 170.29 is well above the 100 psi standard and the standard deviation for this data set is also much higher than the other two lots. With the other two lot's variances coming in at .98 and 7.47, it is very evident that Lot 3 should be further investigated. Please see the results of the analysis below


![Total Summary.png](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/ae6863526ba95d351d97a69e178e63225fb51bfc/Total%20Summary.png)


![Lot Summary](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/e3b61697c50cabd604162f33a82a58952235eaa0/Lot%20Summary.png)


## T-Tests on Suspension Coils
Please see the results below of the t-tests performed in order to determine if all manufacturing lots and each lot individually are different from the population mean of 1,500 pounds per square inch. A brief explanation of what each t-test is demonstrating is included below the results.

![All Lots](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/e93f55259d0839e706e5e810689baf6e5269f7f5/All%20Lots.png)

The t-test performed on all of the lots shows that as a whole, considering all lots, they are not significantly different than the population mean of 1500 psi for suspension coils. The p-value is .06, above our standard of .05, and the mean is 1498.78.


![Lot 1](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/d2e1bec35dbb3601eddd7f80ccbf2bd687f5135c/Lot%201.png)


The t-test performed on Lot 1 shows that Lot 1 is not significantly different than the population mean of 1500 psi for suspension coils. The p-value is 1 and the mean is exactly 1500.

![Lot 2](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/d2e1bec35dbb3601eddd7f80ccbf2bd687f5135c/Lot%202.png)

The t-test performed on Lot 2 shows that Lot 2 is not significantly different than the population mean of 1500 psi for suspension coils. The p-value is .6072, above our standard of .05, and the mean is 1500.2.


![Lot 3](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/d2e1bec35dbb3601eddd7f80ccbf2bd687f5135c/Lot%203.png)


The t-test performed on Lot 3 shows that Lot 3 is significantly different than the population mean of 1500 psi for suspension coils. The p-value is .04168, below our standard of .05, and the mean is 1496.14.

### Conclusion
The above statistical analysis has revealed a very important statistical variance among the lots for the MechaCar prototype. The pounds per square inch of the suspension coils in cars from Lot 3 are significantly different from the cars of the other 2 lots. So, before moving forward with designing a study comparing MechaCar vs the competition, I would suggest either AutosRUs not include Lot 3 in the study, or fix the issue with the suspension coils to bring the cars closer to the statistical mean.

## Study Design: MechaCar vs Competition
### Description
Now that we have a statistically significant population of MechaCars to study, it is time to see how it might stack up to the competition. I plan to perform the following statistical study to determine if cost, fuel efficiency and safety rating have an effect on the consumer rating. Then, using the same metrics, predict what consumer rating the MechaCar can expect and how that compares to the competition.

#### Metrics

Cost
Fuel efficiency
  - City
  - Highway
Safety Rating
Consumer Rating

#### Null Hypothesis
Cost, Fuel efficiency, and Safety Rating have a statistically significant impact on consumer rating.  

#### Alternative Hypothesis
Cost, Fuel efficiency, and Safety Rating do not have a statistically significant impact on consumer rating.

#### Statistical Test
Multiple Linear Regression to determine the variance of the dependent variable, consumer rating, and the independent variables, cost, fuel efficiency and safety rating

#### Data
Cost, fuel efficiency and Safety rating data for the MechaCar and the competition

Consumer reports data on the competition
