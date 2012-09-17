#API data model and object types
***

Below are the possible representation of users, albums, photos, comments, topics, news, and services.
The objects and variables are hopefully self-explanatory, but we will describe those that might be not so clear.

For users, albums and photos, we will also provide the simplest valid object that the server might send back, as well as the possible dictionary names that would contain items of the respective objects.

##Users
***
#### Minimum valid object
```javascript
      {
        "id": "1013",
        "fullname": "Ramzi Rizk",
        "nickname": "ramz",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/9c24eab725f8aa03b99c396dd4d45f2b9asdf3.jpg"
      }
```
#### Extended Object
```javascript
{
  "user": {
    "id": "1013",
    "fullname": "ramz",
    "nickname": "ramz",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg",
    "description": "EyeEm Ramz. EyeEm Happy! Srsly. Choo choo!!",
    "photoUrl": "http://www.eyeem.com/thumb/sq/200/0a4a321f1806b00c668d111a314bd98a14985765.jpg",
    "totalPhotos": 1040,
    "totalFollowers": 283,
    "totalFriends": 478,
    "totalLikedAlbums": 58,
    "email": "ramz@eyeem.com",
    "emailNotifications": true,
    "pushNotifications": true,
    "admin": true,
    "newsSettings": {
      "push_photo_like": true,
      "push_photo_comment": true,
      "push_user_follower": true,
      "push_user_joined": true,
      "push_album_contributor": true,
      "email_photo_like": true,
      "email_photo_comment": true,
      "email_user_follower": true,
      "email_user_joined": true,
      "email_album_contributor": true
    },
    "services": {
      "facebook": {
        "status": "active"
        "id": 12341231235
        "primary": true
        "status": "active"
        "status": "active"
        "status": "active"
        "status": "active"
        "status": "active"

      },
      "twitter": {
        "status": "active"
        "id": 12341231235
        "nickname": "ramz"
      },
      "foursquare": {
        "status": "active"
      },
      "tumblr": {
        "status": "active"
      },
      "flickr": {
        "status": "inactive"
        "id": 12341231235
        "nickname": "letempest"
      }
    }
  }
}
```
#### Remarks
* Arrays of user items can have the following dictionary names as wrappers: `friends`, `contributors`, `followers`, `likers`, `users`
* The fields `email`, `emailNotifications`, `pushNotifications` and the `services` dictionary are only available for the authenticated user object

