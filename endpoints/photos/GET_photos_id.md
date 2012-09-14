# GET /photos/#{id} 
***
`/photos/#{id}`

### Description
***
Retrieves a photo by id.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want to retrieve information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**includeComments**| If true, returns the latest two comments of a photo inline|boolean||0|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||0|
|**numComments**|the number of comments to include in the response|integer||2|
|**numLikers**|the number of likers to include in the response|integer||2|
|**includeAlbums**| If true, includes the albums this photo is part of|boolean||0|

### Response
***


200 and an a photo dictionary

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234?detailed=1&includeAlbums=1&includeComments=1&numComment=5`
