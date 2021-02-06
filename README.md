# Python API Homework - What's the Weather Like?

## Background

Whether financial, political, or social -- data's true power lies in its ability to answer questions definitively. So let's take what you've learned about Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

Now, we know what you may be thinking: _"Duh. It gets hotter..."_

But, if pressed, how would you **prove** it?

In this repository, I display how one would do so!!

![Equator](Images/equatorsign.png)

## Part I - WeatherPy

In this section of the homework I created a Python script to visualize the weather of over 600 cities across the world of varying distance from the equator.
To accomplish this, I utilized a [simple Python library](https://pypi.python.org/pypi/citipy), the [OpenWeatherMap API](https://openweathermap.org/api), and a little creative mainpulation to produce a representative model of weather across world cities.

Initially I created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, a few bullet points were added that gave a brief analysis of what the code was doing and what the plots displayed.

Secondly, I ran a linear regression on each relationship. This time, the plots were seperated into different plots for negative and positive latitudes:

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

Similar to the plots before, a brief analyis of the visualizations were given after.

### Part II - VacationPy

In this part of the assignment, the following tasks were completed:

* A heat map displaying the humidity for every city from Part I.

  ![heatmap](Images/heatmap.png)

* The DataFrame was narrowed down to find my ideal vacation weather condition. Such as:

  * A max temperature lower than 80 degrees but higher than 70.

  * Wind speed less than 10 mph.

  * Zero cloudiness.

* Then, using Google Places API, the first hotel for each city located within 5000 meters of each of those coordinates was found.

* The hotels were then plotted on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.

  ![hotel map](Images/hotel_map.png)

## Overview:

* OpenWeather API calls were used to provide weather data for randomly generated cities using Python's Citipy module.
* This data included a variety of metrics: location, temperature, humidity, cloudiness, and wind speed.
* Once collected and stored in a csv, the csv was then imported into a pandas data frame for manipulation and analysis.
* The analysis of this dataframe produced a variety of graphical comparisons explained in detail above.
* A brief analyis of each of the graphical comparisons were given following each's production.

## Deliverables:

* The images and csv files mentioned above can be found in the "output_data" folder of this respository.
* The visualizations produced in the second part of the assignment can be found in the images folder.
* The completed jupyter notebook files for each part of the assignment can be found in the "starter_code" folder of this repository (WeatherPy & VacationPy).
