# Airbnb CT analysis overview

This project is an exploratory data analysis of Airbnb dataset of Cape Town listings for Udacity's Write A "Data Science Blog Post" project.

Data used can be found on the Inside Airbnb site: http://insideairbnb.com/get-the-data.html

## Libraries used

```bash
import pandas as pd
import geopandas as geopd
import folium
from folium.plugins import MarkerCluster
from folium import IFrame
import glob
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
```

Pandas and Geopandas are used to manipulate and analysis the datasets, along with Numpy which is standard.

Folium is used to generate an interactive choropleth map of the areas.

Matplotlib and Seaborn are used for chart generation.

## Motivation

I decided to go with the Cape Town Airbnb dataset because the city's property prices are known to be high and are always interesting to make better sense of. The main questions this notebook explores are:

1) when are the most popular times to hike up the prices of listings;
2) which areas have the most expensive listings on average and;
3) what contributes most to the price of a listing.

## Files

The files in the repository includes the following:

- airbnb_ct_eda.ipynb - this is the notebook used for the analysis
- calendar.csv.gz - the price of each listing over time
- listings.csv.gz - page information of the listings including ratings, locations and accommodation specifications
- reviews.csv.gz - reviews of each listing (this file has mostly been excluded from the analysis)
- neighbourhoods.geojson - the locations of each ward in Cape Town
- price_df.csv - the prices of the listings that have been parsed to show each one's mean, min and max. I'm including this here as the code takes a couple of minutes to generate the df.

## Overall findings

Some of the findings include that costs are lowest the closer we more to the present date. This is perhaos an indicator that hosts tend to rake up prices over the long run and bring them down as the date approaches to fill up more rooms.

The Atlantic Seaboard are the most expensive along with the inner City. Specific neighbourhoods include Camps Bay and Hout Bay.

Large price correlations include the number of bathrooms, accommodates, square feet and bedrooms.

![alt text](https://cdn-images-1.medium.com/max/2600/1*umGJozQ0DWFLz2LUo5vBWw.jpeg)

A Medium blog post of the above code which dives into the process of the analysis can be found here: https://medium.com/@plan__b/this-airbnb-data-will-make-you-think-twice-about-cape-town-accommodation-costs-7d31e90178eb
