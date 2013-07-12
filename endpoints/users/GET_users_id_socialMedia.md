# GET /users/#{id}/socialMedia     
***
`/users/#{id}/socialMedia`

### Description
***
Only available for the authenticated user, this call returns the status of the various connected social media accounts.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to retrieve information from|integer|x||



### Response
***


200 and an array of services objects

[Errors](../../resources/errors.md#files)
### Examples
***

`https://api.eyeem.com/v2/users/me/socialMedia`



