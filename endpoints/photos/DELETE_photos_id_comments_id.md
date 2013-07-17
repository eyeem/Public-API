# DELETE /photos/#{id}/comments#{comment_id}    
***
`/photos/#{id}/comments#{comment_id}`

### Description
***
Delete a specific comment on a photo (users can only delete their own comments, or comments on their own photos).

requires authed user with delete rights.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want retrieve information about.|integer|x||
|**comment_id**|The id of the comment we want to delete.|integer|x||


### Response
***


200 if success

[Errors](../../resources/errors.md#files)