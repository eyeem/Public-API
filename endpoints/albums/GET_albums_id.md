../../# GET /albums/#{id}
***
`/albums/#{id}`

### Description
***
Retrieves album specified in the id URL query parameter.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||0|
|**numPhotos**|the number of album photos to return|integer||10|
|**photoDetails**|whether to return the photo details (comments, likes, albums)|boolean||0|
|**includeContributors**|if true, returns the album contributors|boolean| |0|
|**includeLikers**| if true, returns the album likers|boolean| |0|




### Response
***


200 and a dictionary containing the album object


[Errors](../../resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234?`



 