# PUT /users/#{id}/friends/#{friend_id} 
***
`/users/#{id}/friends/#{friend_id}`

### Description
***
add a user to the friends list (follow).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**friend_id**|the user id of the friend to follow|integer|x||



### Response
***



200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/friends/1015`



