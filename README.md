# MechaCar_Statistical_Analysis
R
## Overview

The goal of the project is to analyze metrics that can affect the manufacturing a new car prototype and compare vehicle performance across different manufacturer lots. These metrics include vehicle length, weight, spoiler angle, ground clearance, AWD capabilities, MPG, and PSI.

## Linear Regression to Predict MPG

<img width="576" alt="Screenshot 2023-02-21 at 10 13 41 PM" src="https://user-images.githubusercontent.com/113556769/220512302-e0febb28-d94d-4959-9859-3d990812e0ab.png">

3 Key Takeaways:

1. Variance of a non-random variable is usually 0. Given this fact, the intercept, vehicle_length, and ground_clearance coeeficients can be said to provide a non-random amount of variance to the mpg values.

2. At a significance level of 0.05, we are able to reject the null hypothesis because of the extremely small p-value. The null hypothesis of a linear regression states that the slope (β1) is equal to 0. However, if we reject the null hypthesis, we're stating that alternative (β1 ≠ 0) is true. Thus, proving that the slope is not 0.

3. Multiple R-squared increases as more variables are passed through the regression. However, adjusted R-squared controls against this increase, and adds penalties for the number of predictors in the model, thus making it a more accurate predictor of how effective the linear model is. An adjusted R-square of 0.6825 concludes that this linear model predicts the mpg of MechaCar prototypes relatively well.

## Summary Statistics on Suspension Coils

<img width="379" alt="Screenshot 2023-02-21 at 10 20 55 PM" src="https://user-images.githubusercontent.com/113556769/220513033-3dfe7e87-5c5f-4aa8-98bd-e640868da5fd.png">
<img width="545" alt="Screenshot 2023-02-21 at 9 26 26 PM" src="https://user-images.githubusercontent.com/113556769/220512724-95d0abbb-f663-4fee-8881-81306f76da62.png">

The overall variance for the entire dataset indicates that the current manufacturing data meets the 100 pounds per square inch variance limitation. However, when separated into three lots, the third lot demonstrates a much higher variance. Because the lots are chosen randomly, there is a possiblity that a third of the lot does not meet the necessary suspension coils requirement.

## T-Test on Suspension Coils

### T-Test on Entire Lot

At a significance level of 0.05, we fail to reject the null hypothesis since the p-value equals 0.06. Therefore, we cannot reject the fact that the sample mean may be equivalent to the true population mean. Another feature to note is the narrow confidence interval. Although a narrower confidence interval implies that there is a smaller chance of obtaining an observation within that interval, it provides greater accuracy than a wider interval.

<img width="448" alt="Screenshot 2023-02-21 at 9 19 25 PM" src="https://user-images.githubusercontent.com/113556769/220513938-b730f8f6-be74-4c15-ae36-fc4faefe0254.png">

### Lot 1

At a significance level of 0.05, we fail to reject the null hypothesis since the p-value equals 1. An interesting correlation between p-value and confidence intervals is that as the p-values get larger, the confidence interval becomes smaller, implying more precision in predicting the true population mean.

<img width="453" alt="Screenshot 2023-02-21 at 9 19 11 PM" src="https://user-images.githubusercontent.com/113556769/220514225-f1214709-7bec-4e9d-bd18-eec411ad706f.png">

### Lot 2 

At a significance level of 0.05, we fail to reject the null hypthesis again since the p-value equals 0.6072. The second lot also has a relatively small confidence interval.

<img width="451" alt="Screenshot 2023-02-21 at 9 18 43 PM" src="https://user-images.githubusercontent.com/113556769/220514311-3d1d4099-3826-47af-9f31-cd00e23269bc.png">

### Lot 3

At a significance level of 0.05, we can reject the null hypothesis since the p-value equals 0.04168. The mean of this sample is also significantly smaller in comparison to the previous two lots. More importantly, unlike the previous two lots, the confidence interval for the third lot does not include the predicted population mean.

<img width="490" alt="Screenshot 2023-02-21 at 9 17 42 PM" src="https://user-images.githubusercontent.com/113556769/220514358-52fe8645-080b-4db5-acf4-78f15dfcae60.png">

## Study Design: MechaCar vs. Competition

Another statistical study that can be performed to determine MechaCar's standing against its competition is a linear regression on city and highway fuel efficiency. Gasoline is expensive nowadays, and it is an important feature that many consumers look at when purchasing a new car. The metrics that can be included in this analysis are:

1. City and highway fuel efficiency: dependent variable
2. Horse power: independent variable
3. Vehicle weight: independent variable
4. AWD capabilities: independent variable
5. MPG: independent variable In addition to the MPG, AWD, and vehicle weight data that we already have, we would have to collect fuel efficiency and horse power data for the sample data set at hand.
