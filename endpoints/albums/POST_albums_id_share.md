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
|**id**| the id of the album to share|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**services**| comma-separated list of services (twitter,facebook,tumblr)|string|x||
|**message**|user-entered message to be shared with the album|string|||


### Response
***
200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/albums/1234/share`



 