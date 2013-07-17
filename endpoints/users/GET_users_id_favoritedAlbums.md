# GET /users/#{id}/favoritedAlbums  
***
`/users/#{id}/favoritedAlbums`

### Description
***
Get all the albums that a user has favorited.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|
|**onlyId**| returns a json array photoIds containing just the ids|boolean||0|
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||0|
|**numPhotos**|the number of album photos to return|integer||7|
|**includeContributors**|if true, returns the album contributors|boolean| |0|
|**includeLikers**| if true, returns the album likers|boolean| |0|

### Response
***

200 and and a dictionary containing limit, offset, total and an array of album objects


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/1013/favoritedAlbums`