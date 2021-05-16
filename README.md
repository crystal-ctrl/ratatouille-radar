# Ratatouille Radar

A Data Science Solution for NYC DOH Restaurant Inspections

## Goal

This project is a data science solution for New York City Department of Health to help restaurant inspectors efficiently identify restaurant health code violation by better understanding rodent sighting pattern in various neighborhoods in NYC. The project uses the NYC Restaurant Inspection data, NYC 311 Calls for rodent sighting reports, and NYC current restaurant data. With the predictive model, restaurant inspectors can catch the same or more number of health code violation with less inspection conducted by better targeting city resources at what appear to be ratty-kittchen hotspots. After preliminary analysis, in addition to visualizations, the Tableau interactive dashboard can be used as prototype of this project to identify the restaurants in high-risk area for rodent violations based on sightings pattern. 

To learn more, see my [blog post](https://crystalhuang-ds.medium.com/proposing-a-data-science-solution-to-a-real-life-problem-b7668719da4e), [Presentation Slides](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/Presentation%20slides.pdf), and the [Tableau interactive dashboard](https://public.tableau.com/profile/crystal.huang2109#!/vizhome/shared/TBDSBF44Z).

## Workflow

1. [Data Acquisition](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/1_Data%20acquisitions.ipynb)
2. EDA with Excel</br>
    a. [311call](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/2A_311calls_EDA_DataViz.xlsx)</br>
    b. [Restaurant Inspections](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/2B_Restaurant%20inspections_EDA_DataViz.xlsx)</br>
    c. [Restaurant Data](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/2C_Restaurants_data.xlsx)
3. [Tableau Workbook](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/3_Ratatouille%20Radar.twbx)
4. [Python Folium Map Analysis](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/4_Spatial%20visualization%20with%20Folium.ipynb)
5. [(attempt with classification model)](https://github.com/crystal-ctrl/ratatouille-radar/blob/main/5_Classification%20model%20%5Battempt%5D.ipynb)

## Technologies

- SQLite
- sqlalchemy
- Python (Numpy and Pandas)
- Excel
- Tableau
- Folium