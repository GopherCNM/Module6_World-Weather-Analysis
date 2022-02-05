# WeatherPy with Python APIs  

## Overview of the project

The purpose of this project is to build on the travel app functionality that was developed with the help of our colleague, Jack. I built out 3 features with new knowledge I gained of APIs and Python’s citipy module.  

1. Use Python’s NumPy module to randomly generate 2,000 latitude/longitude combinations, and use the citipy module to identify the nearest city for each set of coordinates. This ultimately resulted in a list of 721 unique cities. Then, I used the OpenWeather API to pull in current weather conditions for these cities. I used try-except blocks to skip cities that weren’t found in the OpenWeather API call. I exported the final list of 670 cities, along with current weather, to a CSV file.

2. For this feature, I built an input prompt to allow users to specify their desired temp range for their vacations. Using the list of 670 cities (from part 1), I used .loc to filter the list to only cities that fit the desired temp range criteria. For each of these cities, I made a call to the Google Places API, using its Nearby Search method, to pull in the first hotel for each of these cities. I dropped any cities that didn’t have hotels, and saved the list of 215 cities and hotel information to a CSV file. I also added a marker layer using the Google Maps API to add map markers for all cities. When clicked, the markers display information such as the city and country, hotel name, and current weather.

3. Finally, I selected 4 cities from the list of 215 cities, and created a driving itinerary using the Google Directions API. I selected 4 cities in Peru, starting and ending in the city of Huarmey. I pulled these 4 cities into a new DataFrame and mapped them on their own map with markers.
