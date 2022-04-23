# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 2: Increasing the Home Value in Ames, IA

---

## Purpose

### Problem Statement

As of March 2022, the median home value in Ames, Iowa is 286,826 dollars. The median home value has not seen much consistency with year over year percent changes  in the past 5 years due to the housing crash in 2018-2019 and post COVID-19 economic effects in 2021-2022.

The city of Ames is interested in identifying ways in which they and their residents can do their part to help increase the city’s median home value in spite of the continuing post COVID-19 economic effects.

This project aims to identify specific housing features that have a high impact on a home’s value, so that the city knows what to consider when building new housing and residents know what to consider when building, updating or selling their home. 


### Background

According to historical rates of home appreciation, the universal 'normal' rate of appreciation for the housing market is between 3-5%.  According to Zillow, the Ames, IA median home values for the past 5 years are as follows:

|**Month/Year**|**Median Home Value**|**Percent Change**|
|---|---|---|
|**March 2018**|234k|+4.0%|
|**March 2019**|234k|+0.0%|
|**March 2020**|239k|+2.1%|
|**March 2021**|249k|+4.2%|
|**March 2022**|289k|+15.1%|

The city has mostly fallen within the 2-4% range. The 2 exceptions are in 2019, due to the housing crash that began in the summer of 2018, and in 2022, due to the post COVID-19 economic effects.

---

## Data

### Dataset

The Ames, IA housing data set was obtained directly from the Ames Assessor’s Office. It contains 81 columns which include 22 nominal, 23 ordinal, 14 discrete, and 20 continuous variables (and 2 additional observation identifiers).


### Data Dictionary

