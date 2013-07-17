# GET /albums/#{id}/relatedAlbums
***
`/albums/#{id|/relatedAlbums`

### Description
***
Retrieves albums related to the one specified in the id URL query parameter. useful for finding popular topics at specific venues, cities in a country, etc...

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**type**|only returns related albums of a specific type (city,country,event,venue,tag)|string|||
|**venueCategory**|search for venues that belong to a particular Foursquare venue category (requires type=venue)|string||0|
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|

### Response
***
200 and an array of album objects, optionally (for search) includes pagination parameters
