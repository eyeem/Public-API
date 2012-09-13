# GET /photos/#{id}/likers/#{user_id} 
***
`/photos/#{id}/likers/#{user_id}`

### Description
***
Checks whether a user likes a photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**user_id**|The id of the user we want check.|integer|x||



### Response
***

200 if the user likes a photo, 404 otherwise


[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)
### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/likers/1013`



 