# python-api-challenge
### Background

Weather is constantly changing, but it can be helpful to analyze weather patterns across the globe and uncover trends about why places have the weather they do, such as their distance from the equator. Utilizing Python requests, APIs, and JSON traversals, I uncovered some cool trends about different cities and the weather they had at the specific time and day of my API request: January 05, 2021.

### 3 Observations

- As cities move farther away from the equator, their maximum temperatures decrease gradually. This corresponds with what most people expect, since the equator is typically assumed to have warmer and more stable tempteratures year-round due to the fact that sunlight hits the Earths surface from almost directly above.

- Though there was no strong correlation suggest in the scatter plot consisting of wind speed and latitude, it is important to note that the vast majority of cities have wind speeds from 0 to low-20s, with very few cities lying above the 25mph mark.

- Cloudiness does not appear to have much correlation with latitude, however there is several cities which show 100% cloudiness, and 0% cloudiness. It would be interesting to dive deeper to see which cities reported 0% cloudiness and others which had 100% cloudiness, and see if common regions can be pin-pointed to note whether certain regions are generally more cloudy than others.

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
