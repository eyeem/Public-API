# GET /photos/#{id}/comments/#{comment_id}   
***
`/photos/#{id}/comments/#{comment_id} `

### Description
***
Retrieves a specific comment on a photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want retrieve information about.|integer|x||
|**comment_id**|The id of the comment we want to retrieve.|integer|x||


### Response
***


200 and a comment object

[Errors](../../resources/errors.md#files)
### Examples
***

`https://api.eyeem.com/v2/photos/939584/comments/408870`

```json

{
  "comment": {
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
  }
}

```
 