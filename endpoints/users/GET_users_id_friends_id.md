# GET /users/#{id}/friends/#{friend_id} 
***
`/users/#{id}/friends/#{friend_id}`

### Description
***
Check if the given user is friends with (follows) another user.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**friend_id**|the user id of the friend|integer|x||



### Response
***



200 if friends, 404 if not



[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013/friends/1015`
