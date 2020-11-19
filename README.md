# Group7
## Weather API based on location
This is the best group

## API description
The Weather API has 1 endpoint with 3 parameters. The three parameters, longitude, latitude, and number of hours, indicate the location to collect the report from as well as how many hourly updates the user requests.

## Endpoints

### GET /manitobaweather/report
Gets an hourly report for a specified coordinate pair.

parameters:
 | paramater | data-type | optional? | description |
 | --- | --- | --- | --- |
 | long | number | mandatory | the longitude of location to get a weather report for. Values must be within Manitoba
 | lat | number | manadtory | the latitude of location to get a weather report for. Values must be within Manitoba
 | time  |  number | optional | how many hours from the request will be the beginning of the report. value range 0-24. By default 0, which repurts the current hour
  leng | number | optional | how many hours the report should cover. value range 1 - 24. By default 1 hour will be returned.

## Resources

## Sample Request
