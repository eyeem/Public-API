# PATCH /photos/#{id}/comments/{id} (with POST and PUT as fallback)
***
`/photos/#{id}/comments/{id}`

### Description
***
Update an existing comment on a photo (only possible to owner)

Maximum comment length: 800 characters!

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want post a comment.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**message**| the body of the comment (the message can optionally contain @mentioned users in the form @{nickname}) |string|x||

### Response
***


200 and a comment object

[Errors](../../resources/errors.md#files)
