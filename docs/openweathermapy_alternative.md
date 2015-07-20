# Getting started
# API
## Functions
### get_current
```Python
def get_current(city=None, **params)
```

**Description**
```Python
"""Get current weather data for city.

Args:
   city (str, int or tuple): name, id
      or geographic coordinates (latidude, longitude)
   **params: units, lang[, zip, ...]
   
Return:
   openweathermpay.utils.NestedDict
"""  
```

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
### get_current_for_group
```Python
def get_current_for_group(city_ids=None, **params)
```

**Description**
```
Get current weather data for multiple cities.
	
Args:
   city_ids (tuple): list of city ids,
   **params: units, lang
   
Return:
   openweathermapy.core.DataBlock
```

**Examples**
```Python
# get data for 'Malaga,ES', 'Kassel,DE', 'New York,US'
>>> city_ids = (2892518, 2514256, 5128581)
>>> data = get_current_for_group(city_ids, units="metric")
```

---
