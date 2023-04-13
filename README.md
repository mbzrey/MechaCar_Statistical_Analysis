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

The total summary table was created:

![image](https://user-images.githubusercontent.com/113773420/231855129-267f7b39-995c-4b5a-b477-fd63bcbd4708.png)


The lot summary table was created:

![image](https://user-images.githubusercontent.com/113773420/231854278-1ea05ca1-4b56-4562-aa55-3a65fc20aac1.png)


### Results

Design specification for the MechaCar suspension coils dictate that the standard deviation of the suspension coils must not exceed 10 PSI (variance of 100 PSI squared).

If the analysis is performed on all 3 manufacturing lots, the design specifications are met, as the standard deviation of the total suspension coils' PSI is 7.89 PSI.
However, drilling-down the analysis for each lot, it is shown that Lot 3 has a significant higher stndard deviation than lots 1 and 2. The standard deviarion of lot 3 is 13.05 PSI, value that exceeds the design specification, while the standard deviation of Lots 1 and 2 is 1.00 and 2.73 PSI, respectively.

In conclusion, Lot 3 should be analyzed thoroughly, as it doesn't meet design specifications.



## T-Test on Suspension Coils

Firstly, the t-test was performed on whether the PSI across all manufacturing lots is statistically different from the population mean of 1,500 pounds per square inch.

![image](https://user-images.githubusercontent.com/113773420/231870291-93f6b3ed-5978-4328-a6af-9810f843b5fc.png)


Afterwads, additional t-tests were made to determine if the PSI for each manufacturing lot is statistically different from the population mean of 1,500 pounds per square inch.

### Lot 1

![image](https://user-images.githubusercontent.com/113773420/231871858-c4b8a26c-1e98-4978-8a28-14f032c6f2ff.png)


### Lot 2

![image](https://user-images.githubusercontent.com/113773420/231871968-238a0a6c-170a-4333-8e03-db5017825a33.png)


### Lot 3

![image](https://user-images.githubusercontent.com/113773420/231872149-64d524cf-aa4e-4661-b1fa-2829db04cd48.png)


### Results

The t-test to determine if all manufacturing lots are statistically different from the population mean of 1,500 PSI, provides a p-value of 0.0628, which means that there is not enough evidence to reject the null hypothesis, so the mean PSI of all manufacturing lots is similar tu 1,500 PSI.

In a similar way than the analysis of the standard deviation on suspension coils, the analysis on the mean PSI of manufacturing lot 3 differs widely from manufacturing Lots 1 and 2. The p-value for Lot 1 is 1; for Lot 2 is 0.6072; and, for Lot 3 is 0.04168.

Hence, while it can be stated that he mean PSI of manufacturing Lots 1 and 2 is similar to 1,500, the same cannot be stated for Lot 3.


## Study Design: MechaCar vs Competition

In order to analyze MechaCar against the competition, several steps must be taken.

For starters, it is mandatory to define the competition: which cars should be taken into account? Variables to look for may be, but not limited to:
* price
* drivetrain
* engine
* horsepower
* torque
* fuel/energy used
* mile per gallon economy
* length, width and height
* interior equipment

Metrics are to established and, afterwards, obtained from MechaCar and the competition. Those metrics should be the ones used to define the competition, as they are supposed to be relevant for the market objective. Metrics should also consider what MechaCar manufacturer wants to measure.

Next step, once the data is gathered and arranged, statistical tests should be made to analyze whether the statistics from MechaCar are better than those from the competition. Faster acceleration, faster hot laps, higher horsepower and torque, better mile per gallon economy, etc. In order to do so, an analysis of means should be helpful, as it would allow to infer with statistics foundations if MechaCar is achieving set goals... or not. For example, being faster than the competition.

When comparing MechaCar vs the competition on a one-on-one basis, a t-test should be the best option, but if the comparison is simulteanously against more than 1 competitor, the ANOVA test is the one that should be performed.

As for the data itself, in order for the results to be valid, significance levels must be appropriate so that Level I errors won't be siginficative and the data sample must be large enough so that Level II errors won't bias the results of the test.
