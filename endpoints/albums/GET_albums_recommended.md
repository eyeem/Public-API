# GET /albums/recommended
***
`/albums/recommended`

### Description
***
Retrieves albums recommended by the EyeEm community team.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of albums to return|integer||60|



### Response
***

200 and an array of album objects, includes pagination parameters


[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/albums/recommended?limit=10`

```json

{
  "albums": {
    "offset": 0,
    "limit": 10,
    "total": 21,
    "items": [
      {
        "id": "44210",
        "name": "sport",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/6b4bb761d9bee3c02df4b5d8eb9de32ed204aa5f-1347541313",
        "updated": "2012-09-13T15:04:42+0200",
        "webUrl": "http://www.eyeem.com/a/44210",
        "totalPhotos": 309,
        "totalLikers": 2802,
        "totalContributors": 215
      },
      {
        "id": "11500",
        "name": "portrait",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/134a48ca239fd049bcd3ed48bebecedde0529460-1347615574",
        "updated": "2012-09-14T11:39:41+0200",
        "webUrl": "http://www.eyeem.com/a/11500",
        "totalPhotos": 4157,
        "totalLikers": 6187,
        "totalContributors": 1228
      },
      {
        "id": "1419",
        "name": "London",
        "type": "city",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/665d3ae8e8b6c1e72552a2b97fa448b98c7fb0a3-1347391091",
        "updated": "2012-09-11T21:18:30+0200",
        "location": {
          "latitude": "51.51279",
          "longitude": "-0.09184",
          "countryAlbum": {
            "id": "6318",
            "name": "United Kingdom",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/31dd34fb84553fb36a86596a26747bda896108a3-1347615666",
            "updated": "2012-09-14T11:41:13+0200"
          }
        },
        "webUrl": "http://www.eyeem.com/a/1419",
        "totalPhotos": 3981,
        "totalLikers": 3653,
        "totalContributors": 637
      },
      {
        "id": "12212",
        "name": "Signs",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/a7dfa0cc4b5fc40a13faa9c16c06dff95e235bcd-1347616281",
        "updated": "2012-09-14T11:51:44+0200",
        "webUrl": "http://www.eyeem.com/a/12212",
        "totalPhotos": 1476,
        "totalLikers": 5795,
        "totalContributors": 730
      },
      {
        "id": "5093",
        "name": "art",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/819a483a14483b080f30f33196b005240e53cd04-1347606916",
        "updated": "2012-09-14T09:15:22+0200",
        "webUrl": "http://www.eyeem.com/a/5093",
        "totalPhotos": 1570,
        "totalLikers": 4688,
        "totalContributors": 708
      },
      {
        "id": "25670",
        "name": "Japan",
        "type": "country",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/a7dfa0cc4b5fc40a13faa9c16c06dff95e235bcd-1347616281",
        "updated": "2012-09-14T12:01:50+0200",
        "location": {
          "latitude": "35.6895",
          "longitude": "139.69171"
        },
        "webUrl": "http://www.eyeem.com/a/25670",
        "totalPhotos": 14613,
        "totalLikers": 2646,
        "totalContributors": 1095
      },
      {
        "id": "11316",
        "name": "Cooking",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/27e51ef64fdb7e0986b141298191169dd9eab2b3-1347542112",
        "updated": "2012-09-13T15:16:06+0200",
        "webUrl": "http://www.eyeem.com/a/11316",
        "totalPhotos": 936,
        "totalLikers": 4562,
        "totalContributors": 499
      },
      {
        "id": "717",
        "name": "Moscow",
        "type": "city",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/21c7f2e6d445455c6323e9cdb6c1d52d4ac28543-1347605000",
        "updated": "2012-09-14T08:43:29+0200",
        "location": {
          "latitude": "55.75222",
          "longitude": "37.61556",
          "countryAlbum": {
            "id": "32954",
            "name": "Russia",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/8bc09d19e88fb04119bb35d0f9fddd1fb1bd15e0-1347617828",
            "updated": "2012-09-14T12:17:15+0200"
          }
        },
        "webUrl": "http://www.eyeem.com/a/717",
        "totalPhotos": 1294,
        "totalLikers": 1931,
        "totalContributors": 289
      },
      {
        "id": "4454",
        "name": "blackandwhite",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/7cf206d58f1e5b2a58c76464e5c719d376bb280d-1347616822",
        "updated": "2012-09-14T12:00:32+0200",
        "webUrl": "http://www.eyeem.com/a/4454",
        "totalPhotos": 53947,
        "totalLikers": 90352,
        "totalContributors": 4144
      },
      {
        "id": "51",
        "name": "Coffee",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/bcbcb34a1057f940e9cad627c44b0de19d747bee-1347617796",
        "updated": "2012-09-14T12:16:39+0200",
        "webUrl": "http://www.eyeem.com/a/51",
        "totalPhotos": 3035,
        "totalLikers": 4989,
        "totalContributors": 1624
      }
    ]
  }
}
```



 