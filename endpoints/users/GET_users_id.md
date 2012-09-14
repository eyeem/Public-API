# GET /users/#{id} 
***
`/useres/#{id}`

### Description
***
Get a user's profile information.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**detailed**| returns further user details|boolean||0|



### Response
***
200 and a user object 

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013`

```javascript

{
  "user": {
    "id": "1013",
    "nickname": "ramz",
    "fullname": "ramz",
    "webUrl": "http://www.eyeem.com/u/ramz",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/50/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg",
    "photoUrl": "http://www.eyeem.com/thumb/sq/200/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg",
    "totalPhotos": 1593,
    "totalFollowers": 659,
    "totalFriends": 869,
    "totalLikedAlbums": 50,
    "totalLikedPhotos": 3978,
    "description": "EyeEm Ramz. EyeEm Happy! Srsly. Choo choo!!"
  }
}

```