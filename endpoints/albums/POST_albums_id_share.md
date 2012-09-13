# POST /albums/#{id}/share 
***
`/albums/#{id}/share`

### Description
***
Share an album to the user's connected social media services.


### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**services**| comma-separated list of services (twitter,facebook,tumblr)|string|x||
|**message**|user-entered message to be shared with the album|string|||


### Response
***
200 if success

[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/share`



 