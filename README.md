# MechaCar_Statistical_Analysis
## Linear Regression to Predict MPG
Using R script, I created a linear regression model with summary statistics to determine what variables affect mpg analyzing a production dataset for AutosRUs' newest prototype, MechaCar.  
The results are shown below.


![Linear Regression.png](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/d8298876238e1068df1db1b2cb7894e753fb15e9/Linear%20Regression.png)


![Linear Regression and Summary.png](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/33132bae122ac66c3498323fb817d23d4d1f07aa/Linear%20Regression%20and%20Summary.png)

The statistical analysis provided 3 main findings.

1.) According to our results, vehicle length and ground clearance (as well as intercept) are statistically likely to provide non random amounts of variance to the linear regression model. In other words the vehicle length and ground clearance have a significant impact on mpg. Conversely, according to our results, vehicle weight, spoiler angle and AWD are likely to provide random amounts of variance to our model and therefore do not have a significant impact on mpg. There is one possible caveat. When an intercept is statistically significant, it means that the intercept term explains a significant amount of variability in the dependent variable when all independent vairables are equal to zero. Depending on our dataset, a significant intercept could mean that the significant features (such as vehicle length and ground clearance) may need scaling or transforming to help improve the predictive power of the model. Alternatively, it may mean that there are other variables that can help explain the variability of our dependent variable that have not been included in our model. Depending on the dataset and desired performance of the model, you may want to change your independent variables and/or transform them and then re-evaluate your coefficients and significance. 

2.) The slope of the linear model is not considered to be zero. Assuming a significance level of 0.05, a p-value of 5.35e-11 is much much lower than this. This means we can reject the null Hypothesis, which also means that the slope of our linear model is not zero. 

3.) Despite the number of significant variables, this multiple linear regression model does predict mpg of MechaCar prototypes effectively. According to the summary output, the r-squared value of the model is 0.71, meaning there is a strong positive correlation between our variables, and the p-value remained significant, well below the .05 significance level. I still have reservations about having aa statistically significant intercept however.

## Summary Statistics on Suspension Coils
The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. According to the statistics shown for the Total Summary, the variance across the suspension coils is 62.29 psi, which is below the 100 psi standard, even with a standard deviation of 7.9. This meets the design specification when looking at all lots. However, when examining the lot summary, it becomes apparent that Lot 3 should be further investigated. Its variance of 170.29 is well above the 100 psi standard and the standard deviation for this data set is also much higher than the other two lots. With the other two lot's variances coming in at .98 and 7.47, it is very evident that Lot 3 should be further investigated. Please see the results of the analysis below


![Total Summary.png](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/ae6863526ba95d351d97a69e178e63225fb51bfc/Total%20Summary.png)


![Lot Summary](https://github.com/JeremyKRay/MechaCar_Statistical_Analysis/blob/e3b61697c50cabd604162f33a82a58952235eaa0/Lot%20Summary.png)


##T-Tests on Suspension Coils
Please see the results below of the t-tests performed in order to determine if all manufacturing lots and each lot individually are different from the population mean of 1,500 pounds per square inch. A brief explanation of what each t-test is demonstrating is included below the results.
