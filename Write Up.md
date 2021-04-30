# Ratatouille Radar - A Data Science Solution for NYC DOH Restaurant Inspections

Crystal Huang

## Abstract

This project is a data science solution for New York City Department of Health to help restaurant inspectors efficiently identify restaurant health code violation by better understanding rodent sighting pattern in various neighborhoods in NYC. The project uses the NYC Restaurant Inspection data, NYC 311 Calls for rodent sighting reports, and NYC current restaurant data. With the predictive model, restaurant inspectors can catch the same or more number of health code violation with less inspection conducted by better targeting city resources at what appear to be ratty-kittchen hotspots. After preliminary analysis, in addition to visualizations, the Tableau interactive dashboard can be used as prototype of this project to identify the restaurants in high-risk area for rodent violations based on sightings pattern. 

## Design

**Backstory:** Last year, when the pandemic hits, restaurants were shut down in March and so did the inspections. Restaurants were reopened with outdoor dining in June, 2020. But it wasn't until October when restaurant inspection resumed. NYC encountered another problem in March of this year - a surge of rodent sightings in the city as COVID restrictions are lifted. The main challenge for NYC Health now is the delay in restaurant inspection, and a high volumne of restaurants to inspect. There is also an increased risk of undetected rodent infection and public's exposure to foodborne illnesses that the rodents might be carrying

**Target audience:** NYC Health Department

**Opportunity:** to help NYC Health restaurant inspectors efficiently identify restaurant health code violations

**Data Science Solution:** Using 311 call data of rodent sighting reports to prioritize high-risk restaurants for inspection, identify which restaurants are at most risk for rodent infestation and when restaurants may have higher risk of encountering rodent infestation. 

**Impact hypothesis:** Using the prediction model, NYC Health restaurant inspectors can identify the same or a greater number of violations with fewer inspections by better targeting city resources at what appears to be ratty-kitchen, so they may be able to increase conversions and safer restaurants by educating the restaurants that are in high-risk zone for rodent infestation.

**Measure of Success:** 

- non-technical : efficiency of restaurant inspection
- Technical: model metrics for predictive model

## Data

The datasets used in this project include the [NYC Restaurant Inspection Results](https://data.cityofnewyork.us/Health/DOHMH-New-York-City-Restaurant-Inspection-Results/43nn-pn8j), [NYC 311 Calls](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9), and [NYC Restaurants](https://data.cityofnewyork.us/Transportation/Open-Restaurants-Inspections/4dx7-axux) from NYC open data. Those data set were too large to read in Excel directly. So I created a SQL database to store the dataset and used sqlalchemy to accesss the data in Python. Then, I took a subset of relevant data with pandas and store it as csv file to access in Excel. 

**Subset of data:**

* NYC 311 call - Rodent Sighting reports in Commercial buildings
* NYC Restaurant Inspection with Rodent violation in 2019

**Risk and Assumptions:**

* Most rodent sightings are reported through 311 calls
* Most of the restaurants are in commerical buildings
* Most violation were caught in the year without pause in inspection

## Algorithms

**Preliminary Analysis:** Exploratory analysis and visualization of rodent sightings in various neighborhoods in NYC where restaurants are located.

*Exploratory Data Analysis*

In the time series graph of rodent sightings, there is a trend that shows an increase of sighting around spring and decrease near winter. Comparing the sightings across NYC boroughs, the pattern shows that Brooklyn has the greatest number of rodent sightings in NYC. 

Further investigating on sightings in different types of building, it shows the residential buildlings have the most sightings. Since most of the restaurants in NYC are in commercial buildings, I took the subset of commercial areas and compare the sightings across boroughs. A paired barplot shows that Manhattan has the greatest number of rodent sightings in NYC commercial areas, which correlates with the pattern of the past rodent violation observed at restaurant inspection. There is more residential buildings in Brooklyn than in Manhattan, which is why Brooklyn exhibits the highest sightings in the overall comparison.

*Visualization*

With paired bar plot and geomap comparison of Rodent sightings and violations in 2019, there is a similar pattern between the sightings and violations. The line plot timeseries graph not only shows that Manhattan and Brooklyn have higher rodent sightings, but also shows the trend of number increase in spring and decrease in winter. 

With Python Folium heatmaps, you can also see the higher sighting pattern in Manhattan and Brooklyn during non-pandemic times. 

In addition to the analysis and graphs, the [Interactive Tableau Dashboard](https://public.tableau.com/profile/crystal.huang2109#!/vizhome/shared/TBDSBF44Z) can be used as prototype of this project to identify the restaurants in high-risk area for rodent violations based on sightings pattern. 

**Future Analysis:** Build a predictive model of that rank the NYC restaurants by likelihood of having rodent violations with historical rodent sightings and time series, and identify dirty-kitchen hotspots with yelp reviews

## Tools

- SQLite for creating database
- sqlalchemy for accessing SQL database in Python
- Numpy and Pandas for data manipulation
- Excel for Exploratory Data Analysis
- Excel and Tableau for plotting data visualization and interactive dashboard
- Folium for Spatial visualization with time series

* (attempted at classificataion model but the dataset was highly imbalanced)

## Communication

In addition to the slides and visual presented, the [Tableau interactive dashboard](https://public.tableau.com/profile/crystal.huang2109#!/vizhome/shared/TBDSBF44Z) will be embedded on my personal blog
