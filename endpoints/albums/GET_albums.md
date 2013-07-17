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
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||1|
|**numPhotos**|the number of album photos to return|integer||10|
|**includeContributors**|if true, returns the album contributors|boolean| |0|
|**includeLikers**| if true, returns the album likers|boolean| |0|
|**offset**|offset of search results to start at|integer||0|
|**limit**|num of search results to return|integer||30|
|**q**|search albums by (renders the ids parameter invalid)|string|||
|**minPhotos**|return albums only with at least the specified number of photos (works when "q" is specified)|integer|||
|**type**|only returns albums of a specific type (city,country,event,venue,tag) (works when "q" is specified, or top=1)|string|||
|**top**|used in combination w/ the type parameter to return the most popular cities, countries, etc... |boolean||0|
|**geoSearch**|"city" or "nearbyVenues" or "foursquareVenue"|string|||
|**lat**|latitude|integer| for "city" and "nearbyVenues" geoSearch||
|**lng**|longitude|integer| for "city" and "nearbyVenues" geoSearch||
|**foursquareId**||string|for "foursquareVenue" geoSearch||
|**venueCategory**|search for venues that belong to a particular Foursquare venue category|string||0|
|**trending**|returns 30 new and growing topical albums|boolean||0|
|**ids**|a comma-separated list of album ids to retrieve|int csv|||

### Response
***
200 and an array of album objects, optionally (for search) includes pagination parameters
