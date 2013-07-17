# GET /albums/#{id}
***
`/albums/#{id}`

### Description
***
Retrieves album specified in the id URL query parameter.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||0|
|**numPhotos**|the number of album photos to return|integer||10|
|**includeContributors**|if true, returns the album contributors|boolean| |0|
|**numContributors**|the number of album contributors to return|integer||30|
|**includeLikers**| if true, returns the album likers|boolean| |0|
|**numLikers**|the number of album favoriters to return|integer||30|
|**photoDetails**|whether to return the photo details (comments, likes, albums)|boolean||0|
|**photoLikers**|if true, returns the album contributors|boolean| |1|
|**photoNumLikers**|the number of album contributors to return|integer||1|
|**photoPeople**| if true, returns the album likers|boolean| |1|
|**photoNumPeople**|the number of album favoriters to return|integer||1|
|**photoComments**| if true, returns the album likers|boolean| |1|
|**photoNumComments**|the number of album favoriters to return|integer||1|
|**photoAlbums**|returns the albums a photo belongs to|boolean||1|
|**userDetails**|returns the detailed user profile for each photo|boolean||0|

### Response
***


200 and a dictionary containing the album object