|**Feature**|**Data Type**|**Description**|
|---|---|---|---|
|**Id**|*int*|Identification number.|
|**PID**|*int*|Parcel identification number - can be used with city web site for parcel review.|
|**MS SubClass**|*Nominal - int*|Identifies the type of dwelling involved in the sale.|
|**MS Zoning**|*Nominal - object*|Identifies the general zoning classification of the sale.|
|**Lot Frontage**|*Continuous - float*|Linear feet of street connected to property.|
|**Lot Area**|*Continuous - float*|Lot size in square feet.|
|**Street**|*Nominal - object*|Type of road access to property.|
|**Alley**|*Nominal - object*|Type of alley access to property.|
|**Lot Shape**|*Ordinal - object*|General shape of property.|
|**Land Contour**|*Nominal - object*|Flatness of the property.| 
|**Utilities**|*Ordinal - object*|Type of utilities available.|
|**Lot Config**|*Nominal - object*|ACT|Lot configuration.|
|**Land Slope**|*Ordinal - object*|Slope of property.|
|**Neighborhood**|*Nominal - object*|Physical locations within Ames city limits.|
|**Condition 1**|*Nominal - object*|Proximity to various conditions.|
|**Condition 2**|*Nominal - object*|Proximity to various conditions (if more than one is present).|
|**Bldg Type**|*Nominal - object*|Type of dwelling.|
|**House Style**|*Nominal - object*|Style of dwelling.|
|**Overall Qual**|*Ordinal - int*|Rates the overall material and finish of the house.|
|**Overall Cond**|*Ordinal - int*|Rates the overall condition of the house.|
|**Year Built**|*Discrete - int*|Original construction date.|
|**Year Remod/Add**|*Discrete - int*|Remodel date (same as construction date if no remodeling or additions).|
|**Roof Style**|*Nominal - object*|Type of roof.|
|**Roof Matl**|*Nominal - object*|Roof material.|
|**Exterior 1**|*Nominal - object*|Exterior covering on house.|
|**Exterior 2**|*Nominal - object*|Exterior covering on house (if more than one material).|
|**Mas Vnr Type**|*Nominal - object*|Masonry veneer type.|
|**Mas Vnr Area**|*Continuous - float*|Masonry veneer area.|
|**Exter Qual**|*Ordinal - object*|Evaluates the quality of the material on the exterior.|
|**Exter Cond**|*Ordinal - object*|Evaluates the present condition of the material on the exterior.|
|**Foundation**|*Nominal - object*|Type of foundation.|
|**Bsmt Qual**|*Ordinal - object*|Evaluates the height of the basement.|
|**Bsmt Cond**|*Ordinal - object*|Evaluates the general condition of the basement.|
|**Bsmt Exposure**|*Ordinal - object*|Refers to walkout or garden level walls.|
|**BsmtFin Type 1**|*Ordinal - object*|Rating of basement finished area.|
|**BsmtFin SF 1**|*Continuous - float*|Type 1 finished square feet.|
|**BsmtFinType 2**|*Ordinal - object*|Rating of basement finished area (if multiple types).|
|**BsmtFin SF 2**|*Continuous - float*|Type 2 finished square feet.|
|**Bsmt Unf SF**|*Continuous - float*|Unfinished square feet of basement area.|
|**Total Bsmt SF**|*Continuous - float*|Total square feet of basement area.|
|**Heating**|*Nominal - object*|Type of heating.|
|**HeatingQC**|*Ordinal - object*|Heating quality and condition.|
|**Central Air**|*Nominal - object*|Central air conditioning.|
|**Electrical**|*Ordinal - object*|Electrical system.|
|**1st Flr SF**|*Continuous - int*|First floor square feet.|
|**2nd Flr SF**|*Continuous - int*|Second floor square feet.|
|**Low Qual Fin SF**|*Continuous - int*|Low quality finished square feet (all floors).|
|**Gr Liv Area**|*Continuous - int*|Above grade (ground) living area square feet.|
|**Bsmt Full Bath**|*Discrete - float*|Basement full bathrooms.|
|**Bsmt Half Bath**|*Discrete - float*|Basement half bathrooms.|
|**Full Bath**|*Discrete - int*|Full bathrooms above grade.|
|**Half Bath**|*Discrete - int*|Half baths above grade.|
|**Bedroom**|*Discrete - int*|Bedrooms above grade (does NOT include basement bedrooms).|
|**Kitchen**|*Discrete - int*|Kitchens above grade.|
|**KitchenQual**|*Ordinal - object*|Kitchen quality.|
|**TotRmsAbvGrd**|*Discrete - int*|Total rooms above grade (does not include bathrooms).|
|**Functional**|*Ordinal - object*|Home functionality (Assume typical unless deductions are warranted).|
|**Fireplaces**|*Discrete - int*|Number of fireplaces.|
|**FireplaceQu**|*Ordinal - object*|Fireplace quality.|
|**Garage Type**|*Nominal - object*|Garage location.|
|**Garage Yr Blt**|*Discrete - float*|Year garage was built.|
|**Garage Finish**|*Ordinal - object*|Interior finish of the garage.|
|**Garage Cars**|*Discrete - loat*|Size of garage in car capacity.|
|**Garage Area**|*Continuous - float*|Size of garage in square feet.|
|**Garage Qual**|*Ordinal - object*|Garage quality.|
|**Garage Cond**|*Ordinal - object*|Garage condition.|
|**Paved Drive**|*Ordinal - object*|Paved driveway.|
|**Wood Deck SF**|*Continuous - int*|Wood deck area in square feet.|
|**Open Porch SF**|*Continuous - int*|Open porch area in square feet.|
|**Enclosed Porch**|*Continuous - int*|Enclosed porch area in square feet.|
|**3-Ssn Porch**|*Continuous - int*|Three season porch area in square feet.|
|**Screen Porch**|*Continuous - int*|Screen porch area in square feet.|
|**Pool Area**|*Continuous - int*|Pool area in square feet.|
|**Pool QC**|*Ordinal - object*|Pool quality.|
|**Fence**|*Ordinal - object*|Fence quality.|
|**Misc Feature**|*Nominal - object*|Miscellaneous feature not covered in other categories.|
|**Misc Val**|*Continuous - int*|Value of miscellaneous feature.|
|**Mo Sold**|*Discrete - int*|Month Sold (MM).|
|**Yr Sold**|*Discrete - int*|Year Sold (YYYY).|
|**Sale Type**|*Nominal - object*|Type of sale.|
|**SalePrice**|*Continuous - object*|Sale price.|

