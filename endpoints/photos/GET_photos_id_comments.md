# GET /photos/#{id}/comments  
***
`/photos/#{id}/comments`

### Description
***
Retrieves an array of a photo's comments.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of comments to return|integer||20|
|**offset**|offset of comments to start at|integer||0|
|**onlyId**|if true, returns a comma separated list of comment ids|boolean||0|

### Response
***


200 and and a dictionary containing limit, offset, total and an array of comments

[Errors](../../resources/errors.md#files)
### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/comments?offset=0&limit=5`




 