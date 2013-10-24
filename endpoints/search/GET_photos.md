# GET /search/photos   
***
`/search/photos`

### Description
***
Retrieves an array containing photos

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|the keyword to search|string|x||
|**limit**|num of items to return|integer||10|
|**offset**|(offset of items to start at|integer||0|

|**user_id**|get photos by a particular user|int|||
|**album_id**|get photos in a particular album|int|||
|**grayscale**|get only black and white photos|boolean|||
|**filter**|name of the (EyeEm) filter to filter by|string|||
|**frame**|name of the (EyeEm) frame to filter by|string|||
|**format**|filter photos by a specific format (portrait, landscape, square, panorama)|string|||
|**size**|filter photos by size (xl, l, m, s)|string||
|**topic**|search for photos with a specific topic in description|string||
|**color**|filter by a specific color [H-S-L]|string||
|**venue_name**|get only photos taken at a specific venue|string|||
|**city_name**|get only photos taken in a specific city|string|||
|**country_name**|get only photos taken in a specific country|string|||
|**venue_type**|get only photos taken at a specific type of venue (name)|string|||
|**venue_type_id**|get only photos taken at a specific type of venue (id)|string||
|**latitude**|filter by proximity to a geopoint (requires longitude)|float||
|**longitude**|filter by proximity to a geopoint (requires latitude)|float||||
|**before**|photos taken before a date (ex: 01-Feb-2012)|date|||
|**after**|photos taken after a date (ex: 01-Feb-2012)|date|||
|**before_hour**|photos taken before a specific time (0-24)|int|||
|**after_hour**|photos taken after a specific time (0-24)|int|||
|**weather**|filter by weather type (clear, cloudy, fog, rain, snow)|string|||
|**cam_make**|filter by manufacturer (ex: apple)|string|||
|**cam_model**|filter by device (ex: iphone 5c)|string|||
|**cam_software**|filter by exif cam software|string|||
|**sort**|sort order results (time, popularity, relevance)|string|||

|**detailed**| If true, allow inclusion of details|boolean||1|
|**includeComments**| If true, returns the latest two comments of a photo inline|boolean||1|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||1|
|**numComments**|the number of comments to include in the response|integer||2|
|**numLikers**|the number of likers to include in the response|integer||1|
|**includeAlbums**| If true, includes the albums this photo is part of|boolean||1|
|**userDetails**| If true, includes the detailed profile of the photo's owner|boolean||0|
|**includePeople**|If true, returns the people tagged in this photo photo|boolean||1|
|**numPeople**|the number of tagged people to include in the response|integer||10|
|**simpleDescription**|If true, returns a simple, human-readable photo description|boolean||0|

### Response
***

200 and an array containing photos