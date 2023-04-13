# MechaCar Statistical Analysis

## Linear Regression to Predict MPG

The MechaCar_mpg.csv file was loaded on RStudio correctly:

![image](https://user-images.githubusercontent.com/113773420/231843552-da60eed5-9103-49cc-89a5-59ba871c2bf5.png)


A multiple linear regression model was applied on the variables, selecting the "miles per gallon economy" ("mpg" column) as the dependent variable and all the others as the independent ones:

![image](https://user-images.githubusercontent.com/113773420/231844473-02e2d780-979b-49e8-bcce-1f2085eebc77.png)


Finally, a statistics summary was performed:

![image](https://user-images.githubusercontent.com/113773420/231844843-d56e2c75-62a4-4146-b05c-31232f052efe.png)


### Results

The R-squared value of the linear regression model is 0.7149, which may be considered -barely- a correct model (roughly, 71.5% of the predictions will be correct when using this linear model). The acceptance range for the R-value must be defined depending on the accuracy required by each analysis/project.  

Moreover, the slope of the linear model, there is sufficient evidence to state that it is not zero, due to the fact that the p-value of the multiple linear regression analysis is 5.35e-11 (a value very close to zero, lower than the commonly used significance level of 0.05).

As for the independent variables of the model, the probability that each coefficient contributes a random amount of variance shows that vehicle length and ground clearance (as well as intercept) are statistically unlikely to provide random amounts of variance to the linear model. In other words, the vehicle length and ground clearance have a significant impact on miles per gallon economy.


## Summary Statistics on Suspension Coils

The Suspension_Coil.csv file was loaded on RStudio correctly:

![image](https://user-images.githubusercontent.com/113773420/231850044-d6adf4b9-4919-4a04-8f4e-600664feec50.png)



### Results
Write a short summary using screenshots from your total_summary and lot_summary dataframes, and address the following question:
* The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?



## T-Tets on Suspension Coils

Briefly summarize your interpretation and findings for the t-test results. Include screenshots of the t-test to support your summary.


## Study Design: MechaCar vs Competition

Write a short description of a statistical study that can quantify how the MechaCar performs against the competition. In your study design, think critically about what metrics would be of interest to a consumer: for a few examples, cost, city or highway fuel efficiency, horse power, maintenance cost, or safety rating.
In your description, address the following questions:
* What metric or metrics are you going to test?
* What is the null hypothesis or alternative hypothesis?
* What statistical test would you use to test the hypothesis? And why?
* What data is needed to run the statistical test?
