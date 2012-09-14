# GET /photos/#{id}/comments  
***
`/photos/#{id}/comments`

### Description
***
Retrieves an array of a photo's comments.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of comments to return|integer||20|
|**offset**|offset of comments to start at|integer||0|
|**onlyId**|if true, returns a comma separated list of comment ids|boolean||0|

### Response
***


200 and and a dictionary containing limit, offset, total and an array of comments

[Errors](../../resources/errors.md#files)
### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/comments?offset=0&limit=5`

```javascript

{
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
  }
}

```

 