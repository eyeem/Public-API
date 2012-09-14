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
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of photo objects


[Errors](../../resources/errors.md#files)
### Examples
***

`https://www.eyeem.com/api/v2/users/1013/friendsPhotos?limit=5`


```javascript


{
  "friendsPhotos": {
    "offset": 0,
    "limit": 5,
    "total": 112254,
    "items": [
      {
        "id": 950263,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/f0178db46c43a76647e776ce875cc6e324571fdc-1347618996",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/f0178db46c43a76647e776ce875cc6e324571fdc-1347618996",
        "width": 1296,
        "height": 972,
        "updated": "2012-09-14T12:36:37+0200",
        "webUrl": "http://www.eyeem.com/p/950263",
        "user": {
          "id": "12153",
          "nickname": "napetschnigalex",
          "fullname": "Alex Napetschnig",
          "webUrl": "http://www.eyeem.com/u/napetschnigalex",
          "thumbUrl": "https://graph.facebook.com/615795156/picture?type=square",
          "photoUrl": "https://graph.facebook.com/615795156/picture?type=large"
        },
        "title": "",
        "caption": "klash at Godshot",
        "latitude": 52.533,
        "longitude": 13.423,
        "totalLikes": 0,
        "totalComments": 0,
        "comments": {
          "offset": 0,
          "limit": 2,
          "total": 0,
          "items": []
        },
        "likers": {
          "offset": 0,
          "limit": 1,
          "total": 0,
          "items": []
        }
      },
      {
        "id": 950218,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/54b8b56dab5138fe6560f0189e29724e5e27b46d-1347617876",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/54b8b56dab5138fe6560f0189e29724e5e27b46d-1347617876",
        "width": 968,
        "height": 1296,
        "updated": "2012-09-14T12:18:42+0200",
        "webUrl": "http://www.eyeem.com/p/950218",
        "user": {
          "id": "1923",
          "nickname": "stephenmohammed",
          "fullname": "Stephen Mohammed",
          "webUrl": "http://www.eyeem.com/u/stephenmohammed",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/6c2ed71e4b520ce3a0ef722c2bf52a1a79f06e29.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/6c2ed71e4b520ce3a0ef722c2bf52a1a79f06e29.jpg"
        },
        "title": "",
        "caption": "Finding Treasure at Playa El Arenal",
        "latitude": 38.772833333333,
        "longitude": 0.18966666666667,
        "totalLikes": 0,
        "totalComments": 0,
        "comments": {
          "offset": 0,
          "limit": 2,
          "total": 0,
          "items": []
        },
        "likers": {
          "offset": 0,
          "limit": 1,
          "total": 0,
          "items": []
        }
      },
      {
        "id": 950212,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/b31e06ec1e8f5c7863ef61a8777794b87e8d9a76-1347617799",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/b31e06ec1e8f5c7863ef61a8777794b87e8d9a76-1347617799",
        "width": 968,
        "height": 1296,
        "updated": "2012-09-14T12:16:47+0200",
        "webUrl": "http://www.eyeem.com/p/950212",
        "user": {
          "id": "1923",
          "nickname": "stephenmohammed",
          "fullname": "Stephen Mohammed",
          "webUrl": "http://www.eyeem.com/u/stephenmohammed",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/6c2ed71e4b520ce3a0ef722c2bf52a1a79f06e29.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/6c2ed71e4b520ce3a0ef722c2bf52a1a79f06e29.jpg"
        },
        "title": "",
        "caption": "Being a beach bum at Playa El Arenal",
        "latitude": 38.772833333333,
        "longitude": 0.18966666666667,
        "totalLikes": 0,
        "totalComments": 0,
        "comments": {
          "offset": 0,
          "limit": 2,
          "total": 0,
          "items": []
        },
        "likers": {
          "offset": 0,
          "limit": 1,
          "total": 0,
          "items": []
        }
      },
      {
        "id": 950208,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/54ee9a9dfc0857e2326194f4dd249bc83fe7b5d4-1347617711",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/54ee9a9dfc0857e2326194f4dd249bc83fe7b5d4-1347617711",
        "width": 968,
        "height": 1296,
        "updated": "2012-09-14T12:15:35+0200",
        "webUrl": "http://www.eyeem.com/p/950208",
        "user": {
          "id": "1923",
          "nickname": "stephenmohammed",
          "fullname": "Stephen Mohammed",
          "webUrl": "http://www.eyeem.com/u/stephenmohammed",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/6c2ed71e4b520ce3a0ef722c2bf52a1a79f06e29.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/6c2ed71e4b520ce3a0ef722c2bf52a1a79f06e29.jpg"
        },
        "title": "",
        "caption": "Finding Treasure at Playa El Arenal",
        "latitude": 38.772666666667,
        "longitude": 0.18966666666667,
        "totalLikes": 0,
        "totalComments": 0,
        "comments": {
          "offset": 0,
          "limit": 2,
          "total": 0,
          "items": []
        },
        "likers": {
          "offset": 0,
          "limit": 1,
          "total": 0,
          "items": []
        }
      },
      {
        "id": 950180,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/9f786ef0b2dd0a15a05fe8127e9b083c2a60c94c-1347616838",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/9f786ef0b2dd0a15a05fe8127e9b083c2a60c94c-1347616838",
        "width": 1024,
        "height": 768,
        "updated": "2012-09-14T12:01:29+0200",
        "webUrl": "http://www.eyeem.com/p/950180",
        "user": {
          "id": "194704",
          "nickname": "harry1960",
          "fullname": "Harry",
          "webUrl": "http://www.eyeem.com/u/harry1960",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/85ff80a14dd72508c99784dd81c1376756273a89-1347135446",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/85ff80a14dd72508c99784dd81c1376756273a89-1347135446"
        },
        "title": "",
        "caption": "Relaxing at ATU Auto Teile Unger",
        "latitude": 52.594806098677,
        "longitude": 13.285423341643,
        "totalLikes": 0,
        "totalComments": 0,
        "comments": {
          "offset": 0,
          "limit": 2,
          "total": 0,
          "items": []
        },
        "likers": {
          "offset": 0,
          "limit": 1,
          "total": 0,
          "items": []
        }
      }
    ]
  }
}

```