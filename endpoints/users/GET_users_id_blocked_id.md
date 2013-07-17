# GET /users/#{id}/blocked/#{blocked_id} 
***
`/users/#{id}/blocked/#{blocked_id}`

### Description
***
check if the person (blocked_id) is blocked by the user (id)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**blocked_id**|the user id of the blocked person|integer|x||



### Response
***



200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/blocked/1015`



