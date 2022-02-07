# Weather Services

Call                                                      | Description
----------------------------------------------------------|---------------------------------
[CurrentWeatherData](#currentweatherdata)                 | Retrieve weather data for a given city,country.




## CurrentWeatherData

> Sample Data

```cli
{
  "city_or_city,country": "Toronto,CA",
  "unit_of_measurement": "metric"
}
```
Retrieve weather data for a given city,country.

**Note:** Use ISO 3166 alpha-2 country codes.

### Request Parameters

> Sample Request

```shell
curl -H "Accept: application/json" -H "Content-Type: application/json" -d '["Toronto,CAD","metric"]' https://api.maplenodes.com/v1/CurrentWeatherData
```

<code class="api-call">CurrentWeatherData [city_or_city,country] [unit_of_measurement]</code>

Parameter             | Type       | Description
----------------------|------------|-------------
city_or_city,country  | string     | City or City,Country.
unit_of_measurement   | string     | Data measurement in metric or imperial.


### Response Parameters

<aside class="success">
200 OK
</aside>

> Sample 200 Response

```shell
{
  "coord": {
    "lon": -79.42,
    "lat": 43.7
  },
  "weather": [
    {
      "id": 804,
      "main": "Clouds",
      "description": "overcast clouds",
      "icon": "04d"
    }
  ],
  "base": "stations",
  "main": {
    "temp": 7.51,
    "feels_like": 1.26,
    "temp_min": 6.67,
    "temp_max": 8.33,
    "pressure": 1015,
    "humidity": 61
  },
  "visibility": 14484,
  "wind": {
    "speed": 6.2,
    "deg": 310,
    "gust": 11.3
  },
  "clouds": {
    "all": 90
  },
  "dt": 1588606876,
  "sys": {
    "type": 1,
    "id": 941,
    "country": "CA",
    "sunrise": 1588586703,
    "sunset": 1588638220
  },
  "timezone": -14400,
  "id": 6167865,
  "name": "Toronto",
  "cod": 200
}
```

Parameter             | Type       | Description
----------------------|------------|-------------
coord                 | Object     | Coordinate data.
lon                   | string     | Longitude of the city.
lat                   | string     | Latitude of the city.
weather               | Object     | Weather data.
id                    | int        | Weather ID.
main                  | string     | Main description. 
description           | string     | Weather description.
icon                  | string     | Icon ID.
base                  | string     | Base data.
main                  | Object     | Main temperature data.
temp                  | int        | Temperature.
feels_like            | int        | Temperature including wind chill or humidex.
temp_min              | int        | Temperature low.
temp_max              | int        | Temperature high.
pressure              | int        | Pressure.
humidity              | int        | Humidity.
visibility            | int        | Visibility.
wind                  | Object     | Wind data.
speed                 | int        | Speed of the wind.
deg                   | int        | Degree of the wind.
clouds                | Object     | Cloud data.
all                   | int        | Clouds data.
dt                    | int        | dt.
sys                   | Object     | Sun data.
type                  | int        | Type.
id                    | int        | Sys ID.
country               | string     | Country of city.
sunrise               | int        | Timestamp of sunrise.
sunset                | int        | Timestamp of sunset.
timezone              | int        | Timezone of city.
id                    | int        | ID.
name                  | string     | City name.
cod                   | int        | Cod.
