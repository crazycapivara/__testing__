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
#### openweathermapy.core.get_current_for_group
```Python
def get_current_for_group(city_ids, **params)
```
Get current weather data for multiple cities.