##Albums
***
#### Minimum valid object
```javascript
{
    "id": "17",
    "name": "Berlin",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/200/5993d6f01a18a8fa6a3b13034ca1d8a1e7345edf-1321712288",
    "updated": "2012-02-03T18:06:08+0000"
  }
```
#### Extended Object
```javascript
{
  "album": {
    "id": "17",
    "name": "Berlin",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/200/5993d6f01a18a8fa6a3b13034ca1d8a1e7345edf-1321712288",
    "updated": "2012-02-03T18:06:08+0000",
    "type": "city",
    "location": {
      "latitude": "52.52437",
      "longitude": "13.41053",
      "countryAlbum": {
        "id": "23",
        "name": "Germany",
        "type": "country",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2645e5292c071481368030259ca6102dce273435-1347878975",
        "updated": "2012-09-17T12:50:00+0200"
      }
    },
    "webUrl": "http://www.eyeem.com/a/17",
    "totalPhotos": "10432",
    "totalLikers": 127,
    "totalContributors": 814,
    "hidden": true (depends on user setting)
    "photos": {
      "items": [
        {
          "id": "216365",
          "thumbUrl": "http://www.eyeem.com/thumb/h/100/3ca2b83032785f475476e77d20f2c41e230ec7f7-1328292321",
          "photoUrl": "http://www.eyeem.com/thumb/640/480/3ca2b83032785f475476e77d20f2c41e230ec7f7-1328292321",
          "width": 1024,
          "height": 768,
          "updated": "2012-02-03T18:06:08+0000",
          "user": {
            "id": "4463",
            "fullname": "Fabian-Carlos Guhl",
            "nickname": null,
            "thumbUrl": "https://graph.facebook.com/536656083/picture?type=square"
          },
          "caption": "Discussing world peace at Oburger 69",
          "totalLikes": 0,
          "totalComments": 0,
          "comments": {
            "items": []
          },
          "likers": {
            "items": []
          }
        },
        {
          "id": "216313",
          "thumbUrl": "http://www.eyeem.com/thumb/h/100/1ac3d29659fc7bcf65882d66a676bef4acc1ad22-1328290328",
          "photoUrl": "http://www.eyeem.com/thumb/640/480/1ac3d29659fc7bcf65882d66a676bef4acc1ad22-1328290328",
          "width": 1224,
          "height": 1632,
          "updated": "2012-02-03T17:33:07+0000",
          "user": {
            "id": "60534",
            "fullname": "666",
            "nickname": null,
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/b9101e64f89be9c65bb6f4d9ee1dee66f4d43ad1.jpg"
          },
          "caption": "table at Marietta",
          "totalLikes": 2,
          "totalComments": 0,
          "comments": {
            "items": []
          },
          "likers": {
            "items": [
              {
                "id": "11697",
                "fullname": "steve",
                "nickname": "psoneeleven",
                "thumbUrl": "http://www.eyeem.com/thumb/sq/50/c08e8382817585604405e70813cf650ab20b7577.jpg"
              }
            ]
          }
        }
      ]
    },
    "contributors": {
      "offset": 0,
      "limit": 3,
      "total": 814,
      "items": [
        {
          "id": "1025",
          "fullname": "Moritz Otto",
          "nickname": "moritzotto",
          "thumbUrl": ""
        },
        {
          "id": "1013",
          "fullname": "ramz",
          "nickname": "ramz",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg"
        },
        {
          "id": "1038",
          "fullname": "Graf Heldenbrand",
          "nickname": null,
          "thumbUrl": ""
        },
      ]
    },
    "likers": {
      "offset": 0,
      "limit": 4,
      "total": 127,
      "items": [
        {
          "id": "7801",
          "fullname": "Sandro Günther",
          "nickname": null,
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/ab999ad7e0ac73a7a01cdffcfd5f89b5ce853594.jpg"
        },
        {
          "id": "59083",
          "fullname": "Mathias",
          "nickname": "mathias",
          "thumbUrl": "https://graph.facebook.com/1087532650/picture?type=square"
        },
        {
          "id": "58649",
          "fullname": "Diiana Berlin",
          "nickname": null,
          "thumbUrl": "https://graph.facebook.com/100000343669388/picture?type=square"
        },
        {
          "id": "11117",
          "fullname": "Andreas Zeiser",
          "nickname": null,
          "thumbUrl": "https://graph.facebook.com/100000020995756/picture?type=square"
        }
      ]
    }
  }
}
```
#### Remarks
* Arrays of album items can have the following dictionary names as wrappers: `albums`, `likedAlbums`, `feedAlbums`
* Albums can have the following type: `tag`,`venue`,`event`,`city`,`country`,`live`,`popular`,`radius`,`special`
* The extended album object above is an example based on the following request:
`https://www.eyeem.com/api/v2/albums/17?detailed=1&includePhotos=1&numPhotos=2&photoDetails=1&includeContributors=1&includeLikers=1`
In such a request, the number of inline photos to return, whether to include the photo details (comments, likes, etc) is of course optional, typically, the photos, contributors and likers should be retrieved using additional calls to the respective endpoints. Such calls also offer the option to request more details (such as the other albums to which a photo belongs)

##Photos
***
#### Minimum valid object
```javascript
      {
        "id": "215058",
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/70b5d5feefc5946bb7b912b8661c3329912fda3d-1328177792",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/70b5d5feefc5946bb7b912b8661c3329912fda3d-1328177792",
        "width": 1530,
        "height": 2048,
        "updated": "2012-02-02T10:16:33+0000"
      }
```
#### Extended Object
```javascript
{
  "photo": {
    "id": "215058",
    "thumbUrl": "http://www.eyeem.com/thumb/h/100/70b5d5feefc5946bb7b912b8661c3329912fda3d-1328177792",
    "photoUrl": "http://www.eyeem.com/thumb/640/480/70b5d5feefc5946bb7b912b8661c3329912fda3d-1328177792",
    "width": 1530,
    "height": 2048,
    "updated": "2012-02-02T10:16:33+0000",
    "webUrl": "http://www.eyeem.com/p/215058",
    "user": {
      "id": "1013",
      "fullname": "ramz",
      "nickname": "ramz",
      "webUrl": "http://www.eyeem.com/u/ramz",
      "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg",
      "photoUrl": "http://www.eyeem.com/thumb/sq/200/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg"
    },
    "title": "11:11 at Coffee to go",
    "caption": "11:11 at Coffee to go",
    "latitude": "52.53499985",
    "longitude": "13.40600014",
    "totalLikes": 12,
    "totalComments": 2,
    "comments": {
      "items": [
        {
          "id": "36038",
          "photoId": "215058",
          "message": "i realized i was at the exact same place at the exact same moment on 11:11, had to do it :)",
          "user": {
            "id": "1013",
            "fullname": "ramz",
            "nickname": "ramz",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg"
          },
          "updated": "2012-02-02T10:36:03+0000"
        },
        {
          "id": "36036",
          "photoId": "215058",
          "message": "Simply brilliant!",
          "user": {
            "id": "1923",
            "fullname": "Stephen Mohammed",
            "nickname": "stephenmohammed",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/2e9fe28f92959b9b07ac4ad1cb91534c5ee657e6.jpg"
          },
          "updated": "2012-02-02T10:32:35+0000"
        }
      ]
    },
    "likers": {
      "items": [
        {
          "id": "4962",
          "fullname": "Sarah Weinknecht",
          "nickname": null,
          "thumbUrl": "https://graph.facebook.com/583303009/picture?type=square"
        }
      ]
    },
    "albums": {
      "items": [
        {
          "id": "17",
          "name": "Berlin",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/5993d6f01a18a8fa6a3b13034ca1d8a1e7345edf-1321712288",
          "updated": "2012-02-03T18:06:08+0000",
          "type": "city"
        },
        {
          "id": "23",
          "name": "Germany",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/17662e8dfa7d912c649220f29a85672024fa3d01-1321811964",
          "updated": "2012-02-03T18:31:28+0000",
          "type": "country"
        },
        {
          "id": "10521",
          "name": "Coffee to go",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/70b5d5feefc5946bb7b912b8661c3329912fda3d-1328177792",
          "updated": "2012-02-02T10:16:33+0000",
          "type": "venue"
        },
        {
          "id": "55744",
          "name": "11:11",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/86dce608a49b919c5ee07658e503f5c5d0d8d899-1321956886",
          "updated": "2012-02-03T10:20:08+0000",
          "type": "tag"
        },
        {
          "id": "112649",
          "name": "11:11 at Coffee to go",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/70b5d5feefc5946bb7b912b8661c3329912fda3d-1328177792",
          "updated": "2012-02-02T10:16:38+0000",
          "type": "event"
        }
      ]
    }
  }
}
```
#### Remarks
* `likers` is an array of users
* Arrays of photo items can have the following dictionary names as wrappers: `photos`, `friendsPhotos`, `likedPhotos`

