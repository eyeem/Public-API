# POST | PATCH | PUT /users/#{id}
***
`/useres/#{id}`

### Description
***
Create a new account (email/pass). Only possible with a **native** scope.

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
|**description**|brief text description of a user|string|||
|**photo**|a user's profile photo|file|||



### Response
***
200 and a user object 