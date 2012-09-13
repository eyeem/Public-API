# PUT /albums/#{id}/likers/#{user_id} 
***
`/albums/#{id}/likers/#{user_id}`

### Description
***
Like an album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if success



[Errors][]

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/likers/me`








[Errors]: 