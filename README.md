# Zillow-Housing-Data-Project
Overview

Over the past decade, the prices in the housing market have increased dramatically in all parts of the Bay Area. Several young prospects have been waiting quite a few years now to be able to purchase a standard single-family home with these prices. It is almost given that any standard, single-family home in the Bay Area is not less than $1.5 million. In this first part of the project(Part_1.ipynb),  data was obtained by web scraping and cleaning to gather information about various aspects of the several home listings found on Zillow.com.

Steps Followed

Web Scraping -> Data Cleaning -> Exploratory Analysis -> Model Creation -> Conclusion

Web Scraping

Loaded the data from first four pages for 20 defined cities.
Extracted the URLs for each of the listed properties and extracted the attributes like street address, city, state, zipcode, latitude and longitude, price, YearBuilt, LotSize, HomeType, Zestimate, Bedrooms, Bathrooms, LivingArea, HOA, BrokerageName, LastSoldPrice, HomeStatus, Parking.

Web Scraping - Technical Challenges

Problem:

Zillow has a built-in security system where if you hit their website repeatedly, they would block you for a few hours.

Solution:

Made the header requests as close as possible to a regular user.

Implemented a randomized delay between request calls

After every page, sleep for 2 seconds

After every property links, sleep between 2 to 10 seconds

Dataset Overview

713 listing records from 20 cities in Bay Area.
19 Attributes related to listing Address, specifications, Broker Information and Price.
Attributes of Text, Numeric, and Categorical data types.

The attributes were:
StreetAddress, "City", "State", "ZipCode", "Latitude", "Longitude",	"Price", "YearBuilt",	"LotSize", "HomeType", "Zestimate", "Bedrooms", "Bathrooms", "LivingArea", "HOA", "BrokerageName", "LastSoldPrice",	"HomeStatus",	"Parking"


Data Cleaning

Extracted the data from the website and then converted it into a csv file. Used the same csv file to load the data back into a data frame.

Removed the duplicates using the df.drop function.

Removed the records where the street address was not available.

Checked the missing values and removed / replaced them using df.isna() and df.dropna().

Checked and updated the data types using df.dtypes function.

Outlier - Data Cleaning

Used a box plot to identify the outliers using seaborn and matplotlib.

Using the above libraries we were able to identify the outliers and remove them.

Created a new box plot to re-verify the outliers.

Research Questions 

Questions to answer from this analysis

The Most Famous city in terms of Property listing 

Which city in Bay Area has the highest appreciation ratio

The Most Famous city in terms of Property Median price

Broker with the highest number of property listings

Median price by Home Type

Most significant attribute that impacts the Price 


Answers

The most famous city in terms of property listing

Based on the number of properties by city  San Jose is the most famous city in the Bay Area in terms of property listings. 

City in Bay Area with the highest appreciation ratio

While several Bay Area cities have their homes appreciate in value rapidly, Pleasanton has the highest appreciation ratio of them all coming in at about 0.65. However, not too far behind are Danville, San Mateo, and Cupertino with appreciation ratios of no less than 0.55.

Most Famous city in terms of Property Median price

Cupertino is the most famous Bay Area city in terms of Property Median price. 

Broker with the highest number of property listings

Compass is the brokerage that has the most listings and dominates Zillow’s websites of Bay Area property listings. 

Median price by Home Type

For Single-Family homes, the median price is around 1.35 million

For Multi-Family homes, the median price is around 1.31-1.32 million

For Townhomes, the median price is around 900,000

For Condos, the median price is around 750,000

Most significant attribute that impacts the Price

"Living Area" has a high 0.68 correlation with Price. "Bedrooms" and "Bathrooms" are also significant factors in impacting a home’s price in the Bay Area, coming in at a correlation of 0.61 and 0.51 respectively, but fall short behind Living Area.
HOA price has a negative correlation with the price of a home (-0.25)

Data Modelling


Utilized Gradient Boosting and Linear Regression model to predict the price.

GB model was found to be a better model when compared to the linear regression model. 






