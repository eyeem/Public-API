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
|**X-GEO-closestVenueFsIds**|should contain a comma-separated list of foursquare venue ids|string|||
|**X-GEO-cityName**|should contain the name of the city the device "thinks" it's in|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of albums

[Errors](../../resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/users/me/feed`




