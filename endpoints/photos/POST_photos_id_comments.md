# POST /photos/#{id}/comments   
***
`/photos/#{id}/comments`

### Description
***
Adds a new comment to a photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want post a comment.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**message**| the body of the comment (the message can optionally contain @mentioned users in the form @{nickname}[user:{id}]) |string|x||
|**albumId**|the ID of the album that the user was in when commenting|integer|||

### Response
***


200 and a comment object

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/comments?message=Love_it`

