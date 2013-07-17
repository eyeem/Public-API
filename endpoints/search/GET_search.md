# GET /search    
***
`/search`

### Description
***
Retrieves an array containing a users and an albums dictionary.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|the keyword to search|string|x||
|**includeAlbums**| whether to include results in the albums dictionary|boolean||0|
|**includeUsers**|whether to include results in the users dictionary|boolean||0|
|**limit**|num of items to return|integer||10|
|**offset**|(offset of items to start at|integer||0|

### Response
***

200 and an array containing a users dictionary and an albums dictionary.