# GET /users
***
`/useres`

### Description
***
Search for users or retrieve suggested users.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|string to search users by|string|||
|**suggested**|returns suggested users (replaces "q")|boolean||0|
|**ids**|comma-separated list of ids (to be returned as users)|string|||
|**detailed**|rreturns a more detailed user object|boolean||1|
|**friends**|used when getting users from a search query, searches only among friends|boolean||0|
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|


### Response
***
200, pagination params and a array of user objects (either those queried, or those suggested)

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users?q=ramzi&limit=25`


```javascript


{
  "users": {
    "offset": 0,
    "limit": 25,
    "total": 16,
    "items": [
      {
        "id": "2089",
        "nickname": "RamziRizk",
        "fullname": "Ramzi Rizk",
        "webUrl": "http://www.eyeem.com/u/RamziRizk",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg",
        "totalPhotos": 0,
        "totalFollowers": 10,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": "test account. http://www.rrizk.com"
      },
      {
        "id": "6494",
        "nickname": "ramzissamara",
        "fullname": "Ramzi Samara",
        "webUrl": "http://www.eyeem.com/u/ramzissamara",
        "thumbUrl": "https://graph.facebook.com/10140080/picture?type=square",
        "photoUrl": "https://graph.facebook.com/10140080/picture?type=large",
        "totalPhotos": 1,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": ""
      },
      {
        "id": "6539",
        "nickname": "ramzin",
        "fullname": "ramzin",
        "webUrl": "http://www.eyeem.com/u/ramzin",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": ""
      },
      {
        "id": "17675",
        "nickname": "ramzirabia9",
        "fullname": "Ramzi Rabia",
        "webUrl": "http://www.eyeem.com/u/ramzirabia9",
        "thumbUrl": "https://graph.facebook.com/1110024886/picture?type=square",
        "photoUrl": "https://graph.facebook.com/1110024886/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": ""
      },
      {
        "id": "52233",
        "nickname": "Ramzi",
        "fullname": "Ramzi",
        "webUrl": "http://www.eyeem.com/u/Ramzi",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/a25b05365a39b7f3f843e27b75e1dbdcc8e8c9e5.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/a25b05365a39b7f3f843e27b75e1dbdcc8e8c9e5.jpg",
        "totalPhotos": 1,
        "totalFollowers": 1,
        "totalFriends": 1,
        "totalLikedAlbums": 6,
        "totalLikedPhotos": 1,
        "description": null
      },
      {
        "id": "58194",
        "nickname": "ramziwelcome",
        "fullname": "ramzi welcome",
        "webUrl": "http://www.eyeem.com/u/ramziwelcome",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "58195",
        "nickname": "ramzirrizk7",
        "fullname": "ramzi rrizk7",
        "webUrl": "http://www.eyeem.com/u/ramzirrizk7",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "61338",
        "nickname": "ramzistephan",
        "fullname": "Ramzi Stephan",
        "webUrl": "http://www.eyeem.com/u/ramzistephan",
        "thumbUrl": "https://graph.facebook.com/652131642/picture?type=square",
        "photoUrl": "https://graph.facebook.com/652131642/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 3,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "72556",
        "nickname": "ramzikh9",
        "fullname": "RamZi Kh",
        "webUrl": "http://www.eyeem.com/u/ramzikh9",
        "thumbUrl": "https://graph.facebook.com/100000539177135/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100000539177135/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 12,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "126616",
        "nickname": "ramzikacem3",
        "fullname": "Ramzi Kacem",
        "webUrl": "http://www.eyeem.com/u/ramzikacem3",
        "thumbUrl": "https://graph.facebook.com/1092686257/picture?type=square",
        "photoUrl": "https://graph.facebook.com/1092686257/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "136129",
        "nickname": "ramzi1",
        "fullname": "ramzi",
        "webUrl": "http://www.eyeem.com/u/ramzi1",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "136130",
        "nickname": "ramziammo",
        "fullname": "Ramzi Ammo",
        "webUrl": "http://www.eyeem.com/u/ramziammo",
        "thumbUrl": "https://graph.facebook.com/746879080/picture?type=square",
        "photoUrl": "https://graph.facebook.com/746879080/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "162978",
        "nickname": "juventinopersempre56614",
        "fullname": "Ramzi Juventino Pazzo",
        "webUrl": "http://www.eyeem.com/u/juventinopersempre56614",
        "thumbUrl": "https://graph.facebook.com/100004071199813/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100004071199813/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "174428",
        "nickname": "ramziabuyahya",
        "fullname": "Ramzi",
        "webUrl": "http://www.eyeem.com/u/ramziabuyahya",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "183653",
        "nickname": null,
        "fullname": "Ramzi Csc",
        "webUrl": "http://www.eyeem.com/u/183653",
        "thumbUrl": "https://graph.facebook.com/100004139560992/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100004139560992/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 0,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      },
      {
        "id": "186387",
        "nickname": null,
        "fullname": "Ramzi Hocine",
        "webUrl": "http://www.eyeem.com/u/186387",
        "thumbUrl": "https://graph.facebook.com/100004259771196/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100004259771196/picture?type=large",
        "totalPhotos": 0,
        "totalFollowers": 1,
        "totalFriends": 0,
        "totalLikedAlbums": 0,
        "totalLikedPhotos": 0,
        "description": null
      }
    ]
  }
}

```
