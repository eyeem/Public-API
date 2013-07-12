# POST /users/#{id} 
***
`/useres/#{id}`

### Description
***
Edit (parts of) a user's own profile.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**fullname**|representing the user's full name|string|||
|**nickname**|representing the user's nickname|string|||
|**username**|the user's email address|string|||
|**password**|the user's new password|string|min. 6 characters||
|**description**|brief text description of a user|string|||
|**emailNotifications**|decides whether the user wants to receive email notifications|boolean|||
|**pushNotifications**|decides whether the user wants to receive push notifications|boolean|||
|**photo**|a user's profile photo|file|||
|**facebookTimeline**|this basically sets all the facebook activity stuff to true|boolean|||



### Response
***
200 and a user object 


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/1013?nickname=ramz`




