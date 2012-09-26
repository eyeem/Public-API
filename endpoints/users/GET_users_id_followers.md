# GET /users/#{id}/followers  
***
`/users/#{id}/followers`

### Description
***
Get a user's followers.

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


200 and and a dictionary containing limit, offset, total and an array of followers (users)

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/me/friends/1015`


```javascript


{
  "followers": {
    "offset": 0,
    "limit": 20,
    "total": 659,
    "items": [
      {
        "id": 203125,
        "nickname": "eugenpirogoff",
        "fullname": "Eugen Pirogoff",
        "webUrl": "http://www.eyeem.com/u/eugenpirogoff",
        "thumbUrl": "https://graph.facebook.com/1380365540/picture?type=square",
        "photoUrl": "https://graph.facebook.com/1380365540/picture?type=large"
      },
      {
        "id": "194704",
        "nickname": "harry1960",
        "fullname": "Harry",
        "webUrl": "http://www.eyeem.com/u/harry1960",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/85ff80a14dd72508c99784dd81c1376756273a89-1347135446",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/85ff80a14dd72508c99784dd81c1376756273a89-1347135446"
      },
      {
        "id": "187453",
        "nickname": "JeanetteV",
        "fullname": "Jeanette",
        "webUrl": "http://www.eyeem.com/u/JeanetteV",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/cfd8c6e043b8c40933051233bbbb830a42d5a25a-1347525636",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/cfd8c6e043b8c40933051233bbbb830a42d5a25a-1347525636"
      },
      {
        "id": "195349",
        "nickname": "kamalmkhair",
        "fullname": "Ka Mal",
        "webUrl": "http://www.eyeem.com/u/kamalmkhair",
        "thumbUrl": "https://graph.facebook.com/100001703708572/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100001703708572/picture?type=large"
      },
      {
        "id": "4699",
        "nickname": "espen",
        "fullname": "Revesjef",
        "webUrl": "http://www.eyeem.com/u/espen",
        "thumbUrl": "https://graph.facebook.com/682221367/picture?type=square",
        "photoUrl": "https://graph.facebook.com/682221367/picture?type=large"
      },
      {
        "id": 200186,
        "nickname": "ShayTaylorReyes",
        "fullname": "Shay Reyes",
        "webUrl": "http://www.eyeem.com/u/ShayTaylorReyes",
        "thumbUrl": "https://graph.facebook.com/100000614053956/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100000614053956/picture?type=large"
      },
      {
        "id": "84943",
        "nickname": "beasterfield",
        "fullname": "Beasterfield",
        "webUrl": "http://www.eyeem.com/u/beasterfield",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/8f266e608bd1e34cc90f1cb16cc4daf36ac6e3fe.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/8f266e608bd1e34cc90f1cb16cc4daf36ac6e3fe.jpg"
      },
      {
        "id": "72",
        "nickname": "hany",
        "fullname": "Hany",
        "webUrl": "http://www.eyeem.com/u/hany",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/67e8399cf73fef815e496616f31b923b0f4f7aed.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/67e8399cf73fef815e496616f31b923b0f4f7aed.jpg"
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
        "id": "229",
        "nickname": "chikache",
        "fullname": "chika sato",
        "webUrl": "http://www.eyeem.com/u/chikache",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/36d3dcbe31f7e2a8a0016ddc570c3a487a6446be.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/36d3dcbe31f7e2a8a0016ddc570c3a487a6446be.jpg"
      },
      {
        "id": "238",
        "nickname": "lazylife",
        "fullname": "LaZyLiFe .",
        "webUrl": "http://www.eyeem.com/u/lazylife",
        "thumbUrl": "https://graph.facebook.com/100000573021736/picture?type=square",
        "photoUrl": "https://graph.facebook.com/100000573021736/picture?type=large"
      },
      {
        "id": "328",
        "nickname": "robertpaul",
        "fullname": "Robert-Paul Jansen",
        "webUrl": "http://www.eyeem.com/u/robertpaul",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/e11936ffad0f60c4e6c36a795d52e50bdf75be44.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/e11936ffad0f60c4e6c36a795d52e50bdf75be44.jpg"
      },
      {
        "id": "343",
        "nickname": "magneticart",
        "fullname": "Giovanni Savino",
        "webUrl": "http://www.eyeem.com/u/magneticart",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/828001f76579b4fa2bf183a9039b05cf1856417c.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/828001f76579b4fa2bf183a9039b05cf1856417c.jpg"
      },
      {
        "id": "440",
        "nickname": "mishobaranovic",
        "fullname": "Misho Baranovic",
        "webUrl": "http://www.eyeem.com/u/mishobaranovic",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/90e1f1e9e4b8e0c3f32be9194ab9f45f1aac240c.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/90e1f1e9e4b8e0c3f32be9194ab9f45f1aac240c.jpg"
      },
      {
        "id": "468",
        "nickname": "winkj",
        "fullname": "Johannes Winkelmann",
        "webUrl": "http://www.eyeem.com/u/winkj",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/6dcb2415de472ebe69b76a19df46cd9c00e838af.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/6dcb2415de472ebe69b76a19df46cd9c00e838af.jpg"
      },
      {
        "id": "504",
        "nickname": "marcoyuen",
        "fullname": "Marco Yuen",
        "webUrl": "http://www.eyeem.com/u/marcoyuen",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/7da12e5bd78876414a669c618e1547021de3f690.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/7da12e5bd78876414a669c618e1547021de3f690.jpg"
      },
      {
        "id": "547",
        "nickname": "DandiRomano",
        "fullname": "Dandi Romano",
        "webUrl": "http://www.eyeem.com/u/DandiRomano",
        "thumbUrl": "https://graph.facebook.com/575096087/picture?type=square",
        "photoUrl": "https://graph.facebook.com/575096087/picture?type=large"
      },
      {
        "id": "556",
        "nickname": "joanrbadasune",
        "fullname": "Joan Ramon Bada Suñe",
        "webUrl": "http://www.eyeem.com/u/joanrbadasune",
        "thumbUrl": "https://graph.facebook.com/1619946313/picture?type=square",
        "photoUrl": "https://graph.facebook.com/1619946313/picture?type=large"
      }
    ]
  }
}

```