##Comments
***
```javascript
          {
              "id": "36038",
              "photoId": "215058",
              "message": "i realized @gen was at the exact same place at the exact same moment on 11:11 - same for @lorenz, had to do it :)",
              "extendedMessage": "i realized @gen[user:1015] was at the exact same place at the exact same moment on 11:11 - same for @lorenz[user:1019], had to do it :)",
              "user": {
                "id": "1013",
                "fullname": "ramz",
                "nickname": "ramz",
                "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg"
              },
			"mentionedUsers": [
			  {
				"id": "1015",
				"nickname": null,
				"fullname": "Gen Sadakane",
				"webUrl": "http://eyeem.local/frontend_dev.php/u/1015",
				"thumbUrl": "http://eyeem.local/frontend_dev.php/thumb/sq/50/default_profile.jpg",
				"photoUrl": "http://eyeem.local/frontend_dev.php/thumb/sq/200/default_profile.jpg"
			  },
			  {
				"id": "1019",
				"nickname": null,
				"fullname": "Lorenz Aschoff",
				"webUrl": "http://eyeem.local/frontend_dev.php/u/1019",
				"thumbUrl": "http://eyeem.local/frontend_dev.php/thumb/sq/50/fd8cce4ba31831d8bcb918ec6d879935355b726d.jpg",
				"photoUrl": "http://eyeem.local/frontend_dev.php/thumb/sq/200/fd8cce4ba31831d8bcb918ec6d879935355b726d.jpg"
			  }
			],
              "updated": "2012-02-02T10:36:03+0000"			            
            }
```
### Remarks
* Comment objects always include a basic user object identifying the comment's author

##Topics
***
```javascript
     {
        "name": "Waiting for the bell",
        "totalPhotos": "4"
      }
```
### Remarks
* Topics share the same ids as their respective albums.

##News
***
```javascript
      {
        "id": "19588",
        "itemType": "photo",
        "newsType": "like",
        "photo":{ PHOTO Object if available}
        "user":{ USER Object if available}
        "album":{ ALBUM Object if available}
        "comment":{ COMMENT Object if available}        
        "updated": "2012-02-03T15:11:20+0000",
        "seen": true
      }
```

alternatively, if it's a blog post:

```javascript
      {
        "id": "19588",
        "itemType": "url",
        "newsType": "blogPost",
        "title": "New Blog Post:",
        "body": "Your Week on EyeEm",
        "thumbUrl": "http://blog.eyeem.com/coolimage.jpg",
        "url": "http://blog.eyeem.com/blogpostID",        
        "updated": "2012-02-03T15:11:20+0000",
        "seen": true
      }
```

### Remarks:
* itemType dictates what type of object the news item links to. Possible values: `photo`, `user`, `album`
* newsType dictates what type of notification this is. Possible values: `like`, `comment`, `follow`, `commentAfter`

