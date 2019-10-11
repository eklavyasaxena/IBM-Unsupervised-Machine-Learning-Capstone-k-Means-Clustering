## Categorical Segmentation of NYC Neighborhoods and Crime Rate

**Introduction**

_New York City is the most populous city in the United States, home to the headquarters of the United Nations and an important center for international diplomacy.__It just might be the most diverse city on the planet, as it is home to over 8.6 million people and over 800 languages._

Undoubtedly, **Public Safety** becomes important for an ethnically diverse metropolis. The idea of this project is to categorically segment the neighborhoods of New York City into major clusters and examine their respective crime rate. A desirable intention is to examine the neighborhood cluster more susceptible or prone to criminal activities. Further examination might reveal if the crime rate has any positive relationship with nightlife spots, or any negative relationship with government building, or vice versa.

This project will help to understand the influence of venues in a neighborhood on the regional criminal activities. Exploratory Data Analysis (EDA) will be taken forth with a broad category of venues supplemented by Foursquare API. And, upon exploration that can be further narrowed down to the most dominant ones. I believe that this revelation or relationship between venues and crime rates will help **New York Police Department (NYPD)** to not only increase surveillance but also to scrutinize the operations and functionalities of crime dominant venues.

**Data**

To examine the above said, following data sources will be used:

1. Foursquare API:
  1. Link: [https://developer.foursquare.com/docs](https://developer.foursquare.com/docs)
  2. Description: Foursquare API, a location data provider, will be used to make RESTful API calls to retrieve data about venues in different neighborhoods.
2. New York City Dataset
  1. Link: [https://cocl.us/new\_york\_dataset](https://cocl.us/new_york_dataset)
  2. Description: Provides the addresses of neighborhood of NYC in json format.
3. NYPD Complaint Data Historic
  1. Link: [https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i](https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i)
  2. Description: This dataset includes all valid felony, misdemeanor, and violation crimes reported to the New York City Police Department (NYPD) from 2006 to the end of 2017.