# GET /users/#{id}/friends 
***
`/users/#{id}/friends`

### Description
***
Get a user's friends (users that they follow)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of users to return|integer||20|
|**offset**|offset of users to start at|integer||0|
|**onlyId**|returns a json array userIds containing just the ids|boolean|||
|**detailed**|returns the details for every user >> num photos, num followers, etc|boolean||0|

### Response
***

200 and and a dictionary containing limit, offset, total and an array of friends (users)


[Errors](../../resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013/friends`

