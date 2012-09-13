# PUT /photos/#{id}/likers/#{user_id} 
***
`/photos/#{id}/likers/#{user_id}`

### Description
***
Like a photo.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**user_id**|The id of the user who likes the photo.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**albumId**|The ID of the album that the user was in when liking.|integer|||



### Response
***

200 if success

[Errors](../../resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/likers/me`

