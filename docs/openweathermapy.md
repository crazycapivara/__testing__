# Getting started
# API
## Functions
#### openweathermapy.core.get_current
```Python
def get_current(city=None, **params)
```
Get current weather data for city.

**Parameters**
```
city (str, int or tuple):
  name, id or geographic coordinates
  
**params:
  units, lang ..., see OWM API for details
```
***

#### openweathermapy.core.get_current_for_group
```Python
def get_current_for_group(city_ids, **params)
```
Get current weather data for multiple cities.

``city_ids (tuple)`` _ list of city ids,

``**params`` _ units, lang, ...

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
