# DELETE /photos/#{id}/likers/#{user_id} 
***
`/photos/#{id}/likers/#{user_id}`

### Description
***
Unlike a photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**user_id**|The id of the user who unlikes the photo.|integer|x||

### Response
***

200 if success

[Errors](../../resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/likers/me`





 