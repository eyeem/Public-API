# GET /albums/#{id}/contributors/#{user_id} 
***
`/albums/#{id}/contributors/#{user_id}`

### Description
***
Checks whether a user has contributed a photo to the album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if the user has contributed a photo to the album, 404 otherwise


[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/contributors/1013`



 