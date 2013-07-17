# DELETE /users/#{id}/blocked/#{blocked_id} 
***
`/users/#{id}/blocked/#{blocked_id}`

### Description
***
Remove a person from the blocked list (unblock).

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



