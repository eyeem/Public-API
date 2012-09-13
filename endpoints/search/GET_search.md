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
|**includeAlbums**| whether to include results in the albums dictionary|boolean|x||
|**includeUsers**|whether to include results in the users dictionary|boolean|x||

### Response
***


200 and an array containing a users dictionary and an albums dictionary.


[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/search?q=berlin&includeAlbums=1`

