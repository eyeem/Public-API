# POST /users/#{id}/share
***
`/users/#{id}/share`

### Description
***
Share a user to the user's connected social media services.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the id of the user to share|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**services**|comma-separated list of services (twitter,facebook,tumblr)|string|x||
|**message**|user-entered message to be shared with the user|string|||


### Response
***

200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/1234/share`




