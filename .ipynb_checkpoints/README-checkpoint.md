## ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2

<h1 align="center">Increasing Home Values in Ames, Iowa</h1>

## Purpose

### Problem Statement

As of March 2022, the median home value in Ames, Iowa is 286,826 dollars. The median home value has not seen much consistency with year over year percent changes  in the past 5 years due to the housing crash in 2018-2019 and post COVID-19 economic effects in 2021-2022.

The city of Ames is interested in identifying ways in which they and their residents can do their part to help increase the city’s median home value in spite of the continuing post COVID-19 economic effects.

This analysis aims to identify specific housing features that have a high impact on a home’s value using a machine learning regression model. With this information, the city will know what to consider when building new housing and residents will know what to consider when building, updating or selling their home. 

### Background

According to historical rates of home appreciation, the universal 'normal' rate of appreciation for the housing market is between 3-5%.  According to Zillow, the Ames, IA median home values for the past 5 years are as follows:

|**Month/Year**|**Median Home Value**|**Percent Change**|
|---|---|---|
|**March 2018**|234k|+4.0%|
|**March 2019**|234k|+0.0%|
|**March 2020**|239k|+2.1%|
|**March 2021**|249k|+4.2%|
|**March 2022**|289k|+15.1%|

The city has mostly fallen within the 2-4% range with the exceptions of 2019, due to the housing crash that began in the summer of 2018, and 2022, due to the post COVID-19 economic effects.

Their 15.1% increase falls in line with the nationwide 15.8% increase. Existing home sales hit a 15-year high in 2021 because of the incredibly low interest rates and a low inventory of homes. The Federal Reserve Board is signaling there may be as many as four rate hikes, which is suspected to cause a shift in the housing market.

---

## Data

### Dataset

The Ames, IA housing data set was obtained from the Ames Assessor’s Office. It contains 2051 observations, spanning from 2006-2011, and 81 features.

### Data Dictionary

