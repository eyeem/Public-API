# PUT /users/#{id}/blocked/#{blocked_id} 
***
`/users/#{id}/blocked/#{blocked_id}`

### Description
***
add a person to the blocked list (block).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**blocked_id**|the user id of the person to block|integer|x||



### Response
***



200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/blocked/1015`



