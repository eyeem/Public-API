# GET /photos
***
`/photos`

### Description
***
Retrieves the authenticated user's latest twenty photos or popular photos (collection).

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**type**|"popular" returns popular photos, else defaults to the user's photos|string|||
|**ids**| comma-separated list of ids to return (if type not specified)|string|||
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|
|**includeComments**| If true, returns the latest two comments of a photo inline|boolean||0|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean| |0|


### Response
***

200 and an array of photos.

[Errors](../../resources/errors.md#files)
### Examples
***

`https://www.eyeem.com/api/v2/photos?offset=0&limit=20&includeComments=1`





 