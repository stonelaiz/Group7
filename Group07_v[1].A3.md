# The Weather API 

## API description
The Weather API(Application Programming Interface) allows consumers to inquire on how to approach their day by providing a quick weather report of the precipitation and temperature based on the coordinates of Manitoba. The Weather API, takes four inputs, longitude(long), latitude(lat), time, and length(optional), and returns weather information for the region specified as well as an option to request hourly reports. So whether the customer is a farmer or a daily commuter they will be able to make favourable decisions based on the report provided.

## Endpoints

### GET /manitobaweather/report
Gets an hourly report for a specified coordinate pair.

parameters:
 | paramater | data-type | optional? | description |
 | --- | --- | --- | --- |
 | long | float | mandatory | the longitude of location to get a weather report for. Values must be within Manitoba
 | lat | float | mandatory | the latitude of location to get a weather report for. Values must be within Manitoba
 | time  |  integer | optional | how many hours from the request will be the beginning of the report. value range 0-24. By default 0, which reports the current hour
  leng | integer | optional | how many hours the report should cover. value range 1 - 24. By default 1 hour will be returned.

## Resources
```
{  
   "precipitation": the probability of snow/rain in the area
   "temperature": the current temperature in the area
   "region": is the given by the coordinates provided which must be within Manitoba
   "time": the times provided by the API depending on the parameter; 1-24 hours from the current time
}
```

## Sample Request/Response
### Request
```
https://api.manitoba.weather.org/json/weather?long=27.2&lat=77.1&time=0&leng=3
```
### Response
```
{
   "results":
   {
   "time": 18:00
        "precipitation": 60%
        "temperature": -21
   "time": 19:00
        "precipitation": 10%
        "temperature": -17
   "time": 20:00
        "precipitation": 0%
        "temperature": -15
   "time": 21:00
        "precipitation": 50%
        "temperature": -24
   }
   "status": "OK"
}
```
### Request
```
https://api.manitoba.weather.org/json/weather?long=27.2&lat=77.1
```
### Response
```
{
   "results":
   {
   "time": 18:00
        "precipitation": 60%
        "temperature": -21
   }
   "status": "OK"
}
```





