# POST /venues    
***
`/venues`

### Description
***
Create a venue on EyeEm.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**service**|the name of the service this venue is retrieved from (for now: foursquare)|string|x||
|**id**| the id of the venue on the external service|integer|x||
|**name**|the name of the venue|string|x||
|**location**|key/value array of various location related info (lat,lng,city,country, etc...)y|array|x||

### Response
***


201


[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/venues?service=foursquare&id=4adcda7af964a5201a4721e3&location[city]=Berlin&location[country]=Germany`






