# Getting started
# API
## Functions
#### get_current
```Python
def get_current(city=None, **params)
```
Get current weather data for city.

* ``city (str, int or tuple):`` name, id or geographic coordinates
* ``**params:`` units, lang[, zip, q ...], see OWM API for details

**Examples**
```Python
# get data by city name and country code
>>> data = get_current("Kassel,DE")
	
# get data by city id and set language to german (de)
>>> data = get_current(2892518, lang="DE")
	
# get data by latitude and longitude and return temperatures in Celcius
>>> location = (51.32, 9.5)
>>> data = get_current(location, units="metric")
	
# optional: skip city argument and get data by zip code
>>> data = get_current(zip="34128,DE") 
```

---
#### get_current_for_group
```Python  
def get_current_for_group(city_ids, **params)
```
Get current weather data for multiple cities.

* ``city_ids (tuple):``  list of city ids
* ``**params:`` units, lang

***
#### find_city
```Python
def find_city(city, **params)
```
Search for city (name) and return current weather data for match(es).

**Examples**   
```Python   
>>> data = find_city("New York")
>>> data = find_city("Malaga,ES")
```
