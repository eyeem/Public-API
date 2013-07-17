# DELETE /albums/#{id}/likers/#{user_id} 
***
`/albums/#{id}/likers/#{user_id}`

### Description
***
Unlike an album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/albums/1234/likers/1013`






 