# GET /users/#{id}/friendsPhotos 
***
`/users/#{id}/friendsPhotos`

### Description
***
Get all the photos by users that the given user follows (ordered chronologically).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of photo objects


[Errors](../../resources/errors.md#files)
### Examples
***

`https://www.eyeem.com/api/v2/users/1013/friendsPhotos`


