# GET /users/#{id}/followers  
***
`/users/#{id}/followers`

### Description
***
Get a user's followers.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**friend_id**|the user id of the friend|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of users to return|integer||20|
|**offset**|offset of users to start at|integer||0|
|**onlyId**|returns a json array userIds containing just the ids|boolean|||
|**detailed**|returns the details for every user >> num photos, num followers, etc|boolean||0|

### Response
***


200 and and a dictionary containing limit, offset, total and an array of followers (users)




[Errors][]

### Examples
***

`https://www.eyeem.com/api/v2/users/me/friends/1015`







[Errors]: 