##Services
***
```javascript
{
  "services": {
    "facebook": {
      "status": "active"
      "id": "12342335"
      "upload": true
      "primary": true
      "photolike": true
      "photocomment": true
      "albumlike": true
      "userfollow": true
    },
    "twitter": {
      "status": "active"
      "nickname": "EyeEm"
      "id": "12342335"
    },
    "foursquare": {
      "status": "active"
    },
    "tumblr": {
      "status": "active"
    },
    "flickr": {
      "status": "inactive"
    }
  }
}
```

##Contacts
***

```javascript
{
    "serviceType": "twitter",
    "serviceId": 105133786,
    "nickname": "thisislorenz",
    "fullname": "Lorenz Aschoff",
    "thumbUrl": "http://a1.twimg.com/profile_images/632871017/me_normal.png"
}
```

Or with a matching user:

```javascript
{
    "serviceType": "twitter",
    "serviceId": 105133786,
    "nickname": "thisislorenz",
    "fullname": "Lorenz Aschoff",
    "thumbUrl": "http://a1.twimg.com/profile_images/632871017/me_normal.png",
    "user": {
      "id": "8203",
      "fullname": "Mac Gyver",
      "nickname": null,
      "thumbUrl": "",
      "isFriend": false
    }
}
```

##Location (sub-object attached to location-based albums at the moment)
***

The location object always contains at least latitude and longitude, and depending on the album type, further embedded objects: 
* venue: has a simple city album, simple country album and a venueService object
* city: has a simple country album
* country: only has latitude and longitude

```javascript
location:{
    "latitude": 52.5031436,
    "longitude": 13.40083313,
    "cityAlbum":{
       ... simple album object
     },
    "countryAlbum":{
       ... simple album object
     },
    "venueService":{
       ... venue service object (see below)
     }
}
```

##Venue service
***
Additional meta-data for venue albums

```javascript
venueService:{
    "name": "foursquare",
    "id": 123512oino1958123047235,
    "category": 1234nlu091235bnl1iy,
    "categoryName": "Tech Startup"
}
```


### Remarks:
* name: enum, for now either foursquare or eyeem. if foursquare, then the id and category are valid foursquare values
* id: the venue object's id (not the albumID), reflects either a valid foursquare id (can be used to query the FQ API) or an eyeem one.
* category and categoryName: only valid for foursquare venues, ids/names come from foursquare

##Collections
***
Collections are ad-hoc sets of photos that are related to each other, but not necessarily albums. For now, collections are primarily used in the discover feed.

#### Object Format
```javascript
{
  "collection": {
    "title": "Black and White photos in Berlin",
    "subtitle": "150 photos in this collection",
    "type": "album",
    "album": {
      "id": "17",
      "name": "Berlin",
      "thumbUrl": "http://www.eyeem.com/thumb/sq/200/5993d6f01a18a8fa6a3b13034ca1d8a1e7345edf-1321712288",
      "updated": "2012-02-03T18:06:08+0000"
    },
    "photos": {
      "offset": 0,
      "limit": 3,
      "total": 3,
      "items": [
        {
          "id": "216365",
          "thumbUrl": "http://www.eyeem.com/thumb/h/100/3ca2b83032785f475476e77d20f2c41e230ec7f7-1328292321",
          "photoUrl": "http://www.eyeem.com/thumb/640/480/3ca2b83032785f475476e77d20f2c41e230ec7f7-1328292321",
          "width": 1024,
          "height": 768,
          "updated": "2012-02-03T18:06:08+0000",
          "user": {
            "id": "4463",
            "fullname": "Fabian-Carlos Guhl",
            "nickname": null,
            "thumbUrl": "https://graph.facebook.com/536656083/picture?type=square"
          },
          "caption": "Discussing world peace at Oburger 69",
          "totalLikes": 0,
          "totalComments": 0
        },
        {
          "id": "216313",
          "thumbUrl": "http://www.eyeem.com/thumb/h/100/1ac3d29659fc7bcf65882d66a676bef4acc1ad22-1328290328",
          "photoUrl": "http://www.eyeem.com/thumb/640/480/1ac3d29659fc7bcf65882d66a676bef4acc1ad22-1328290328",
          "width": 1224,
          "height": 1632,
          "updated": "2012-02-03T17:33:07+0000",
          "user": {
            "id": "60534",
            "fullname": "666",
            "nickname": null,
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/b9101e64f89be9c65bb6f4d9ee1dee66f4d43ad1.jpg"
          },
          "caption": "table at Marietta",
          "totalLikes": 2,
          "totalComments": 0
        }
      ]
    },
  }
}
```
#### Remarks
* Collections can have the following type: `album`,`nearbyLive`,`popular`,`userFavorites`,`nearby`
* based on the type, collections can additionally contain a simple `album` or `user` object