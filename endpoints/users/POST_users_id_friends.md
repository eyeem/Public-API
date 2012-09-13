# POST /users/#{id}/friends 
***
`/users/#{id}/friends`

### Description
***
Add users to the friends list (follow)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**friend_id**|comma-separated list of user_ids|string|x||


### Response
***


200 if success




[Errors][]

### Examples
***

`https://www.eyeem.com/api/v2/users/me/friends?friend_id=1,1230,42325,55351,123425`







[Errors]: 