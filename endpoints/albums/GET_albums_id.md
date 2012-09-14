../../# GET /albums/#{id}
***
`/albums/#{id}`

### Description
***
Retrieves album specified in the id URL query parameter.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**detailed**|returns a simple or detailed album object|boolean||1|
|**includePhotos**|if true it returns some of the album's photos|boolean||0|
|**numPhotos**|the number of album photos to return|integer||10|
|**photoDetails**|whether to return the photo details (comments, likes, albums)|boolean||0|
|**includeContributors**|if true, returns the album contributors|boolean| |0|
|**includeLikers**| if true, returns the album likers|boolean| |0|




### Response
***


200 and a dictionary containing the album object


[Errors](../../resources/errors.md#files)

### Examples
***

`http://www.eyeem.com/api/v2/albums/1234?`

```javascript

{
  "album": {
    "id": "1234",
    "name": "M41 Erkstraße",
    "type": "venue",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/200/4bc10409624629ebe33699ee8c00bd8b93539051-1333387979",
    "updated": "2012-04-02T17:33:11+0200",
    "location": {
      "latitude": "52.48172760",
      "longitude": "13.43966293",
      "cityAlbum": {
        "id": "17",
        "name": "Berlin",
        "type": "city",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/aced33f0969ffd6a64cb301fed92d9c52f18df81-1347618272",
        "updated": "2012-09-14T12:24:34+0200"
      },
      "countryAlbum": {
        "id": "23",
        "name": "Germany",
        "type": "country",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/aced33f0969ffd6a64cb301fed92d9c52f18df81-1347618272",
        "updated": "2012-09-14T12:24:34+0200"
      },
      "venueService": {
        "name": "foursquare",
        "id": "4d7f9c12dd4a6ea8d3eb7d25",
        "category": "4bf58dd8d48988d12b951735",
        "categoryName": "Bus Line"
      }
    },
    "webUrl": "http://www.eyeem.com/a/1234",
    "totalPhotos": 1,
    "totalLikers": 0,
    "totalContributors": 1
  }
}
```


 