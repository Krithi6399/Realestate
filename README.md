# Realestate
Analysis of Real estate data set 
Firstly after generating a linear model and analyzing the summary considering price per unit versus the 3 independent variables, nearest-station, house-age and convenience stores individually, it is clearly evident that the houses with the nearest train stations are priced higher than the once farther away from the station.
House age and convenience stores don’t have a huge impact on predicting the price of the units(houses) as compared to the nearest station. 
The linear model has a negative slope which indicates that the price of houses(y – axis) decreases as the distance to the nearest station increases( x- axis) The multiple R squared value is the highest(0.6538) for the linear model2 plotted against  price per unit and the nearest stations. 
Thus approximately 65% of the variations in the price per unit(house) can be explained by the independent variable -nearest station. 

# Model 1 summary

Model1 <- lm(price.per.unit ~ house.age,real)
> summary(model1)

Call:
lm(formula = price.per.unit ~ house.age, data = real)

Residuals:
    Min      1Q  Median      3Q     Max 
-31.113 -10.738   1.626   8.199  77.781 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)    
(Intercept) 42.43470    1.21098  35.042  < 2e-16 ***
house.age   -0.25149    0.05752  -4.372 1.56e-05 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 13.32 on 412 degrees of freedom
Multiple R-squared:  0.04434,	Adjusted R-squared:  0.04202 
F-statistic: 19.11 on 1 and 412 DF,  p-value: 1.56e-05

# Model 2 summary

> model1 <- lm(price.per.unit ~ nearest.station,real)
> summary(model1)

Call:
lm(formula = price.per.unit ~ nearest.station, data = real)

Residuals:
    Min      1Q  Median      3Q     Max 
-35.396  -6.007  -1.195   4.831  73.483 

Coefficients:
                  Estimate Std. Error t value Pr(>|t|)    
(Intercept)     45.8514271  0.6526105   70.26   <2e-16 ***
nearest.station -0.0072621  0.0003925  -18.50   <2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 10.07 on 412 degrees of freedom
Multiple R-squared:  0.6538,	Adjusted R-squared:  0.4524 
F-statistic: 342.2 on 1 and 412 DF,  p-value: < 2.2e-16

# Model 3 summary

model1 <- lm(price.per.unit ~ convenience.stores,real)
> summary(model1)

Call:
lm(formula = price.per.unit ~ convenience.stores, data = real)

Residuals:
    Min      1Q  Median      3Q     Max 
-35.407  -7.341  -1.788   5.984  87.681 

Coefficients:
                   Estimate Std. Error t value Pr(>|t|)    
(Intercept)         27.1811     0.9419   28.86   <2e-16 ***
convenience.stores   2.6377     0.1868   14.12   <2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 11.18 on 412 degrees of freedom
Multiple R-squared:  0.326,	Adjusted R-squared:  0.3244 
F-statistic: 199.3 on 1 and 412 DF,  p-value: < 2.2e-16





# Conclusion

Based on the visualization and the R summary, the real estate firm can consider nearest train stations as one of the predicting variables for price of the houses in that locality.  This prediction will help the firm to better gauge the fluctuations in the price of houses. This will benefit easy commute for people living near to the train station and thus reduces the hazel of huge traffic jams, save money on transport costs (gas, toll, parking, vehicle wear and tear etc.). Houses situated near the grater suburb will benefit superior growth value than the ones located in isolated areas as the government will invest more to develop these areas. Moreover, train stations are surrounded by public bus stops, motels, restaurants and overall, well developed infrastructure. 

