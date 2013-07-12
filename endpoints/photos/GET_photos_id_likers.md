# GET /photos/#{id}/likers 
***
`/photos/#{id}/likers `

### Description
***
Retrieves an array of the users who like the photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of users to return|integer||20|
|**offset**|offset of users to start at|integer||0|
|**onlyId**| if true, returns only the likers ids|boolean|||



### Response
***


200 and and a dictionary containing limit, offset, total and an array of likers (users)

[Errors](../../resources/errors.md#files)
### Examples
***

`https://www.eyeem.com/api/v2/photos/939584/likers?offset=0&limit=5`

```json

{
  "likers": {
    "offset": 0,
    "limit": 5,
    "total": 53,
    "items": [
      {
        "id": "3163",
        "nickname": "wiljonesjr",
        "fullname": "Wil Jones",
        "webUrl": "http://www.eyeem.com/u/wiljonesjr",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/0b303096d5269a0c1560f6f410079edba00fa116.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/0b303096d5269a0c1560f6f410079edba00fa116.jpg"
      },
      {
        "id": "137287",
        "nickname": "binks",
        "fullname": "binks702",
        "webUrl": "http://www.eyeem.com/u/binks",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/68111e223275930ea366d080830e01ae552a582e-1347147322",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/68111e223275930ea366d080830e01ae552a582e-1347147322"
      },
      {
        "id": "126415",
        "nickname": "paulineabril",
        "fullname": "Pauline_",
        "webUrl": "http://www.eyeem.com/u/paulineabril",
        "thumbUrl": "https://graph.facebook.com/1524195517/picture?type=square",
        "photoUrl": "https://graph.facebook.com/1524195517/picture?type=large"
      },
      {
        "id": "87074",
        "nickname": "DCR",
        "fullname": "Dana",
        "webUrl": "http://www.eyeem.com/u/DCR",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/afc8aa7cd675f2c55adcbdd8b019e26c8c2aab40-1347124196",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/afc8aa7cd675f2c55adcbdd8b019e26c8c2aab40-1347124196"
      },
      {
        "id": "133614",
        "nickname": "klacsamana",
        "fullname": "Oceanbreeze",
        "webUrl": "http://www.eyeem.com/u/klacsamana",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/cce8a991ec0603ed323b1379fd58ba53f387de10.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/cce8a991ec0603ed323b1379fd58ba53f387de10.jpg"
      }
    ]
  }
}

```


