# Flatiron Data Science Project 2: Linear Regression

## Primary Goals:

## Introduction
AirBnB is an internet marketplace where users can both rent and rent out accomodations. One of the biggest challenges of AirBnB is finding the right price per night to set an accomodation. In this project we will be looking at the factors that have the highest impact in order to estimate the price per night of an AirBnB rental in the five boroughs of New York City.

### Business Case
Since 2008, AirBnB has acted as an online retailer for short term rentals. There has been a great debate between whether or not short term rentals should be allowed and the aim of this project is to create a model that can predict price in order to entice landowners into renting out their property using AirBnB.

### About our Data
Our data set was downloaded from http://tomslee.net/airbnb-data-collection-get-the-data

It contains the following elements:

room_id: A unique number identifying an Airbnb listing.

host_id: A unique number identifying an Airbnb host.

room_type: One of “Entire home/apt”, “Private room”, or “Shared room”

borough: A subregion of the city or search area for which the survey is carried out. The borough is taken from a shapefile of the city that is obtained independently of the Airbnb web site. For some cities, there is no borough information; for others the borough may be a number. If you have better shapefiles for a city of interest, please send them to me.

neighborhood: As with borough: a subregion of the city or search area for which the survey is carried out. For cities that have both, a neighbourhood is smaller than a borough. For some cities there is no neighbourhood information.

reviews: The number of reviews that a listing has received. Airbnb has said that 70% of visits end up with a review, so the number of reviews can be used to estimate the number of visits. Note that such an estimate will not be reliable for an individual listing (especially as reviews occasionally vanish from the site), but over a city as a whole it should be a useful metric of traffic.

overall_satisfaction: The average rating (out of five) that the listing has received from those visitors who left a review.

accommodates: The number of guests a listing can accommodate.

bedrooms: The number of bedrooms a listing offers.

price: The price (in US) for a night stay. In early surveys, there may be some values that were recorded by month.

minstay: The minimum stay for a visit, as posted by the host.

latitude and longitude: The latitude and longitude of the listing as posted on the Airbnb site: this may be off by a few hundred metres. I do not have a way to track individual listing locations with

last_modified: the date and time that the values were read from the Airbnb web site.

## Methodology
1. Data Collection

2. Data Wrangling

3. EDA and Visualization

4. Hypothesis Testing

5. Model Development

6. Cross Validation

## Results
Looking at the results, our model is able to predict the value of AirBnB rental with a R score of 0.578.

Iterating on the model and adjusting the price parameters, we chose to segment and remove part of the data. For some reason, the data set contained a large concentration of zeros for price which is not helpful in creating a tool. Even though there is quite a bit of noise between the True Values and the Predicted Values, our model scores are very close. This means the model has very low variance. 

Coefficients with the largest impact:

Accomodation Size had the highest correlation with price, this intuitively makes sense as larger bookings usually come at a higher cost.

Prices vary between Boroughs. Brooklyn and Manhattan are the most popular and therefore tend to be more expensive while Queens and Staten Island were the cheapest.

Offering an Entire House instead of just a private room demonstrated higher prices.


## Conclusion 
The purpose of this project was to be able to predict the price of an accomodation for a night in New York City through AirBnB. While the debate has mostly gone away, this model can be used to entice landowners into using AirBnB to book short term rentals and help them choose a price per night.

But after going through all of the data we notice that there were some shortcomings. The model isn't going to be great at predicting 'new' rentals to the market. Some of the points we cut out were listings that had zero reviews. Also, the model has included geographic position data but does not include competitive information such as proximity to entertainment or grocery stores.

A more complete data set would yield better results, however for a first iteration, we propose the above shown models.

