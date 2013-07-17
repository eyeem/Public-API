# GET /photos
***
`/photos`

### Description
***
Retrieves the authenticated user's latest twenty photos or popular photos (collection).

the params type,date,frame/filter,ids are processed in that order. the first match is the source of the response.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**type**|"popular" returns popular photos|string|||
|**date**|returns photos taken on a specific date (YYYY-MM-DD)|date||0|
|**interval**|num of days before "date" to look for|integer||1|
|**frame**|returns photos taken using a particular frame |string||0|
|**filter**|returns photos taken using a particular filter |string||0|
|**ids**| comma-separated list of ids to return (if type not specified)|csv int|||
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|
|**detailed**| If true, allows for inline embedding of detailed objects|boolean||0|
|**includeComments**| If true, returns the latest two comments of a photo inline|boolean||0|
|**numComments**| number of comments to return inline|integer||2|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean| |0|
|**numLikers**| number of likers to return inline|integer||1|
|**includePeople**|If true, returns the tagged people inline|boolean||0|
|**numPeople**| number of tagged people to return inline|integer||10|
|**includeAlbums**|If true, returns the albums inline|boolean||0|
|**userDetails**|If true, returns the detailed user profile of photo owner|boolean| |0|


### Response
***

200 and an array of photos.
