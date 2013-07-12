# DELETE /albums/#{id}/photos/#{photo_id} 
***
`/albums/#{id}/photos/#{photo_id} `

### Description
***
Remove an existing photo from an album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album|integer|x||
|**photo_id**| the id of the photo|integer|x||

### Response
***


200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`http://api.eyeem.com/v2/albums/1234/photos/11234134`






 