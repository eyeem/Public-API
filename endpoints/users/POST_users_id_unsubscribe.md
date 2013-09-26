# POST /users/#{id}/unsubscribe     
***
`/users/#{id}/unsubscribe`

### Description
***
Allow users to modify email (and other) flags without logging in.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to edit|integer|x||
|**token**|the unique user token|string|x||
|**type**|the [flag](users/POST_users_id_flags.md#files) to unset|string|x||
|**parameter**| **description**| **type** |**required?** |**default**|

### Response
***


200 and confirmation message

[Errors](../../resources/errors.md#files)


### Examples
***

`https://api.eyeem.com/v2/users/1013/unsubscribe?token=abcdefg&type=email_friend_joined`


