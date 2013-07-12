# GET /users/#{id}/followers/#{friend_id}   
***
`/users/#{id}/followers/#{friend_id}`

### Description
***
Check if a user follows the given user.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**friend_id**|the user id of the friend|integer|x||


### Response
***

200 if following, 404 if not


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/1013/followers/1015`


```json


{
  "message": "User X is following user Y."
}

```

