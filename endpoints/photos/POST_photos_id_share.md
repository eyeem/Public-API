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
|**upload**|The reason for flagging the photo (Pornographic, Terms of Service, Copyright).|string||0|

### Response
***


200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/photos/1234/share?services=facebook`



