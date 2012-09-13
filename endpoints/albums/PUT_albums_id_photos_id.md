../../# PUT /albums/#{id}/photos/#{photo_id} 
***
`/albums/#{id}/photos/#{photo_id} `

### Description
***
Add an existing photo to an album.

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**photo_id**| The id of the photo|integer|x||

### Response
***


200 if success

[Errors](../../resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/photos/11234134`


 