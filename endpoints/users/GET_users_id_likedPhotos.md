# GET /users/#{id}/likedPhotos  
***
`/users/#{id}/likedPhotos`

### Description
***
Get all the photos that a user has liked.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|
|**onlyId**| returns a json array photoIds containing just the ids|boolean||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of photo objects


[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013/likedPhotos`



