# GET /albums/#{id}/likers/#{user_id} 
***
`/albums/#{id}/likers/#{user_id}`

### Description
***
Checks whether a user likes an album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if the user likes the album, 404 otherwise



[Errors][]

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/likers?offset=0&limit=5`








[Errors]: 