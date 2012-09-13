# DELETE /photos/#{id} 
***
`/photos/#{id}`

### Description
***
Deletes a photo by id (has to be a photo belonging to the authenticated user).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want to delete.|integer|x||


### Response
***



200 if success

[Errors](../../resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234`




 