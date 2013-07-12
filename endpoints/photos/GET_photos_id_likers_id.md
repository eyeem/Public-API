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

[Errors](../../resources/errors.md#files)
### Examples
***

`https://api.eyeem.com/v2/photos/939584/likers/3346`


```json

{
  "message": "User has favorited this photo."
}

```
 