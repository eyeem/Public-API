# POST /photos/#{id}/share       
***
`/photos/#{id}/share`

### Description
***
Share a photo to the user's connected social media services.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo to flag.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**services**|comma-separated list of services (twitter,facebook,tumblr,flickr,foursquare)|string|x||
|**message**|user-entered message to be shared with the photo.|string|||
|**upload**|whether it's a new upload or an existing photo to share|boolean||0|

### Response
***


200 if success

[Errors](../../resources/errors.md#files)