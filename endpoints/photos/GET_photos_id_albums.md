# GET /photos/#{id}/albums  
***
`/photos/#{id}/albums`

### Description
***
Retrieves an array of a photo's albums.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of comments to return|integer||20|
|**offset**|offset of comments to start at|integer||0|
|**onlyId**|if true, returns a comma separated list of comment ids|boolean||0|
|**detailed**|If true, allows for album details to be included|boolean||0|
|**includePhotos**|If true, adds photo array inline|boolean||0|
|**includeContributors**|If true, adds album contributor array inline|boolean||0|
|**includeLikers**|If true, adds album favoriters array inline|boolean||1|

### Response
***


200 and and a dictionary containing limit, offset, total and an array of albums

[Errors](../../resources/errors.md#files)