# GET /users/#{id}/friendsPhotos 
***
`/users/#{id}/friendsPhotos`

### Description
***
Get all the photos by users that the given user follows (ordered chronologically).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of photos to return|integer||30|
|**offset**|(offset of photos to start at|integer||0|
|**after**|new pagination|photo ID|||
|**before**|new pagination|photo ID|||
|**order**|sort order (desc,asc)|string||desc|
|**detailed**|returns a simple or detailed photo object|boolean||1|
|**includeComments**|If true, returns the latest two comments of a photo inline|boolean||1|
|**numComments**|the number of comments to include in the response|integer||2|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||1|
|**numLikers**|the number of likers to include in the response|integer||1|
|**includePeople**|If true, returns the tagged people in a photo|boolean||1|
|**numPeople**|the number of tagged people to include in the response|integer||4|
|**includeAlbums**|If true, includes the albums a photo is part of|boolean||0|
|**userDetails**|If true, includes the detailed user profile of each photographer|boolean||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of photo objects