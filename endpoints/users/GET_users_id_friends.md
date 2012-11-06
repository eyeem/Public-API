# GET /users/#{id}/friends 
***
`/users/#{id}/friends`

### Description
***
Get a user's friends (users that they follow)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of users to return|integer||20|
|**offset**|offset of users to start at|integer||0|
|**onlyId**|returns a json array userIds containing just the ids|boolean|||
|**detailed**|returns the details for every user >> num photos, num followers, etc|boolean||0|

### Response
***

200 and and a dictionary containing limit, offset, total and an array of friends (users)


[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013/friends`

```json


{
  "friends": {
    "offset": 0,
    "limit": 20,
    "total": 869,
    "items": [
      {
        "id": "194704",
        "nickname": "harry1960",
        "fullname": "Harry",
        "webUrl": "http://www.eyeem.com/u/harry1960",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/85ff80a14dd72508c99784dd81c1376756273a89-1347135446",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/85ff80a14dd72508c99784dd81c1376756273a89-1347135446"
      },
      {
        "id": 201141,
        "nickname": "sarinafoto",
        "fullname": "Sarina",
        "webUrl": "http://www.eyeem.com/u/sarinafoto",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/70ac4f4e826b231c6c2a6a9bc6506918d81b6b2c-1347472150",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/70ac4f4e826b231c6c2a6a9bc6506918d81b6b2c-1347472150"
      },
      {
        "id": 200139,
        "nickname": "antoinettehabbouche",
        "fullname": "Antoinette Habbouche",
        "webUrl": "http://www.eyeem.com/u/antoinettehabbouche",
        "thumbUrl": "https://graph.facebook.com/100000183436279/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100000183436279/picture?type=large"
      },
      {
        "id": 200200,
        "nickname": "MurrNadim",
        "fullname": "Nadim Murr",
        "webUrl": "http://www.eyeem.com/u/MurrNadim",
        "thumbUrl": "https://graph.facebook.com/750410701/picture?type=square",
        "photoUrl": "https://graph.facebook.com/750410701/picture?type=large"
      },
      {
        "id": 199337,
        "nickname": "fabiendamien",
        "fullname": "Fabien Damien",
        "webUrl": "http://www.eyeem.com/u/fabiendamien",
        "thumbUrl": "https://graph.facebook.com/803120507/picture?type=square",
        "photoUrl": "https://graph.facebook.com/803120507/picture?type=large"
      },
      {
        "id": "64",
        "nickname": "DixonHamby",
        "fullname": "Dixon Hamby",
        "webUrl": "http://www.eyeem.com/u/DixonHamby",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/9ad11f78ec0abf253a338f9fdf5d1a5c65fdede2.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/9ad11f78ec0abf253a338f9fdf5d1a5c65fdede2.jpg"
      },
      {
        "id": "82",
        "nickname": "RichardClarke",
        "fullname": "Richard Clarke",
        "webUrl": "http://www.eyeem.com/u/RichardClarke",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg"
      },
      {
        "id": "105",
        "nickname": "hyrizk",
        "fullname": "Hikmat Rizk",
        "webUrl": "http://www.eyeem.com/u/hyrizk",
        "thumbUrl": "https://graph.facebook.com/100000312838226/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100000312838226/picture?type=large"
      },
      {
        "id": "108",
        "nickname": "iphonegrapher",
        "fullname": "iphonegraher",
        "webUrl": "http://www.eyeem.com/u/iphonegrapher",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/56314a2b03929a746ecdeec3e0f92275b53fca20.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/56314a2b03929a746ecdeec3e0f92275b53fca20.jpg"
      },
      {
        "id": "110",
        "nickname": "YvesTimmermans",
        "fullname": "Yves Timmermans",
        "webUrl": "http://www.eyeem.com/u/YvesTimmermans",
        "thumbUrl": "https://graph.facebook.com/100001798858119/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100001798858119/picture?type=large"
      },
      {
        "id": "111",
        "nickname": "FionaConrad",
        "fullname": "Fiona Conrad",
        "webUrl": "http://www.eyeem.com/u/FionaConrad",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg"
      },
      {
        "id": "115",
        "nickname": "AndyC",
        "fullname": "Andy Chapman",
        "webUrl": "http://www.eyeem.com/u/AndyC",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg"
      },
      {
        "id": "123",
        "nickname": "romankeller",
        "fullname": "Roman Keller",
        "webUrl": "http://www.eyeem.com/u/romankeller",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/42f41c6ce2050d900771c734e49686cface66e96.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/42f41c6ce2050d900771c734e49686cface66e96.jpg"
      },
      {
        "id": "124",
        "nickname": "StephanieChappe",
        "fullname": "Stephanie Chappe",
        "webUrl": "http://www.eyeem.com/u/StephanieChappe",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg"
      },
      {
        "id": "142",
        "nickname": "SuzanMikiel",
        "fullname": "Suzan Mikiel",
        "webUrl": "http://www.eyeem.com/u/SuzanMikiel",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/7eb08e73653b9f017cfcb699c2b9d0a89cb8dfef.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/7eb08e73653b9f017cfcb699c2b9d0a89cb8dfef.jpg"
      },
      {
        "id": "148",
        "nickname": "arch",
        "fullname": "ARCH @iPhone",
        "webUrl": "http://www.eyeem.com/u/arch",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/8d4c75e1760b1af153d5192c8b9321f012d1957f.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/8d4c75e1760b1af153d5192c8b9321f012d1957f.jpg"
      },
      {
        "id": "162",
        "nickname": "caitlinwinner1",
        "fullname": "caitlin winner",
        "webUrl": "http://www.eyeem.com/u/caitlinwinner1",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/default_profile.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/default_profile.jpg"
      },
      {
        "id": "206",
        "nickname": "ira",
        "fullname": "Ira Aikman",
        "webUrl": "http://www.eyeem.com/u/ira",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/9c24eab725f8aa03b99c396dd4d45f2b9b450b90.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/9c24eab725f8aa03b99c396dd4d45f2b9b450b90.jpg"
      },
      {
        "id": "213",
        "nickname": "SamCornwell",
        "fullname": "Sam Cornwell",
        "webUrl": "http://www.eyeem.com/u/SamCornwell",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/068401355dbca9fa00bf4ccd83370fbeeca1c54f.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/068401355dbca9fa00bf4ccd83370fbeeca1c54f.jpg"
      },
      {
        "id": "215",
        "nickname": "MissPixels",
        "fullname": "MissPixels",
        "webUrl": "http://www.eyeem.com/u/MissPixels",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/6f84bb282d9d69d4444377593b90f59e0ee5c809.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/6f84bb282d9d69d4444377593b90f59e0ee5c809.jpg"
      }
    ]
  }


``