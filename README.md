# WeatherPy

## Overview

This repository holds the updates to the PlanMyTrip app.  This app allows users to chose vacation destinations based on current weather criteria.  The updates include:
  1. Addition of "current weather" descriptions to information lists by city
  2. Introduction of Travel itinerary functionality.  Creates travel paths and attaches weather data to defined cities using google maps, places, and directions API's

## Attachments

### Weather Data
  1. **Weather_Database.ipynb**  - creates dataframe of cities (citypy generated) based on randomly chosen Latitude and longitude (with numpy np.random) and connects to OpenWeather.com API's to collect and store current weather information by city
  2. **Weather_Database/WetherPy_Database.csv** - output csv from **Weather_Database.ipynb**

### Vacation Search
  1. **Vacation_Search.ipynb** - uses data from **Weather Data** to access google places API and chooses a hotel destination in the city specifed.  The hotel name was extracted from output JSON's and merged with the prior weather destination to create a new dataframe.  The hotel info dataframe data was used to create a google mpas output with markers that allow the user the abillity to click on an output destination based on desired vacation temperatures.  The result shows the hotel, city, country, and current weather.
  2. **Vacation_Search/WetherPy_vacations.csv** - output csv of dataframe with city, weather, location, and hotel information
  3. **Vacation_Search/Wether_vacation_map** - png of graphical google map output.

### Vacation Itinerary
  1.**Vacation_Itinerary.ipynb** - using google directions,**Vacation_Search/WetherPy_vacations.csv** was used and four destintations were chosen and seperated from the data frame.  Using google destinations a route was created between the four, and the weather information (as in **Vacation Search**) were inserted as markers for the destinations.
  2. **Vacation_Itinerary/WeatherPy_travel_map.png** - output google directions for 4 chosen cities
  3. **Vacation_Itinerary/WeatherPy_travel_map_Markers.png** - output google map with weather markers.
  
