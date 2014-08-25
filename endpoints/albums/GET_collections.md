# GET /collection
***
`/collection`

### Description
***
Retrieves a collection of photos (at the moment, only "nearbyLive" is supported)

NearbyLive is a mixture of photos uploaded very close to me w/in the last 2 hours + all nearby photos (geo-box)
### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**parameter**| **description**| **type** |**required?** |**default**|
|**type**|type of collection, atm only "nearbyLive"|string|||
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|
|**lat**|latitude|float||X|
|**lng**|longitude|float||X|
|**detailed**| If true, allows for inline embedding of detailed objects|boolean||0|
|**includeComments**| If true, returns the latest two comments of a photo inline|boolean||0|
|**numComments**| number of comments to return inline|integer||2|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean| |0|
|**numLikers**| number of likers to return inline|integer||1|
|**includeAlbums**|If true, returns the albums inline|boolean||0|
|**includePeople**|If true, returns the tagged persons in a photo|boolean| |0|
|**numPeople**| number of tagged people to return inline|integer||10|
|**simpleDescription**|If true, returns a simple, human-readable photo description|boolean||0|

### Response
***
200 and a dictionary containing the album object
