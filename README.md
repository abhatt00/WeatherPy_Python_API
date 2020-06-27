## WeatherPy

Utilizes the OpenWeatherMap API and the citipy library to accomplish the objective.

Your objective is to build a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


## Resources

Data source: cities.csv

Software: Python 3, Jupyter Notebook

URL: OpenWeatherMap.org


# Analysis

1st Observation: The only discernable trend occurs in the Latitude v Temp plot, where it shows that the closer a city is to 20 degrees N of the Equator, the higher the Maximum temperature is for that city. This is shown by the upside-down "V" shape in the scatter plot. 


2nd Oberservation: Although the Latitude v Humidity plot does not show a very strong trend, there is cause to argue that there is a higher frequency of cities that experience humidity the farther North of the Equator a city is. A good way to make a comparison is measuring humidity of the cities in question during different seasons.


3rd Observation: It seems that regardless of Latitude, cities are more likely to experience average wind speeds between 0 and 5 MPH.


Additional observation: After creating a second list of random cities and doing analysis by creating new scatter plots, it is clear that the patterns are not affected by time of year. A few weeks passed between API calls, and the scatter plots appear consistent from first to second city list.


## Generate Cities List
Cities are generated from a combination of 1500 latitude and longitude points. All unique cities are appended into a list to run through the API.

<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Generated_Cities_List_20200611.jpg">



## Perform API Calls
 These cities are cycled through the OpenWeatherMap API until 500 cities are found that have all relevant data points available in the API. 

<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Perform_API_Calls_1.jpg">

For each city, the data points gathered are each put into their own list. 

<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Perform_API_Calls_2.jpg">
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Perform_API_Calls_3.jpg">

These lists are combined into one DataFrame, which is utilized to create scatter plots that will showcase the relationships we want to emphasize.

Scatter charts are created using Matplotlib.


## Latitude vs Temperature Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Temp.jpg">
Chart shows that cities closer to the equator and 20 degrees N of the equator experience higher average temperatures. This can be explained by the tilt of the Earth's axis in relation to the Sun.  

## Latitude vs Humidity Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Humidity.jpg">
There are more cities where higher humidity occurs the further ones travels North of the Equator.

## Latitude vs Cloudiness Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Cloudiness.jpg">
No clear correlation can be found between these two factors.

## Latitude vs Wind Speed Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Wind_Speed.jpg">
No clear correlation can be found between these two factors.



# Second API Call and Scatter Plot Analysis

<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Perform_API_Calls_20200626_1.jpg">

The same code is used to initiate another API call to the site and gather the relevant information for the new list of cities.

<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Perform_API_Calls_20200626_2.jpg">

All the data from the second API call is stored into a new dataframe, "weather_df_2", which will be utilized to create new scattter plots.


## Latitude vs Temperature Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/code/LatitudeVsTemperature_2.png">
This chart shows that the trend of higher temperatures for cities between the Equator and 20 degrees N is consistent even when a second list of randomly selected cities is charted. The upsidw-down "V" curve shows up in both plots.

## Latitude vs Humidity Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/code/LatitudeVsHumidity_2.png">
The second list of cities also shows a higher frequenqy of cities that experience humidity North of the Equator.

## Latitude vs Cloudiness Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/code/LatitudeVsCloudiness_2.png">
No clear correlation can be found between these two factors from the first plot to the second plot. Cloudiness does not seem to depend on location.

## Latitude vs Wind Speed Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/code/LatitudeVsWindSpeed_2.png">
No clear correlation can be found between these two factors. Average wind speed across all cities seems to stay between 0 and 5 MPH.