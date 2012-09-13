# DELETE /photos/#{id}/comments#{comment_id}    
***
`/photos/#{id}/comments#{comment_id}`

### Description
***
Delete a specific comment on a photo (users can only delete their own comments).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want retrieve information about.|integer|x||
|**comment_id**|The id of the comment we want to delete.|integer|x||


### Response
***


200 if success

[Errors](../../resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/comments/11353`





 