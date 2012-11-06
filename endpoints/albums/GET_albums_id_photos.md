# GET /albums/#{id}/photos
***
`/albums/#{id}/photos`

### Description
***
Retrieves photos of an album specified in the id URL query parameter.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of photos to return|integer||20|
|**offset**|(offset of photos to start at|integer||0|
|**onlyId**|if true, returns only the photo ids|boolean||0|
|**detailed**|returns a simple or detailed photo object|boolean||0|
|**includeComments**|If true, returns the latest two comments of a photo inline|boolean||0|
|**includeLikers**|If true, returns the latest two likers of a photo|boolean||0|
|**numComments**|the number of comments to include in the response|integer||2|
|**numLikers**|the number of likers to include in the response|integer||2|
|**includeAlbums**|If true, includes the albums this photo is part of|boolean||0|



### Response
***


200 and and a dictionary containing limit, offset, total and an array of photos


[Errors](../../resources/errors.md#files)

### Examples
***

`http://www.eyeem.com/api/v2/albums/12/photos?offset=0&limit=5`


```json
{
  "photos": {
    "offset": 0,
    "limit": 5,
    "total": 19,
    "items": [
      {
        "id": "56167",
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/6a59c1597178c55ca1cf6fe9e5a0056958eab8f1-1302692235",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/6a59c1597178c55ca1cf6fe9e5a0056958eab8f1-1302692235",
        "width": 864,
        "height": 640,
        "updated": "2011-04-13T12:57:46+0200"
      },
      {
        "id": "56166",
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/74f586ac6e4f7a711d3d7c17a954ad362e464578-1302692207",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/74f586ac6e4f7a711d3d7c17a954ad362e464578-1302692207",
        "width": 864,
        "height": 640,
        "updated": "2011-04-13T12:56:55+0200"
      },
      {
        "id": "56165",
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/8491863745c57723bfaa9419e00aafdd04c213d9-1302692115",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/8491863745c57723bfaa9419e00aafdd04c213d9-1302692115",
        "width": 2048,
        "height": 1530,
        "updated": "2011-04-13T12:55:58+0200"
      },
      {
        "id": "56164",
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/e9341d43b55d2ec7a3d537c816ec9d0881d63df9-1302692132",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/e9341d43b55d2ec7a3d537c816ec9d0881d63df9-1302692132",
        "width": 864,
        "height": 640,
        "updated": "2011-04-13T12:55:40+0200"
      },
      {
        "id": "56163",
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/7ea5fccdee012da92c5c54d42b177139c84742d5-1302692061",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/7ea5fccdee012da92c5c54d42b177139c84742d5-1302692061",
        "width": 864,
        "height": 640,
        "updated": "2011-04-13T12:54:29+0200"
      }
    ]
  }
}

```

 