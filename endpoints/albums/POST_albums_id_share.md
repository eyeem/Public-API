# POST /albums/#{id}/share 
***
`/albums/#{id}/share`

### Description
***
Share an album to an external Social service.


### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album to share|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**services**|comma-separated list of services (twitter,facebook,tumblr)|string|x||
|**message**|user-entered message to be shared with the photo.|string|||


### Response
***
200 if success