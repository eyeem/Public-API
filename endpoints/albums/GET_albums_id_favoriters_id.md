# GET /albums/#{id}/favoriters/#{user_id} 
***
`/albums/#{id}/favoriters/#{user_id}`

### Description
***
Checks whether a user favorited an album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if the user favorited the album, 404 otherwise