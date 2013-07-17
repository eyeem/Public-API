# GET /users/#{id} 
***
`/useres/#{id}`

### Description
***
Get a user's profile information. some parameters (liked settings, are only available to native clients.)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||0|
|**numPhotos**|the number of album photos to return|integer||10|
|**photoDetails**|whether to return the photo details (comments, likes, albums)|boolean||0|
|**photoLikers**|if true, returns the album contributors|boolean| |1|
|**photoNumLikers**|the number of album contributors to return|integer||1|
|**photoPeople**| if true, returns the album likers|boolean| |1|
|**photoNumPeople**|the number of album favoriters to return|integer||1|
|**photoComments**| if true, returns the album likers|boolean| |1|
|**photoNumComments**|the number of album favoriters to return|integer||2|
|**photoAlbums**|returns the albums a photo belongs to|boolean||1|
|**includeSettings**|returns the user settings (native/own account)|boolean||0|


### Response
***
200 and a user object 