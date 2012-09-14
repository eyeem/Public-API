# GET /albums/#{id}/contributors 
***
`/albums/#{id}/contributors`

### Description
***
Retrieves an array of the users who have added photos to the album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of contributors to return|integer||20|
|**offset**|offset of contributors to start at|integer||0|
|**onlyId**|if true, returns only the user id|boolean||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of contributors (users)


[Errors](../../resources/errors.md#files)
### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/contributors?offset=0&limit=5`




 