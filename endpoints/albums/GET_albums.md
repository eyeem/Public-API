# GET /albums
***
`/albums`

### Description
***
Retrieves albums specified in the id URL query parameter, or searches for albums based on their names.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|a comma-separated list of album ids to retrieve|string|||
|**q**|search albums by (renders the ids parameter invalid)|string|||
|**trending**|returns 30 new and growing topical albums|boolean|||
|**geoSearch**|"city" or "nearbyVenues" or "foursquareVenue"|string|||
|**lat**|latitude|integer| for "city" and "nearbyVenues" geoSearch||
|**lng**|longitude|integer| for "city" and "nearbyVenues" geoSearch||
|**foursquareId**||string|for "foursquareVenue" geoSearch||
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|
|**minPhotos**|return albums only with at least the specified number of photos (works when "q" is specified)|integer|||
|**type**|only returns albums of a specific type (city,country,event,venue,tag) (works when "q" is specified)|string|||


### Response
***
200 and an array of album objects, optionally (for search) includes pagination parameters

[Errors](../../resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/albums?ids=35,123,3352,3563`

`http://www.eyeem.com/api/v2/albums?q=berlin&limit=25&offset=20`

 