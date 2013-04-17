# POST /users/#{id}/facebookPage    
***
`/users/#{id}/facebookPage`

### Description
***
Only available for the authenticated user, this call sets a default page or his timeline to upload to.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to retrieve information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**page_id**|id of the page or "me"|string|x||

### Response
***

200 


[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/me/facebookPage`


