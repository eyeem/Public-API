# GET /albums/#{id}/contributors/#{user_id} 
***
`/albums/#{id}/contributors/#{user_id}`

### Description
***
Checks whether a user has contributed a photo to the album.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**user_id**| The id of the user|integer|x||

### Response
***


200 if the user has contributed a photo to the album, 404 otherwise


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/albums/17/contributors/1013`


```json


{
  "message": "User has contributed to album.",
  "contributed": true,
  "user": {
    "id": "1013",
    "nickname": "ramz",
    "fullname": "ramz",
    "webUrl": "http://www.eyeem.com/u/ramz",
    "thumbUrl": "http://cdn.eyeem.com/thumb/sq/50/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg",
    "photoUrl": "http://cdn.eyeem.com/thumb/sq/200/7c0ff01c33815d65840b1ff9c849786898bad7d4.jpg",
    "totalPhotosContributed": 1008,
    "latestContribution": "2012-09-13T22:27:31+0200"
  }
}

```
 