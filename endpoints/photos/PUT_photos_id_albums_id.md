# PUT /photos/#{id}/albums/#{album_id}     
***
`/photos/#{id}/albums/#{album_id}`

### Description
***
Add an existing photo to an album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want retrieve information about.|integer|x||
|**album_id**|The id of the album to interact with.|integer|x||


### Response
***


200 if success

[Errors][]

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/albums/11234134`







[Errors]: 