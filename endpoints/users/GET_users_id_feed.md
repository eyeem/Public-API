# GET /users/#{id}/feed 
***
`/users/#{id}/feed`

### Description
***
Gets albums relevant to a user (selection happens server side, includes albums they like, albums they contributed to, trending, recommended and nearby albums)

If requested from a user other than the authenticated one, only the user's liked albums are returned

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**X-GEO-closestVenueFsIds**|should contain a comma-separated list of foursquare venue ids|string|||
|**X-GEO-cityName**|should contain the name of the city the device "thinks" it's in|string|||
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||1|
|**numPhotos**|the number of album photos to return|integer||10|
|**includeContributors**|if true, returns the album contributors|boolean| |0|
|**includeLikers**| if true, returns the album likers|boolean| |0|

### Response
***

200 and and a dictionary containing limit, offset, total and an array of albums

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/feed`




