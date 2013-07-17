# GET /users/#{id}/suggestions  
***
`/users/#{id}/suggestions`

### Description
***
Get a list of suggested people to follow.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**service**|string(facebook, twitter, eyeem)|string||"all"|
|**detailed**|returns the details for every user >> num photos, num followers, etc|boolean||0|

### Response
***


200 and a dictionary containing limit, offset, total and an array of suggested people (users)

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/suggestions`