|**Feature**|**Data Type**|**Description**|
|---|---|---|
|**Id**|*int*|Identification number.|
|**PID**|*int*|Parcel identification number - can be used with city web site for parcel review.|
|**MS SubClass**|*int*|Identifies the type of dwelling involved in the sale.|
|**MS Zoning**|*object*|Identifies the general zoning classification of the sale.|
|**Lot Frontage**|*float*|Linear feet of street connected to property.|
|**Lot Area**|*float*|Lot size in square feet.|
|**Street**|*object*|Type of road access to property.|
|**Alley**|*object*|Type of alley access to property.|
|**Lot Shape**|*object*|General shape of property.|
|**Land Contour**|*object*|Flatness of the property.| 
|**Utilities**|*object*|Type of utilities available.|
|**Lot Config**|*object*|Lot configuration.|
|**Land Slope**|*object*|Slope of property.|
|**Neighborhood**|*object*|Physical locations within Ames city limits.|
|**Condition 1**|*object*|Proximity to various conditions.|
|**Condition 2**|*object*|Proximity to various conditions (if more than one is present).|
|**Bldg Type**|*object*|Type of dwelling.|
|**House Style**|*object*|Style of dwelling.|
|**Overall Qual**|*int*|Rates the overall material and finish of the house.|
|**Overall Cond**|*int*|Rates the overall condition of the house.|
|**Year Built**|*int*|Original construction date.|
|**Year Remod/Add**|*int*|Remodel date (same as construction date if no remodeling or additions).|
|**Roof Style**|*object*|Type of roof.|
|**Roof Matl**|*object*|Roof material.|
|**Exterior 1**|*object*|Exterior covering on house.|
|**Exterior 2**|*object*|Exterior covering on house (if more than one material).|
|**Mas Vnr Type**|*object*|Masonry veneer type.|
|**Mas Vnr Area**|*float*|Masonry veneer area.|
|**Exter Qual**|*object*|Evaluates the quality of the material on the exterior.|
|**Exter Cond**|*object*|Evaluates the present condition of the material on the exterior.|
|**Foundation**|*object*|Type of foundation.|
|**Bsmt Qual**|*object*|Evaluates the height of the basement.|
|**Bsmt Cond**|*object*|Evaluates the general condition of the basement.|
|**Bsmt Exposure**|*object*|Refers to walkout or garden level walls.|
|**BsmtFin Type 1**|*object*|Rating of basement finished area.|
|**BsmtFin SF 1**|*float*|Type 1 finished square feet.|
|**BsmtFinType 2**|*object*|Rating of basement finished area (if multiple types).|
|**BsmtFin SF 2**|*float*|Type 2 finished square feet.|
|**Bsmt Unf SF**|*float*|Unfinished square feet of basement area.|
|**Total Bsmt SF**|*float*|Total square feet of basement area.|
|**Heating**|*object*|Type of heating.|
|**HeatingQC**|*object*|Heating quality and condition.|
|**Central Air**|*object*|Central air conditioning.|
|**Electrical**|*object*|Electrical system.|
|**1st Flr SF**|*int*|First floor square feet.|
|**2nd Flr SF**|*int*|Second floor square feet.|
|**Low Qual Fin SF**|*int*|Low quality finished square feet (all floors).|
|**Gr Liv Area**|*int*|Above grade (ground) living area square feet.|
|**Bsmt Full Bath**|*float*|Basement full bathrooms.|
|**Bsmt Half Bath**|*float*|Basement half bathrooms.|
|**Full Bath**|*int*|Full bathrooms above grade.|
|**Half Bath**|*int*|Half baths above grade.|
|**Bedroom**|*int*|Bedrooms above grade (does NOT include basement bedrooms).|
|**Kitchen**|*int*|Kitchens above grade.|
|**KitchenQual**|*object*|Kitchen quality.|
|**TotRmsAbvGrd**|*int*|Total rooms above grade (does not include bathrooms).|
|**Functional**|*object*|Home functionality (Assume typical unless deductions are warranted).|
|**Fireplaces**|*int*|Number of fireplaces.|
|**FireplaceQu**|*object*|Fireplace quality.|
|**Garage Type**|*object*|Garage location.|
|**Garage Yr Blt**|*float*|Year garage was built.|
|**Garage Finish**|*object*|Interior finish of the garage.|
|**Garage Cars**|*float*|Size of garage in car capacity.|
|**Garage Area**|*float*|Size of garage in square feet.|
|**Garage Qual**|*object*|Garage quality.|
|**Garage Cond**|*object*|Garage condition.|
|**Paved Drive**|*object*|Paved driveway.|
|**Wood Deck SF**|*int*|Wood deck area in square feet.|
|**Open Porch SF**|*int*|Open porch area in square feet.|
|**Enclosed Porch**|*int*|Enclosed porch area in square feet.|
|**3-Ssn Porch**|*int*|Three season porch area in square feet.|
|**Screen Porch**|*int*|Screen porch area in square feet.|
|**Pool Area**|*int*|Pool area in square feet.|
|**Pool QC**|*object*|Pool quality.|
|**Fence**|*object*|Fence quality.|
|**Misc Feature**|*object*|Miscellaneous feature not covered in other categories.|
|**Misc Val**|*int*|Value of miscellaneous feature.|
|**Mo Sold**|*int*|Month Sold (MM).|
|**Yr Sold**|*int*|Year Sold (YYYY).|
|**Sale Type**|*object*|Type of sale.|
|**SalePrice**|*object*|Sale price.|

---

## Exploratory Data Analysis

### Distribution of Sale Prices

The distribution of the sale prices is left-skewed and ranges from 0 to 600k. The peak of the distribution seems to be in the 140k-200k range, with about 800 sales, followed by the 75k-130k range with just over 500 sales.

### Sale Price vs. Numerical Features Heatmap

The top highly correlated features are: 
* Overall Quality (0.8)
* Above Ground Living Area (0.7)
* Garage Area (0.65) 
* Garage Cars (0.65)
* Total Basement Square Footage (0.63)
* First Floor Square Footage (0.62)

These features can be considered strong predictors of the sale price.

