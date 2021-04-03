# World_Weather_Analysis
## Overview
PlanMyTrip is a top travel technology company that specializes in internet-related services in the hotel and lodging industry. The user interface team head, Jack asked us to help him collect temperature-based city data and present it to the customers during their search page to help plan their trip. By using data from citipy, OpenWeatherMap API, Google Maps and Places API, and Google Maps Directions API analysis has been performed in three stages:
- Retrieve weather data
- Create a customer travel destination map
- Create a travel itinerary map

## Summary
### Retrieve Weather Data
- By using Random and Uniform functions, 2000 sets of random latitudes and longitudes have been generated and stored as a list.
- By using the citipy function, 742 unique cities were found for the list of latitudes and longitudes.
- By using Open Weather Map API, the weather data was retrieved for 742 cities and stored in a dataframe as the below indexes:
1.	City
2.	Country
3.	Latitudes
4.	Longitudes
5.	Maximum Temperature
6.	Humidity
7.	Cloudiness
8.	Wind Speed
9.	Weather Description

![image](https://user-images.githubusercontent.com/76491891/113481383-45e35200-9467-11eb-8968-87deae515df4.png)

### Create a Customer Travel Destination Map
- A customer is prompted to enter the maximum and minimum temperatures for their trip.
- A new dataframe is created and stored with city weather data for the maximum and minimum temperatures provided by customers.
- By using Google Maps and Places API, hotels located within 5000 meters radius for each location are inserted in the dataframe as Hotel names.
- A map is then created using gmaps to show preferred locations for the customer. Each location is shown as a pop-up box containing the Hotel Name, City, Country, Weather Description, and Temperature.

<img width="960" alt="WeatherPy_vacation_map" src="https://user-images.githubusercontent.com/76491891/113481415-71fed300-9467-11eb-9f41-83528708a43f.png">

### Create a Travel Itinerary Map
- Using the vacation search map, four random cities (Kununurra, Carnarvon, Mount Isa, Mackay) were selected from the same country which the customer wants to visit. Directions to visit the four cities selected above are provided using the Google Maps Directions API.

<img width="960" alt="WeatherPy_travel_map" src="https://user-images.githubusercontent.com/76491891/113481438-922e9200-9467-11eb-9952-171705ec2b7c.png">

- By using Concat(), weather data for the four cities selected above are combined and stored in a new dataframe as shown below:

![image](https://user-images.githubusercontent.com/76491891/113481475-c3a75d80-9467-11eb-999a-0003c7a739ad.png)

- Using gmaps, a map is created to show the four preferred cities by the customer. A pop-up box containing Hotel Name, City, Country, Weather Description, and Temperature is displayed for each of the four cities.

<img width="960" alt="WeatherPy_travel_map_markers" src="https://user-images.githubusercontent.com/76491891/113481483-d883f100-9467-11eb-9890-a9417acf1200.png">
