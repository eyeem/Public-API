# POST | PATCH | PUT /users/#{id}
***
`/useres/#{id}`

### Description
***
Edit (parts of) a user's own profile. only updates whichever params are actually provided in the request.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**fullname**|representing the user's full name|string|||
|**nickname**|representing the user's nickname|string|||
|**email**|the user's email address|string|||
|**password**|the user's new password|string|min. 6 characters||
|**description**|brief text description of a user|string|max 150 chars||
|**photo**|a user's profile photo|file|||



### Response
***
200 and a user object 