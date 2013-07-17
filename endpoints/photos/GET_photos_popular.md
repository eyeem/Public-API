# GET /photos/popular
***
`/photos/popular`

### Description
***
Return a collection of the current popular photos.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
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
|**userDetails**|If true, returns the detailed user profile of the photo owners|boolean||0|


### Response
***

200 and an array of photos.
