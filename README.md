# python-api-challenge
### Background

Weather is constantly changing, but it can be helpful to analyze weather patterns across the globe and uncover trends about why places have the weather they do, such as their distance from the equator. Utilizing Python requests, APIs, and JSON traversals, I uncovered some cool trends about different cities and the weather they had at the specific time and day of my API request: January 05, 2021.

### 3 Observations

- As cities move farther away from the equator, their maximum temperatures decrease gradually. This corresponds with what most people expect, since the equator is typically assumed to have warmer and more stable tempteratures year-round due to the fact that sunlight hits the Earths surface from almost directly above.

- Though there was no strong correlation suggested in the scatter plot for wind speed vs. latitude, it is important to note that the vast majority of cities have wind speeds from 0 to low-20s, with very few cities lying above the 25mph mark.

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

For this part of the analysis, I started by creating a heat map that displays the humidity for every city from Part I.

I then narrowed down my DataFrame to find my ideal weather condition and dropped the cities which didn't meet the conditions.
My ideal weather conditions are:

- A max temperature equal to or lower than 85 degrees but higher than 72 degrees.

- Wind speed being less than 5 mph.

- Cloudiness less than or equal to 30%, since blue skies with nice clouds is hard to beat!

After gathering the cities which met my weather conditions, I used the Google Places API to find the first hotel for each city located within 5000 meters of their coordinates.

Finally, I plotted the hotels on top of the humidity heatmap I made earlier, with a pin on each city displaying the Hotel Name, City, and Country.

#### Instructions to Run Code

- Save this repository in your desired location, then cd into that directory in git bash (or terminal if OS user).
- Type jupyter notebook into terminal.
- Once in jupyter notebook, open each .ipynb file and run through each section of the script.
###### Note**: Make sure to enter your own API Key for VacationPy. You can create an API key by going to the Google API Console.
- Once you create your Google API Key, enable: Places API, Maps JavaScript API, and Geocoding API.
- Place your API key into the api_keys file in the VacationPy directory and run the script in jupyter notebook.
- Feel free to use to the given API key for WeatherPy, as it is not linked to any billing account. Or enter your own (from OpenWeatherMap).
