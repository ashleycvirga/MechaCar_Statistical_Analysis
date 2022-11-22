# MechaCar_Statistical_Analysis
Using R in R Studio to perform statistical analysis on MechaCar data

AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ sought to review the production data for insights that may help the manufacturing team.

This project performs multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes, collects summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots, runs t-tests to determine if the manufacturing lots are statistically different from the mean population, and designs a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. 

## Linear Regression to Predict MPG

The MechaCar_mpg.csv dataset contains mpg test results for 50 prototype MechaCars. The MechaCar prototypes were produced using multiple design specifications to identify ideal vehicle performance. Multiple metrics, such as vehicle length, vehicle weight, spoiler angle, drivetrain, and ground clearance, were collected for each vehicle. 

This multiple linear regression model predicts the mpg of MechaCar prototypes using using all of the specification variables provided. 

The null hypothesis states that the slope of the linear model is zero and thus any effects of the given variables on mpg can be explained by random chance. 

The alternative hypothesis states that the slope of the linear model is not zero and thus the effects of one or more of the given variables on mpg cannot be explained by random chance. 

The significance level used is a p-value of 0.05.

![lm_function](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/848f4f2114136c29ff32b9ecb6316048ac273984/Resources/lm_function.png)

![summary_lm_function](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/848f4f2114136c29ff32b9ecb6316048ac273984/Resources/summary_lm_function.png)

### Based on this ouput, the variables "vehicle_length" and "ground_clearance" provided a non-random amount of varience to the mpg values in the dataset.

vehicle_length: Pr(>|t|) = 2.60e-12 is statistically significant even at the highest level of scrutiny

ground_clearance: Pr(>|t|) = 5.21e-08 is also statistically significant even at the highest level of scrutiny 

The variables for vehicle_weight: Pr(>|t|) = 0.0776

spoiler_angle: Pr(>|t|) = 0.3069
                  
and AWD: Pr(>|t|) = 0.1852
              
are not less than the statistical significance level of the p-value 0.05

### The slope of this linear model is not considered to be zero

With a p-value: 5.35e-11 we can reject the null hypothesis at the 95% confidence level.

In other words, we can state thwith 95% confidence that the intercept term of -1.040e+02 determined by the model explains a significant amount of variability in the dependent variable (mpg) when all independent vairables(specifications) are equal to zero.

### Considering the field of research we are dealing with here--vehicle manufacturing--this linear model ability to predict mpg of MechaCar prototypes is not quite as effective as we would like it to be.

The Multiple R-squared value of 0.7149 tells us that about 71% of the variability in mpg can be explained by the model. 

When manufacturing vehicles we would hope for a stronger accuracy level for the MechaCar's mpg than less than 3 in every 4 cars produced meeting the manufacturers fuel efficiency target.


## Summary Statistics on Suspension Coils

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. In this dataset, the weight capacities of multiple suspension coils were tested to determine if the manufacturing process is consistent across production lots. 

Below are the summary statistics of the suspension coils:

![total_summary](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/ebe95a927cbb93fa0f2e82f29ae8c90efa7e66e9/Resources/total_summary.png)

![lot_summary](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/ebe95a927cbb93fa0f2e82f29ae8c90efa7e66e9/Resources/lot_summary.png)

The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch.

The overall total_summary statistics show that the manufactured coils have a variance of 62.29356 which is within the design specifications.

However, when we look at the lot summary, it's clear that Lot3 has a varience of 170.2861224 which does not meet the design specifications.


## T-Tests on Suspension Coils

The following t-tests on the suspension coil data were performed in order to determine if a sample mean is statistically different from the population mean of 1500 PSI. The first t-test analyzes the difference in the mean PSI for all 150 suspension coils in the data set. The second through the fourth t-tests analyze the difference in mean PSI for each of the three individual manufacturing lots: Lot1, Lot2 & Lot3. The p-value used to determine statistical significance here is 0.05.

![total_t_test](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/41568c425df94503ed62c0b620f9295ffba2c940/Resources/total_t_test.png)


![lot_1_t_test](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/41568c425df94503ed62c0b620f9295ffba2c940/Resources/lot_1_t_test.png)


![lot_2_t_test](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/41568c425df94503ed62c0b620f9295ffba2c940/Resources/lot_2_t_test.png)


![lot_3_t_test](https://github.com/ashleycvirga/MechaCar_Statistical_Analysis/blob/41568c425df94503ed62c0b620f9295ffba2c940/Resources/lot_3_t_test.png)

Based on these results, the mean of all 150 sampled suspension coils and the population mean of all suspension coils manufactured shows no statistical difference.

Additionally, Lot 1 and Lot 2 sample means show no statistical difference from the population mean.

Lot 3, however, IS statistically different from the population mean. The p-value from the t-test on Lot 3 is  0.04168 which is less than the p-value = 0.05 statistical significance level for this test. Lot 3 is statistically significantly different than the population of manufactured suspension coils.


## Study Design: MechaCar vs Competition