### Numerical Feature Distributions

To supplement the heatmap, plotting the distribution of each of the numerical columns provides a different perspective on which features will be useful. The more distribution present, the better chance the feature has of being a strong predictor. 

As in the heatmap, overall quality, above ground living area, garage area, garage cars, total basement square footage, and first floor square footage have good distributions. The year built and year remodeled/of additions fell lower on the correlation scale but also have good distributions and would make for good predictors.

### Categorical Feature Barcharts

Similar to the distribution of the numerical features, the categorical feature barcharts provide a look into which features will be useful. The more variability, the better chance the feature has of being a strong predictor. 

Based on this, it seems that neighborhood, building type, house style, external qualities, basement details and garage details would make for good predictors.

---

## Model Exploration

### Pre-Processing

The numerical features were scaled and the categorical features were one hot encoded, causing the number of total features to increase to 301.

### Modeling

With a regression model in mind, I explored 4 model types:

* Linear Regression
* Ridge Regression
* Lasso Regression
* ElasticNet Regression

The R2 score and RMSE metrics were used to evaluate the performance of the models.

* An R2 score explains how much variability a model is able to explain. On a scale of 0 to 1, the higher the score, the better. And when comparing the train and validation R2 scores, if the validation R2 score is higher than the train R2 score, then the model is likely to do well when applied to unseen data. On the other hand, if the train R2 score is higher than the validation R2 score, then the model is in danger of being overfit, and will likely not do well when applied to unseen data.

* The RMSE describes how far off the predicted values are from the actual values, and when compared to the standard deviation, can indicate if the predicted value is within an acceptable range. Ideally, the RMSE should be less than the standard deviation.

#### Linear Regression

The simple linear regression model did not perform well. The train R2 score was 0.94, while the validation R2 score was in the negatives. The model was incredibly overfit, meaning that the model was trained too closely to the training data, and therefore, does not do well with unseen data. The train RMSE (18,879) was less than the train standard deviation (79,793), but the validation RMSE (3,480,982,442,410,043) way beyond the validation standard deviation (77,175).

#### Ridge Regression

The RidgeCV model applies ridge (L2) regularization to a linear regression model. This means that features with large coefficients will be shrunk toward zero, thereby reducing model complexity to help prevent overfitting. The alpha parameter dictates the strength of the regularization, making it very important to get the alpha just right. Fortunately, given a range, the RidgeCV model itself can cross validate various alphas and fit the data according to the best-performing alpha.

The best-performing alpha was 10.24, and it allowed for a much better performing model, compared to the simple linear regression.

* The train R2 score was 0.9127, and the validation R2 score was 0.9148. Having both scores in the 0.90s indicated that the model performed well, and a validation R2 score that was higher than the train R2 score meant that the model did very well with unseen data.

* The train RMSE (23,571) was less than the train standard deviation (79,793), and the validation RMSE (22,499) was less than the validation standard deviation (77,175).

Since the RidgeCV model did so well, I wanted to see if I could find a better performing alpha by focusing the range a bit more.

The best-performing alpha was then 9.77, and the model performed very similarly to the first RidgeCV model.

* The train R2 score increased slightly (0.9127 -> 0.9131), while the validation R2 score decreased slightly (0.9148 -> 0.91478).

* The train RMSE decreased (23,571 -> 23,417), while the validation RMSE increased (22,499 -> 22,509).

Though the train metrics improved, the opposite happened for the validation metrics. For this reason, the RidgeCV model with an alpha of 10.24 remained the best performer.

#### Lasso Regression

The LassoCV model applies a lasso (L1) regularization to a linear regression model. This means that non-important feature coefficients will be zeroed out, and will be eliminated as features, allowing the model to focus on features of importance. This reduces model complexity and helps prevent overfitting. Again, the alpha parameter dictates the strength of the regularization, making it very important to get the alpha just right. Fortunately, given a range, the LassoCV model itself can cross validate various alphas and fit the data according to the best-performing alpha.

The best-performing alpha was 83.02. Of the 301 features, 173 were zeroed out, and 128 were kept. This allowed for a better performing model, compared to all previous models.

