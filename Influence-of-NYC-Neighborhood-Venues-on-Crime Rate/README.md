# Influence of NYC Neighborhood Venues on Crime Rate


## Introduction

*New York City is the most populous city in the United States, home to the
headquarters of the United Nations and an important center for international
diplomacy. It just might be the most diverse city on the planet, as it is home
to over 8.6 million people and over 800 languages.*

Undoubtedly, **Public Safety** becomes important for an ethnically diverse
metropolis. The idea of this project is to categorically segment the
neighborhoods of New York City into major clusters and examine their respective
crime rate. A desirable intention is to examine the neighborhood cluster more
susceptible or prone to criminal activities. Further examination might reveal if
the crime rate has any positive relationship with nightlife spots, or any
negative relationship with government building, or vice versa.

This project will help to understand the influence of venues in a neighborhood
on the regional criminal activities. Exploratory Data Analysis (EDA) will be
taken forth with a broad category of venues supplemented by Foursquare API. And,
upon exploration that can be further narrowed down to the most dominant ones. I
believe that this revelation or relationship between venues and crime rates will
help **New York Police Department (NYPD)** to not only increase surveillance but
also to scrutinize the operations and functionalities of crime dominant neighborhood's
venues.


## Data

To examine the above said, following data sources will be used:

1.  **New York City Dataset**
    1.  Link: <https://geo.nyu.edu/catalog/nyu_2451_34572>
    2.  Description: This New York City Neighborhood Names point file was created as a guide to New York City’s neighborhoods that appear on the web resource, “New York: A City of Neighborhoods.” Best estimates of label centroids were established at a 1:1,000 scale, but are ideally viewed at a 1:50,000 scale. This dataset will provide the addresses of neighborhood of NYC in json format. An extract of the json is as follows:
```
		{'type': 'Feature',
		'id': 'nyu_2451_34572.306',
		'geometry': {'type': 'Point',
		'coordinates': [-74.08173992211962, 40.61731079252983]},
		'geometry_name': 'geom',
		'properties': {'name': 'Fox Hills',
		'stacked': 2,
		'annoline1': 'Fox',
		'annoline2': 'Hills',
		'annoline3': None,
		'annoangle': 0.0,
		'borough': 'Staten Island',
		'bbox': [-74.08173992211962,
		40.61731079252983,
		-74.08173992211962,
		40.61731079252983]}}
```

2.  **Foursquare API:**
    1.  Link: <https://developer.foursquare.com/docs>
    2.  Description: Foursquare API, a location data provider, will be used to make RESTful API calls to retrieve data about venues in different neighborhoods. This is the link to [Foursquare Venue Category Hierarchy](https://developer.foursquare.com/docs/resources/categories). Venues retrieved from all the neighborhoods will be categorized broadly into "Arts & Entertainment", "College & University", "Event", "Food", "Nightlife Spot", "Outdoors & Recreation", etc. An extract of an API call is as follows:
```
		'categories': [{'id': '4bf58dd8d48988d110941735',
		   'name': 'Italian Restaurant',
		   'pluralName': 'Italian Restaurants',
		   'shortName': 'Italian',
		   'icon': {'prefix': 'https://ss3.4sqi.net/img/categories_v2/food/italian_',
		   'suffix': '.png'},
		   'primary': True}],
		'verified': False,
		'stats': {'tipCount': 17},
		'url': 'http://eccorestaurantny.com',
		'price': {'tier': 4, 'message': 'Very Expensive', 'currency': '$'},
		'hasMenu': True,
		'likes': {'count': 30,
		'groups': [{'type': 'others', 'count': 30, 'items': []}],
		'summary': '30 Likes'},
```


3.  **NYPD Complaint Data Historic**
    1.  Link: <https://data.cityofnewyork.us/Public-Safety/NYPD-Complaint-Data-Historic/qgea-i56i>
    2.  Description: This dataset includes all valid felony, misdemeanor, and violation crimes reported to the New York City Police Department (NYPD) from 2006 to the end of 2017. Intent would be to create choropleth map of crimes in the city using the latitude and longitude data provided.