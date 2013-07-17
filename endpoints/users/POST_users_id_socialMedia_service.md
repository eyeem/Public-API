# POST /users/#{id}/socialMedia/{service}    
***
`/users/#{id}/socialMedia/{service}`

### Description
***
Only available for the authenticated user, this call adds a service to the user's connected services.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to retrieve information from|integer|x||
|**service**|the service name|string|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**keys**|to simply store the access_token/access_secret for a specific service|boolean|||
|**oauth_token**|the token provided by a service|integer|||
|**oauth_token_secret**|the secret provided by a service, applies for tumblr and twitter at the moment|integer|||
|**service_user_id**|the user's id on the chosen service, applies for facebook and twitter|integer||0|
|**service_screen_name**|the user's nickname on the chosen service, applies for twitter onlyt|string||0|
|**follow**|whether to follow EyeEm on twitter|boolean|||
|**callback**||boolean|||
|**connect**||boolean|||
|**expires**||facebook_token expiration date|||
|**photolike**|whether to share photo likes on facebook|boolean|||
|**photocomment**|whether to share photo comments on facebook|boolean|||
|**albumlike**|whether to share album likes on facebook|boolean|||
|**userfollow**| whether to share user follows on facebook|boolean|||
|**timelinepopup**|a flag for us to track which users have been notified about facebook timeline|boolean|||




### Response
***


200 and an array of services objects


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/socialMedia/twitter`


