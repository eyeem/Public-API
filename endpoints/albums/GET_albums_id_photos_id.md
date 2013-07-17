# GET /albums/#{id}/photos/#{photo_id} 
***
`/albums/#{id}/photos/#{photo_id}`

### Description
***
Checks whether a photo is in a particular album

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if in, 400 if not.