# python-api-challenge
### Background

Weather is constantly changing, but it can be helpful to analyze weather patterns across the globe and uncover trends about why places have the weather they do, such as their distance from the equator. Utilizing Python requests, APIs, and JSON traversals, I uncovered some cool trends about different cities and the weather they had at the specific time and day of my API request: January 05, 2021.

## WeatherPy

In this example, I creating a Python script to visualize the weather of over 500 cities across the world with varying distance from the equator. I utilized a simple Python library and an API Key from OpenWeatherMap to construct representative models of the weather across world cities on January 05, 2021.

For the first part of my analysis, I created a series of scatter plots to showcase the following relationships:

- Temperature (F) vs. Latitude
- Humidity (%) vs. Latitude
- Cloudiness (%) vs. Latitude
- Wind Speed (mph) vs. Latitude

I then added a simple observation for each scatter plot describing what each plot suggests.

For the second part of my analysis, I ran a linear regression on each relationship listed above after separating the plots by Northern and Southern Hemisphere. 

After each pair of plots, I showed the r-squared value and a description of any relationships I noticed.

The script is in the WeatherPy directory titled "WeatherPy.ipynb", and .pngs of each plot is included in the output_data folder of the WeatherPy directory along with the city_weather.csv file I conducted my analysis with after cleaning the data I received from the API request.

## VacationPy