* The train R2 score was 0.9268, and the validation R2 score was 0.9258.

* The train RMSE (21,582) was less than the train standard deviation (79,793), and the validation RMSE (20,996) was less than the validation standard deviation (77,175).

Though the validation R2 score here was not higher than the train R2 score, it wasn't off by very much, and both were in the 0.92s, which was higher than any of the previous R2 scores. The train and validation RMSEs were also decreased by about 2,000 and reached an all time low. This made the LassoCV with an alpha of 83.02 the best-performer.

Since the LassoCV model did so well, I wanted to see if I could find a better performing alpha by focusing the range a bit more.

The best-performing alpha was then 79.25. As in the previous LassoCV model, of the 301 features, 173 were zeroed out, and 128 were kept.

* The train R2 score increased slightly (0.9268 -> 0.9279), as did the validation R2 score (0.9258 -> 0.9262).

* The train RMSE decreased (21,582 -> 21,425), while the validation RMSE increased (20,996 -> 20,945).

Both the train and the validation metrics improved, and the LassoCV model with an alpha of 79.25 became the best-performing model.

#### ElasticNet Regression

The ElasticNetCV model can be used to apply a combination of both ridge (L2) and lasso (L1) regularization to a linear regression model. Given ranges, the model can find the best-performing alpha as well as the best-performing ratio between the regularizations.

It turns out that this model performed best when using a full lasso regularization, seeing that it found the best-performing alpha to be 79.25, just as the second LassoCV model did. As a result, it returned the same metrics as that model did.

#### Best Model

Of all the models, the LassoCV can be said to be the best-performer when using the alpha of 79.25. Though the ElasticNetCV model returned the same results, it only did so because it was using a full lasso regularization. In cases such as this one, where there are an excess of features to consider, reducing the amount of predictors is necessary, and the elimination of more than half of the predictors by using regularization resulted in optimal performance. As a result, the LassoCV model with the alpha of 79.25 will be used to draw insights from.

---

## Best Model Insights

### Neighborhood Impact on Home Sale Price

Of the 28 neighborhoods, 7 were assigned a positive coefficient, 14 were eliminated and 7 were assigned a negative coefficient.

The top 5 neighborhoods that increase home value are:

* Green Hills by 48k
* Stone Brook by 42k
* Northridge by 27k
* Northridge Heights by 25k
* Crawford by 12k

The bottom 5 neighborhoods that decrease home value are:

* Edwards by 9k
* Gilbert by 3k
* Old Town by 3k
* Northwest Ames by 3k
* North Ames by 2k

### Home Feature Impact on Home Sale Price

The top 5 home features that increase home value are:

* Exterior Material Quality - Excellent by 30k
* Above Ground Living Area Sqft by 22k
* Roof Material - Wood Shingle by 22k
* Kitchen Quality - Excellent by 19k
* 2nd Garage by 15k

The bottom 5 home features that decrease home value are:

* Roof Material - Clay or Tile by 396k
* Elevator by 207k
* Court Officer Deed/Estate Sale Type by 10k
* Masonry Veneer Type - Brick Common by 6k
* Basement Exposure - None by 5k

---

## Conclusion

### Recommendations

It's recommended that the city of Ames, IA invest in housing in the Green Hills, Stone Brook, Northridge, Northridge Heights and Crawford neighborhoods.

The following housing features should also be considered:

* Excellent Exterior Material Quality (and avoid  Common Brick)
* Above Ground Living Area Square Footage
* Wood Shingle Roofing (and avoid Clay/Tile)
* Excellent Kitchen Quality
* 2nd Garage
* Avoiding unnecessary luxury features (elevator)

### Next Steps

It will be beneficial to gain a deeper understanding of how each rating is defined, if not already stated, for those categorical features that were ordinal. For example, the difference between average, god, excellent, etc. 

Also, given that the dataset of this analysis only contained observations ranging from 2006-2011, a follow-up analysis on an updated dataset is suggested to see if the findings of this analysis continue to hold true.