# GET /users/#{id} 
***
`/useres/#{id}`

### Description
***
Get a user's profile information.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**detailed**| returns further user details|boolean||0|



### Response
***
200 and a user object 

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013`

