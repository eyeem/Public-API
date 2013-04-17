# GET /albums/#{id}/likers 
***
`/albums/#{id}/likers`

### Description
***
Retrieves an array of the users who like the album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of likers to return|integer||20|
|**offset**|offset of likers to start at|integer||0|



### Response
***

200 and and a dictionary containing limit, offset, total and an array of likers (users)

[Errors](../../resources/errors.md#files)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/likers?offset=0&limit=5`







 