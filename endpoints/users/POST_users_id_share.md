# POST /users/#{id}/share
***
`/useres/#{id}/share`

### Description
***
Share a user to the user's connected social media services.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**services**|comma-separated list of services (twitter,facebook,tumblr)|string|x||
|**message**|user-entered message to be shared with the user|string|||


### Response
***

200 if success

[Errors][]

### Examples
***

`http://www.eyeem.com/api/v2/users/1234/share`







[Errors]: 