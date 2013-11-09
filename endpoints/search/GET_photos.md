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
