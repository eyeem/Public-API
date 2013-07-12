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

`http://www.eyeem.com/api/v2/users/me`

```json
{
  "user": {
    "id": "174921",
    "nickname": "sb",
    "fullname": "Sebastian",
    "webUrl": "http://www.eyeem.com/u/sb",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/50/1629b0a3a6a4c9772fba1c82b2972ceff4b5c49a-1351259458",
    "photoUrl": "http://www.eyeem.com/thumb/sq/200/1629b0a3a6a4c9772fba1c82b2972ceff4b5c49a-1351259458",
    "totalPhotos": 89,
    "totalFollowers": 171,
    "totalFriends": 69,
    "totalLikedAlbums": 10,
    "totalLikedPhotos": 4427,
    "description": " @EyeEm",
    "email": "sebastian@eyeem.com",
    "emailNotifications": true,
    "pushNotifications": true,
    "services": {
      "facebook": {
        "third_party_id": "4Ci6GTRNyX8vIWfBBM1n09m9JdQ",
        "id": "100000492297860",
        "upload": false,
        "photolike": true,
        "photodiscover": false,
        "photocomment": false,
        "albumlike": false,
        "userfollow": false,
        "timelinepopup": true,
        "managedPages": [
          {
            "id": "154793581210614",
            "name": "Halö",
            "posting": 0
          }
        ],
        "status": "active"
      },
      "twitter": {
        "id": "19140455",
        "nickname": "ksslng",
        "status": "active"
      },
      "tumblr": {
        "status": "inactive"
      },
      "foursquare": {
        "status": "active"
      },
      "flickr": {
        "status": "inactive"
      }
    },
    "newsSettings": {
      "push_photo_like": true,
      "push_photo_comment": true,
      "push_user_follower": true,
      "push_user_joined": true,
      "push_album_contributor": true,
      "push_photo_comment_mention": true,
      "email_photo_like": false,
      "email_photo_comment": false,
      "email_user_follower": false,
      "email_user_joined": false,
      "email_album_contributor": false,
      "email_photo_comment_mention": false,
      "email_weekly_newsletter": true
    }
  }
}
```