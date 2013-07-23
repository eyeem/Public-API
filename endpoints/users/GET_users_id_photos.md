# GET /users/#{id}/photos
***
`/users/#{id}/photos`

### Description
***
Get the given user's photos, sorted chronologically (default).

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
|**onlyId**|if true, returns only the photo ids|boolean||0|
|**filter**|get a subset, atm only "nearby" supported. requires lat/lng|string|||
|**lat**|latitude|float| for filter="nearby"||
|**lng**|longitude|float| for filter="nearby"||
|**sort**|sort order (top,chronological)|string||chronological|
|**detailed**|returns a simple or detailed photo object|boolean||0|
|**includeComments**|If true, returns the latest two comments of a photo inline|boolean||0|
|**numComments**|the number of comments to include in the response|integer||2|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||0|
|**numLikers**|the number of likers to include in the response|integer||2|
|**includePeople**|If true, returns the tagged people in a photo|boolean||0|
|**numPeople**|the number of tagged people to include in the response|integer||4|
|**includeAlbums**|If true, includes the albums a photo is part of|boolean||0|
|**simpleDescription**|If true, returns a simple, human-readable photo description|boolean||0|

### Response
***

200 and and a dictionary containing limit, offset, total and an array of photo objects

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/1013/photos?limit=10`


```json


{
  "photos": {
    "offset": 0,
    "limit": 10,
    "total": 1593,
    "items": [
      {
        "id": 948082,
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/82acc3f0656b5c91e9a8c30ae4700b78908708fc-1347567992",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/82acc3f0656b5c91e9a8c30ae4700b78908708fc-1347567992",
        "width": 816,
        "height": 612,
        "updated": "2012-09-13T22:27:31+0200"
      },
      {
        "id": 946005,
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/b4ea428ae4c33ce70f38368d5a5b482b5199fb0c-1347534463",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/b4ea428ae4c33ce70f38368d5a5b482b5199fb0c-1347534463",
        "width": 816,
        "height": 612,
        "updated": "2012-09-13T13:07:56+0200"
      },
      {
        "id": 936990,
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/a9e6a20f2268589b6d68511d43dd1ce93960f55f-1347365013",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/a9e6a20f2268589b6d68511d43dd1ce93960f55f-1347365013",
        "width": 816,
        "height": 612,
        "updated": "2012-09-11T14:03:38+0200"
      },
      {
        "id": 936979,
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/d743ac378b05716b448748b0674c801bd0d3280e-1347364565",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/d743ac378b05716b448748b0674c801bd0d3280e-1347364565",
        "width": 816,
        "height": 612,
        "updated": "2012-09-11T13:57:07+0200"
      },
      {
        "id": 936972,
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/2ea3ee9df1bf7e3ddd32f5ac66a6297416ffcafa-1347364488",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/2ea3ee9df1bf7e3ddd32f5ac66a6297416ffcafa-1347364488",
        "width": 816,
        "height": 612,
        "updated": "2012-09-11T13:55:12+0200"
      },
      {
        "id": 936757,
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/f7341a38de57d5b4526ec14622dd6ee5e639a0d8-1347360965",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/f7341a38de57d5b4526ec14622dd6ee5e639a0d8-1347360965",
        "width": 816,
        "height": 612,
        "updated": "2012-09-11T12:56:18+0200"
      },
      {
        "id": "936281",
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/f302b7bb9bfcf702ce81a7f164cd7a565b0abf52-1347351872",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/f302b7bb9bfcf702ce81a7f164cd7a565b0abf52-1347351872",
        "width": 816,
        "height": 612,
        "updated": "2012-09-11T10:24:57+0200"
      },
      {
        "id": "936254",
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/2ca5be2f671e437eeb256e858541bcbfcac1c6b7-1347351397",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/2ca5be2f671e437eeb256e858541bcbfcac1c6b7-1347351397",
        "width": 816,
        "height": 612,
        "updated": "2012-09-11T10:20:20+0200"
      },
      {
        "id": "933480",
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/57a099f5514de955e30743d2b40f5d3afc9c2963-1347298351",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/57a099f5514de955e30743d2b40f5d3afc9c2963-1347298351",
        "width": 816,
        "height": 612,
        "updated": "2012-09-10T19:32:49+0200"
      },
      {
        "id": "919213",
        "thumbUrl": "http://cdn.eyeem.com/thumb/h/100/dc2828c845c9802a7e81a13b4cb713852bc2f027-1347110117",
        "photoUrl": "http://cdn.eyeem.com/thumb/640/480/dc2828c845c9802a7e81a13b4cb713852bc2f027-1347110117",
        "width": 816,
        "height": 612,
        "updated": "2012-09-08T15:16:30+0200"
      }
    ]
  }
}

```

