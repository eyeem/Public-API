# DELETE /users/#{id}/friends/#{friend_id} 
***
`/users/#{id}/friends/#{friend_id}`

### Description
***
Remove a user from the friends list (unfollow).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**friend_id**|the user id of the friend|integer|x||



### Response
***



200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/me/friends/1015`



