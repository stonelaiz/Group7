# Group7
## Weather API based on location
This is the best group

## API description
The Weather API has 1 endpoint with 3 parameters. The three parameters, longitude, latitude, and number of hours, indicate the location to collect the report from as well as how many hourly updates the user requests. (the assignment says the description should pitch it to a manager or something. not sure if you care to update it, but that is what the assignment says) Note from nick 

## Endpoints

### GET /manitobaweather/report
Gets an hourly report for a specified coordinate pair.

parameters:
 | paramater | data-type | optional? | description |
 | --- | --- | --- | --- |
 | long | number | mandatory | the longitude of location to get a weather report for. Values must be within Manitoba
 | lat | number | mandatory | the latitude of location to get a weather report for. Values must be within Manitoba
 | time  |  number | optional | how many hours from the request will be the beginning of the report. value range 0-24. By default 0, which repurts the current hour
  leng | number | optional | how many hours the report should cover. value range 1 - 24. By default 1 hour will be returned.

## Resources
{  
   "precipitation": the probability of snow/rain in the area
   "temperature": the current temperature in the area
   "region": is the given by the coordinates provided which must be within Manitoba
   "time": the times provided by the API depending on the parameter; 1-24 hours from the current time
}

## Sample Request/Response
###Request
```

https://api.manitoba.weather.org/json/weather?long=27.2&lat=77.1&time=0&leng=3
```
###Response
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
###Request
```

https://api.manitoba.weather.org/json/weather?long=27.2&lat=77.1
```
###Response
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





