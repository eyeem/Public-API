# GET /albums/#{id}/photos
***
`/albums/#{id}/photos`

### Description
***
Retrieves photos of an album specified in the id URL query parameter.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of photos to return|integer||20|
|**offset**|(offset of photos to start at|integer||0|
|**onlyId**|if true, returns only the photo ids|boolean||0|
|**detailed**|returns a simple or detailed photo object|boolean||0|
|**includeComments**|If true, returns the latest two comments of a photo inline|boolean||0|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||0|
|**numComments**|the number of comments to include in the response|integer||2|
|**numLikers**|the number of likers to include in the response|integer||2|
|**includeAlbums**|If true, includes the albums this photo is part of|boolean||0|



### Response
***


200 and and a dictionary containing limit, offset, total and an array of photos


[Errors](../../resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/photos?offset=0&limit=5`






 