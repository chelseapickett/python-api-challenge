# python-api-challenge
Module 6 Challenge

There are two parts to this challenge. The first part is called WeatherPy and the second is called VacationPy. 
In the WeatherPy notebook, the Openweather API is called to create a list of cities with the following data associated with each city: 
- Latitude
- Longitude
- Max Temperature
- Humidity
- Cloudiness
- Wind Speed 
- Country
- Date

The resulting dataframe was saved as a csv file and can be found in the [output_data](https://github.com/chelseapickett/python-api-challenge/tree/main/WeatherPy/output_data) folder. 
Using this dataframe several scatter plots were created to showcase the following relationships and each image was also saved to the [output_data](https://github.com/chelseapickett/python-api-challenge/tree/main/WeatherPy/output_data) folder:

- Latitude vs. Temperature ![image](https://user-images.githubusercontent.com/120599626/229192262-33ee68f7-44f3-486d-a185-c0ff93ce25ca.png)

- Latitude vs. Humidity![image](https://user-images.githubusercontent.com/120599626/229192322-c2c65aa4-7711-4bce-b147-3b706cd996cd.png)

- Latitude vs. Cloudiness ![image](https://user-images.githubusercontent.com/120599626/229192383-496ed9d7-a7bf-44bf-b1cb-cb21750faf21.png)   
 
- Latitude vs. Wind Speed ![image](https://user-images.githubusercontent.com/120599626/229192443-bc736880-a16e-42a0-a1d1-fff91ccf06c9.png)
 
Lastly, linear regression was also calculated for the same relationships while separating the northern and southern hemisphere for each relationship. A summary statement follows each scattter plot pair for northern/southern hemisphere and featured data column. The following scatter plot(s) highlight the most correlated relationship found, latitude and max temperature:

Northern Hemisphere: 
![image](https://user-images.githubusercontent.com/120599626/229193336-4de4ae21-3c89-4813-8dc1-898d11f63c12.png)

Southern Hemisphere: 
![image](https://user-images.githubusercontent.com/120599626/229193403-4940808c-013d-4068-8c3a-2db2f7e96bf1.png)

In the VacationPy notebook, the Geoapigy API is called to create a map that displays all cities in the same dataframe used in WeatherPy, highlighting the humidity for each city. Then ideal weather conditions were selected to create an ideal vacation destination based on weather conditions and the other column parameters available in the dataframe. For this exercise the ideal conditions selected were : 

- A Max Tempe between 20 and 30 degrees Celsius 
- Zero cloudiness
- Not in the US

A new dataframe (hotel_df) was created to include only the City,	Country,	Latitude,	Longitude,	Humidity and	Hotel Name. After this, a for loop was creted to access the geoapify API and locate the first hotel within 10,000 meters of the cities in the dataframe. The results were plotted on a geomap that showcases the dataframe information when you hover over each plot point. 
![image](https://user-images.githubusercontent.com/120599626/229193524-afedc21f-707d-470a-88b4-3194ab96e471.png)

The constraints selected for ideal weather conditions resulted in only one option for a hotel that was 10,000 meters away from a city with ideal weather conditions and that was the Grand Lion Hotel in Riyadh, Saudi Arabia. 
