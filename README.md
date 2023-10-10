## Dataset and Algorithm
This project is based on a **multivariate regression model** that can predict housing prices using the following independent variables: *lotsize*, *bedrooms*, *bathrooms*, *number of stories*, *number of garage places*, *recreation room*, *full basement*, and *air-conditioning*. 

**Dependent Variable**: Price *in US dollars*

The dataset has 546 records and all the variables are continuous.

Additionally, recommendations will be made for the necessary next steps to take.

## Written form of the Regression Model
**Model equation**

![image](https://user-images.githubusercontent.com/121362860/225081971-df3ac138-5283-4256-a42f-9932be0d9f54.png)

![image](https://user-images.githubusercontent.com/121362860/225081818-6432af18-9a15-4014-94a2-b07b51e33fda.png)

![image](https://user-images.githubusercontent.com/121362860/225081577-8403db82-7661-48af-b2cc-604656979389.png)

The intercept = 68860.08

### The Effects of the Coefficients
All the independent variables have a positive effect/weight on the output variable, price. Consequently, for every unit increase in these variables, there is a corresponding increase in price. Iotsize, however, has the highest weight and effect on the output variable. For every unit increase in the lot size, there is a corresponding 8634.48 dollar increase in price. On the other hand, bedrooms, has the least effect on the output variable. 

## Model Outputs and Metrics Explanation
* **Mean**: 68121.6
* **Adjusted R2**: 53%. This implies that the model can only explain about 53% of the variability in the output variable (price) and does not have a good fit. The R2 is not considered since this is a multivariate model.
+ **MAE**: 12127.85. This value is greater than 10% of the mean.
- **RMSE**: 15921.56. The root mean square error of the model is also greater than 10% of the mean.
Since both the MAE and the RMSE are not within the 10% range, it implies that there is a large variance and an indication of the potential for outliers and skewness.

## Recommendations
* **Improve normality using regularization or Yeo-Johnson transformation**
Further analysis using a histogram showed that the continuous independent variables in the dataset were found to have a skewed distribution, which can negatively impact the performance of a linear regression model. To address this issue, one of the transformation techniques can be implemented to normalize the distribution depending on skewness.
+ **Correlation Feature Selection**
This technique can be used to choose the most important variables that will improve the model. This will be useful in selecting the features that have a high enough correlation with the output variable. With the newly selected features, a new model can be created which may turn out to be an optimized one in comparison to the base model.






