---

## Methodology

Machine learning is the process of letting your machine use data to learn the relationship between predictors and responses. In this case, the predictors are the housing features and the responses are the sale prices.

The model used in this analysis was a lasso regression model. It's a supervised, white-box, linear regression model that applies a penalty and shrinks predictor coefficients. Predictor coefficients describe the relationship between a predictor and the response, and lasso regression is helpful in identifying predictors by eliminating predictors. In cases such as this one, where there are an excess of features to consider, reducing the amount of predictors is beneficial, as it will allow the model to produce more accurate results.

Through the use of LassoCV, an iterative process that returns the optimal alpha penalty term, the optimal alpha was found to be 46.4158883361278. This alpha returned a cross validation score of 0.838402361575566, which describes the baseline amount of variability that can be explained when applied to a new dataset.

The R2 scores, which also describes the amount of variability that can be explained, on the training and validation data were 0.9356412511488261 and 0.9274721464439819, respectively, meaning that the model performed better than expected and is a reasonable model to use for this analysis.

---

## Findings

### Home Sale Price Distribution

The distribution of the home sale prices in Ames, IA from 2006-2011 is right skewed, with most home sale prices falling right below the 200,000 dollar mark. 


### Neighborhood Impact on Home Sale Price

With lasso regression, of the 28 neighborhoods in Ames, IA, 8 were assigned a positive coefficient, 12 were eliminated and 8 were assigned a negative coefficient.

The top 5 neighborhoods that increase home value are:

   * Green Hills by 75.2k
   * Stone Brook by 42.3k
   * Northridge by 27.0k
   * Northridge Heights by 23.5k
   * Crawford by 12.1k

The bottom 5 neighborhoods that decrease home value are:

   * Edwards by 8.9k
   * Gilbert by 4.1k
   * Northwest Ames by 3.9k
   * Old Town by 3.0k
   * North Ames by 2.9k


### Home Feature Impact on Home Sale Price

The top 5 home features that increase home value are:

   * Roof Material - Wood Shingle by 40.7k
   * Exterior Material Quality - Excellent by 31.5k
   * Kitchen Quality - Excellent by 18.9k
   * Proximity to a park/greenbelt by 14k
   * Garage Quality - Good by 14k

The bottom 5 home features that decrease home value are:

   * Roof Material - Clay or Tile by 498.2k
   * Elevator by 345.2k
   * Court Officer Deed/Estate Sale Type by 12.7k
   * Roof Style - Mansard by 12.5k
   * Masonry Veneer Type - Brick Common by 10.9k

---

## Conclusion


### Recommendations

It's recommended that the city of Ames, IA invest in housing in the Green Hills, Stone Brook, Northridge, Northridge Heights and Crawford neighborhoods, and invest in more parks and green spaces.

The following housing features should also be considered:

   * Wood Shingle Roofing (and avoid Clay, Tile or a Mansard style)
   * Excellent Exterior Material Quality (and avoid  Common Brick)
   * Excellent Kitchen Quality
   * Good Garage Quality
   * Brick Face Exterior House Covering
   * Second Floor Square Footage
   * Avoiding unnecessary luxury features (elevator, 2 garages)


### Next Steps

It will be beneficial to gain a deeper understanding of how each rating is defined, if not already stated, for those categorical features that were ordinal. For example, the difference between average, god, excellent, etc. 

Also, given that the dataset of this analysis only contained observations ranging from 2006-2011, a follow-up analysis on an updated dataset is suggested to see if the findings of this analysis continue to hold true.