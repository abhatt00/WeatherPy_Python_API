## WeatherPy

Utilizes the OpenWeatherMap API and the citipy library to accomplish the objective.

Your objective is to build a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude


# Analysis

1st Observation: The only discernable trend occurs in the Latitude v Temp plot, where it shows that the closer a city is to 20 degrees N of the Equator, the higher the Maximum temperature is for that city. This is shown by the upside-down "V" shape in the scatter plot. 


2nd Oberservation: Although the Latitude v Humidity plot does not show a very strong trend, there is cause to argue that there is a higher frequency of cities that experience humidity the farther North of the Equator a city is. A good way to make a comparison is measuring humidity of the cities in question during different seasons.


3rd Observation: It seems that regardless of Latitude, cities are more likely to experience average wind speeds between 0 and 4 MPH.


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
Chart shows that cities closer to the equator and 20 degrees N of the equator experience higher humidity. This can be explained by the tilt of the Earth's axis in relation to the Sun.  

## Latitude vs Humidity Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Humidity.jpg">

## Latitude vs Cloudiness Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Cloudiness.jpg">

## Latitude vs Wind Speed Plot
<img width=“500” alt=“” src="https://github.com/abhatt00/WeatherPy_Python_API/blob/master/Images/Latitude_v_Wind_Speed.jpg">
