# PUT /users/#{id}/socialMedia/{service}    
***
`/users/#{id}/socialMedia/{service}`

### Description
***
Only available for the authenticated user, this call disconnects a service.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to retrieve information from|integer|x||
|**service**|the service name|string|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**photolike**|whether to share photo likes on facebook|boolean|||
|**photocomment**|whether to share photo comments on facebook|boolean|||
|**albumlike**|whether to share album likes on facebook|boolean|||
|**userfollow**| whether to share user follows on facebook|boolean|||
|**timelinepopup**|a flag for us to track which users have been notified about facebook timeline|boolean|||



### Response
***


200 and confirmation message



[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/socialMedia/facebook`


