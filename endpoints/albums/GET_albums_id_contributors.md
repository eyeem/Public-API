# GET /albums/#{id}/contributors 
***
`/albums/#{id}/contributors`

### Description
***
Retrieves an array of the users who have added photos to the album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of contributors to return|integer||20|
|**offset**|offset of contributors to start at|integer||0|
|**onlyId**|if true, returns only the user id|boolean||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of contributors (users)


[Errors](../../resources/errors.md#files)
### Examples
***

`http://www.eyeem.com/api/v2/albums/1234/contributors?offset=0&limit=5`

```javascript


{
  "contributors": {
    "offset": 0,
    "limit": 5,
    "total": 2127,
    "items": [
      {
        "id": "1015",
        "nickname": "Gen",
        "fullname": "Gen Sadakane",
        "webUrl": "http://www.eyeem.com/u/Gen",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/f39a693bdc2f09a8af61ecf003e448e8482755a8.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/f39a693bdc2f09a8af61ecf003e448e8482755a8.jpg",
        "totalPhotosContributed": 1652,
        "latestContribution": "2012-09-13T20:44:52+0200"
      },
      {
        "id": "24961",
        "nickname": "steph",
        "fullname": "Stephanie",
        "webUrl": "http://www.eyeem.com/u/steph",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/8cd6ad61c04d891321decc446dcf7c1ff36eb631.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/8cd6ad61c04d891321decc446dcf7c1ff36eb631.jpg",
        "totalPhotosContributed": 1474,
        "latestContribution": "2012-09-13T15:59:02+0200"
      },
      {
        "id": "1013",
        "nickname": "ramz",
        "fullname": "ramz",
        "webUrl": "http://www.eyeem.com/u/ramz",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg",
        "totalPhotosContributed": 1008,
        "latestContribution": "2012-09-13T22:27:31+0200"
      },
      {
        "id": "5491",
        "nickname": "severin",
        "fullname": "Severin",
        "webUrl": "http://www.eyeem.com/u/severin",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/b9c94f9b2aaa2e0445816f21593035cdc997f53e.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/b9c94f9b2aaa2e0445816f21593035cdc997f53e.jpg",
        "totalPhotosContributed": 838,
        "latestContribution": "2012-09-14T11:52:45+0200"
      },
      {
        "id": "4962",
        "nickname": "sarahweinknecht",
        "fullname": "Sarah Weinknecht",
        "webUrl": "http://www.eyeem.com/u/sarahweinknecht",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/50/abb52a61123224887b42ac49c4f4cda6a1cf3fbf.jpg",
        "photoUrl": "http://www.eyeem.com/thumb/sq/200/abb52a61123224887b42ac49c4f4cda6a1cf3fbf.jpg",
        "totalPhotosContributed": 643,
        "latestContribution": "2012-09-07T01:49:52+0200"
      }
    ]
  }
}

```


 