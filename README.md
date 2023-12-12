# Solar-Power-Generation-Forecast
**Introduction**

Solar power production and consumption in India have witnessed remarkable growth and transformation in recent years. With a total solar power generation capacity exceeding 35 gigawatts (GW) as of September 2020, India ranks among the world's largest solar power producers. Government initiatives, incentives, and large-scale solar parks have fueled this capacity expansion. India's commitment to solar energy aligns with its sustainable development goals, providing electricity to remote areas and reducing costs for industries. India had numerous solar power plants and installations across the country, with a wide range of capacities and sizes. India's abundant sunshine, low cloud cover, and diverse geography create favorable conditions for solar production year-round. Motivated by this, we have gathered data from a solar power facility located in near Mumbai, India, to conduct an in-depth analysis of solar production based on the weather conditions.

**Problem Statement**

The objective of this project is to develop an accurate and reliable time series forecasting model for the solar power generation of a solar plant, specifically focusing on the daily power generation. This forecasting model will utilize historical solar power generation data in conjunction with concurrent weather sensor data, including ambient temperature, module temperature, and irradiation. In this project, through the forecasting, we will try to forecast the power generated, analyze components such as trend, seasonality and cycles of occurrence and the occurrence in different times of the week, using models like exponential smoothing, and, ARIMAX. We aim to test the cross correlation and causation of various weather factors on solar power generation.


**Dataset Description**

The dataset contains information related to approximately 1 month performance and output of a solar power plant captured over 15-minute intervals, including various attributes such as date and time stamps, weather conditions, power generation readings, and possibly other relevant data points. Analyzing this dataset can help users gain insights into the efficiency and reliability of solar power generation under different weather conditions and times of the day.

**Data Exploration**

To perform detailed exploration and forecasting of the data, we first analyzed the raw dataset. 
We have extracted the base data from Kaggle, which contains the details about solar power generation from a plant located near Mumbai, India.
The overview of the same is in the snapshot and description below:

**Plant_2_Generation_Data.csv:**

This dataset contains the solar power generation data for one plant gathered at 15 minutes intervals over a 34 days period, and has the following variables:
DATE_TIME : Date and time for each observation. Observations recorded at 15 minute intervals.
PLANT_ID : Plant ID - this will be common for the entire file.
SOURCE_KEY : Source key in this file stands for the inverter id.
DC_POWER : Amount of DC power generated by the inverter (source_key) in this 15 minute interval. Units - kW.
AC_POWER : Amount of AC power generated by the inverter (source_key) in this 15 minute interval. Units - kW.
DAILY_YIELD : Daily yield is a cumulative sum of power generated on that day, till that point in time.
TOTAL_YIELD : This is the total yield for the inverter till that point in time.


**Plant_2_Weather_Sensor_Data.csv**

This dataset contains the weather sensor data gathered for one solar plant every 15 minutes over a 34-day period, and has the following column variables:
DATE_TIME: Date and time for each observation. Observations recorded at 15-minute intervals.
PLANT_ID: Plant ID - this will be common for the entire file.
SOURCE_KEY: Stands for the sensor panel id. This will be common for the entire file because there's only one sensor panel for the plant.
AMBIENT_TEMPERATURE: This is the ambient temperature at the plant.
MODULE_TEMPERATURE: There's a module (solar panel) attached to the sensor panel. This is the temperature reading for that module.
IRRADIATION: Amount of irradiation for the 15-minute interval.


**Mumbai_temp.csv**
This dataset is a timeseries dataset that we as a team generated to be able to forecast the solar power generation more accurately. We extracted the weather conditions from the daily weather reports at Mumbai over the same period of time to help us with the same. The dataset contains the following variable columns :
Temperature : temperature measure in Fahrenheit 
Dew Point : dewpoint measure in Fahrenheit
Humidity : the percent humidity at that point in time
Wind : direction of wind – categorical variable
Wind Speed : the wind speed in mph
Wind Gust : the measure of wind gust in mph
Pressure : the measure of mercury rise in inches while calculating the pressure
Precip. : the measure of precipitation in inches
Condition : the condition definition of that area – which is a categorical variable
DateTime : Date time stamp of when the measurement was taken- data available for every 30 minutes 




