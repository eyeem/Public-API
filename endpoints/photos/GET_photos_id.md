# GET /photos/#{id} 
***
`/photos/#{id}`

### Description
***
Retrieves a photo by id.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want to retrieve information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**includeComments**| If true, returns the latest two comments of a photo inline|boolean||0|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||0|
|**numComments**|the number of comments to include in the response|integer||2|
|**numLikers**|the number of likers to include in the response|integer||2|
|**includeAlbums**| If true, includes the albums this photo is part of|boolean||0|

### Response
***


200 and an a photo dictionary

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/photos/939584?detailed=1&includeAlbums=1&includeComments=1&numComment=5`

```javascript

{
  "photo": {
    "id": 939584,
    "thumbUrl": "http://www.eyeem.com/thumb/h/100/3e6683d12d88ac5c4b256fc01000181a0c24a9e4-1347402279",
    "photoUrl": "http://www.eyeem.com/thumb/640/480/3e6683d12d88ac5c4b256fc01000181a0c24a9e4-1347402279",
    "width": 1297,
    "height": 1297,
    "updated": "2012-09-12T00:24:52+0200",
    "webUrl": "http://www.eyeem.com/p/939584",
    "user": {
      "id": "85578",
      "nickname": "Jason",
      "fullname": "jasonmpeterson",
      "webUrl": "http://www.eyeem.com/u/Jason",
      "thumbUrl": "http://www.eyeem.com/thumb/sq/50/34250df54b171c0a3e7ff5b7b2baca9a6f91878c.jpg",
      "photoUrl": "http://www.eyeem.com/thumb/sq/200/34250df54b171c0a3e7ff5b7b2baca9a6f91878c.jpg"
    },
    "title": "",
    "caption": "blackandwhite at Bike Trail Lake Michigan",
    "latitude": 41.9135,
    "longitude": -87.622,
    "totalLikes": 53,
    "totalComments": 8,
    "comments": {
      "offset": 0,
      "limit": 5,
      "total": 8,
      "items": [
        {
          "id": 408870,
          "photoId": 939584,
          "message": "moody photograph--I like it!",
          "extendedMessage": "moody photograph--I like it!",
          "user": {
            "id": "1658",
            "nickname": "starrush",
            "fullname": "Star Rush",
            "webUrl": "http://www.eyeem.com/u/starrush",
            "thumbUrl": "https://graph.facebook.com/100000001240866/picture?type=square",
            "photoUrl": "https://graph.facebook.com/100000001240866/picture?type=large"
          },
          "mentionedUsers": [],
          "updated": "2012-09-12T21:11:03+0200"
        },
        {
          "id": 408594,
          "photoId": 939584,
          "message": "Congrats @Jason ! Your picture just got featured on "In 24 Pictures Around the World". Check it out on the EyeEm blog!",
          "extendedMessage": "Congrats [user:85578] ! Your picture just got featured on "In 24 Pictures Around the World". Check it out on the EyeEm blog!",
          "user": {
            "id": "5491",
            "nickname": "severin",
            "fullname": "Severin",
            "webUrl": "http://www.eyeem.com/u/severin",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/b9c94f9b2aaa2e0445816f21593035cdc997f53e.jpg",
            "photoUrl": "http://www.eyeem.com/thumb/sq/200/b9c94f9b2aaa2e0445816f21593035cdc997f53e.jpg"
          },
          "mentionedUsers": [
            {
              "id": "85578",
              "nickname": "Jason",
              "fullname": "jasonmpeterson",
              "webUrl": "http://www.eyeem.com/u/Jason",
              "thumbUrl": "http://www.eyeem.com/thumb/sq/50/34250df54b171c0a3e7ff5b7b2baca9a6f91878c.jpg",
              "photoUrl": "http://www.eyeem.com/thumb/sq/200/34250df54b171c0a3e7ff5b7b2baca9a6f91878c.jpg"
            }
          ],
          "updated": "2012-09-12T17:51:54+0200"
        },
        {
          "id": 408566,
          "photoId": 939584,
          "message": "woooow :-):-)",
          "extendedMessage": "woooow :-):-)",
          "user": {
            "id": "57442",
            "nickname": "david60439",
            "fullname": "David Oesterreicher",
            "webUrl": "http://www.eyeem.com/u/david60439",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/a02c018e582b054280466f97045e9fb35746f82f.jpg",
            "photoUrl": "http://www.eyeem.com/thumb/sq/200/a02c018e582b054280466f97045e9fb35746f82f.jpg"
          },
          "mentionedUsers": [],
          "updated": "2012-09-12T17:44:48+0200"
        },
        {
          "id": 407646,
          "photoId": 939584,
          "message": "gorgeous solitaire!",
          "extendedMessage": "gorgeous solitaire!",
          "user": {
            "id": "121943",
            "nickname": "yammay",
            "fullname": "yammay",
            "webUrl": "http://www.eyeem.com/u/yammay",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/3f4e7207826e012c99c9945c61621961975c317a.jpg",
            "photoUrl": "http://www.eyeem.com/thumb/sq/200/3f4e7207826e012c99c9945c61621961975c317a.jpg"
          },
          "mentionedUsers": [],
          "updated": "2012-09-12T06:24:46+0200"
        },
        {
          "id": 407596,
          "photoId": 939584,
          "message": "Love it.",
          "extendedMessage": "Love it.",
          "user": {
            "id": "75949",
            "nickname": "n_cruz",
            "fullname": "n_cruz",
            "webUrl": "http://www.eyeem.com/u/n_cruz",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/50/caf3628a3b53b94596dcee724a5eb142414e498f.jpg",
            "photoUrl": "http://www.eyeem.com/thumb/sq/200/caf3628a3b53b94596dcee724a5eb142414e498f.jpg"
          },
          "mentionedUsers": [],
          "updated": "2012-09-12T05:40:30+0200"
        }
      ]
    },
    "likers": {
      "offset": 0,
      "limit": 1,
      "total": 53,
      "items": [
        {
          "id": "3163",
          "nickname": "wiljonesjr",
          "fullname": "Wil Jones",
          "webUrl": "http://www.eyeem.com/u/wiljonesjr",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0b303096d5269a0c1560f6f410079edba00fa116.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/0b303096d5269a0c1560f6f410079edba00fa116.jpg"
        }
      ]
    },
    "albums": {
      "offset": 0,
      "limit": 5,
      "total": 5,
      "items": [
        {
          "id": "1702",
          "name": "United States",
          "type": "country",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/1762e9039140b7589e8371d471cc5191b2ba0630-1347618089",
          "updated": "2012-09-14T12:21:51+0200",
          "location": {
            "latitude": "37.13054",
            "longitude": "-113.50829"
          },
          "webUrl": "http://www.eyeem.com/a/1702",
          "totalPhotos": 58411,
          "totalLikers": 59,
          "totalContributors": 6624
        },
        {
          "id": "2364",
          "name": "Chicago",
          "type": "city",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/b50cc13c430f99d3f012558a624fde4b4b414931-1347596066",
          "updated": "2012-09-14T06:14:27+0200",
          "location": {
            "latitude": "41.85003",
            "longitude": "-87.65005",
            "countryAlbum": {
              "id": "1702",
              "name": "United States",
              "type": "country",
              "thumbUrl": "http://www.eyeem.com/thumb/sq/200/1762e9039140b7589e8371d471cc5191b2ba0630-1347618089",
              "updated": "2012-09-14T12:21:51+0200"
            }
          },
          "webUrl": "http://www.eyeem.com/a/2364",
          "totalPhotos": 1565,
          "totalLikers": 58,
          "totalContributors": 181
        },
        {
          "id": "242549",
          "name": "Bike Trail Lake Michigan",
          "type": "venue",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/3e6683d12d88ac5c4b256fc01000181a0c24a9e4-1347402279",
          "updated": "2012-09-12T00:24:52+0200",
          "location": {
            "latitude": "41.91158676",
            "longitude": "-87.62506866",
            "cityAlbum": {
              "id": "2364",
              "name": "Chicago",
              "type": "city",
              "thumbUrl": "http://www.eyeem.com/thumb/sq/200/b50cc13c430f99d3f012558a624fde4b4b414931-1347596066",
              "updated": "2012-09-14T06:14:27+0200"
            },
            "countryAlbum": {
              "id": "1702",
              "name": "United States",
              "type": "country",
              "thumbUrl": "http://www.eyeem.com/thumb/sq/200/1762e9039140b7589e8371d471cc5191b2ba0630-1347618089",
              "updated": "2012-09-14T12:21:51+0200"
            },
            "venueService": {
              "name": "foursquare",
              "id": "4bdaf88d63c5c9b6b9aa2568",
              "category": "4bf58dd8d48988d159941735",
              "categoryName": "Hiking Trail"
            }
          },
          "webUrl": "http://www.eyeem.com/a/242549",
          "totalPhotos": 4,
          "totalLikers": 0,
          "totalContributors": 1
        },
        {
          "id": "4454",
          "name": "blackandwhite",
          "type": "tag",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/200/a98feaa594040ad24f4f3616d16e8f6c96ea16d5-1347618315",
          "updated": "2012-09-14T12:25:23+0200",
          "webUrl": "http://www.eyeem.com/a/4454",
          "totalPhotos": 53948,
          "totalLikers": 90352,
          "totalContributors": 4144
        }
      ]
    }
  }
}

```