# GET /search    
***
`/search`

### Description
***
Retrieves an array containing a users and an albums dictionary.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|the keyword to search|string|x||
|**includeAlbums**| whether to include results in the albums dictionary|boolean|x||
|**includeUsers**|whether to include results in the users dictionary|boolean|x||

### Response
***


200 and an array containing a users dictionary and an albums dictionary.


[Errors](../../resources/errors.md#files)

### Examples
***

`http://www.eyeem.com/api/v2/search?q=berlin&includeAlbums=1`

```javascript


{
  "totalAlbums": 1352,
  "albums": {
    "offset": 0,
    "limit": 10,
    "total": 1352,
    "items": [
      {
        "id": "17",
        "name": "Berlin",
        "type": "city",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
        "updated": "2012-09-14T12:56:01+0200",
        "location": {
          "latitude": "52.52437",
          "longitude": "13.41053",
          "countryAlbum": {
            "id": "23",
            "name": "Germany",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          }
        },
        "webUrl": "http://www.eyeem.com/a/17",
        "totalPhotos": 34251,
        "totalLikers": 3114,
        "totalContributors": 2127
      },
      {
        "id": "626",
        "name": "Berlin",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/39843d26436fa1e4bac5768f566f809a651ba28c-1347616663",
        "updated": "2012-09-14T11:58:00+0200",
        "webUrl": "http://www.eyeem.com/a/626",
        "totalPhotos": 887,
        "totalLikers": 29,
        "totalContributors": 220
      },
      {
        "id": "378520",
        "name": "EyeEm Berlin Meetup",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/fd5c86ba46e49b470ba50f5c1430e2d2d3d965e7-1344709646",
        "updated": "2012-08-31T20:38:46+0200",
        "webUrl": "http://www.eyeem.com/a/378520",
        "totalPhotos": 276,
        "totalLikers": 16,
        "totalContributors": 41
      },
      {
        "id": "368520",
        "name": "Berlin Wilmersdorf",
        "type": "city",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/61d0e17b9d98071af36b5d0b4812bbc89324b535-1347608390",
        "updated": "2012-09-14T09:40:56+0200",
        "location": {
          "latitude": "52.50097",
          "longitude": "13.29097",
          "countryAlbum": {
            "id": "23",
            "name": "Germany",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          }
        },
        "webUrl": "http://www.eyeem.com/a/368520",
        "totalPhotos": 167,
        "totalLikers": 1,
        "totalContributors": 66
      },
      {
        "id": "30201",
        "name": "Berlin Festival 2011",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/21d270cd4b6dfaec756c00c4d9873bef700c2068-1315831129",
        "updated": "2012-06-01T00:30:53+0200",
        "location": {
          "latitude": "52.48030090",
          "longitude": "13.39051437",
          "cityAlbum": {
            "id": "17",
            "name": "Berlin",
            "type": "city",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          },
          "countryAlbum": {
            "id": "23",
            "name": "Germany",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          },
          "venueService": {
            "name": "foursquare",
            "id": "4e665b43aeb736031693a6e9",
            "category": "4bf58dd8d48988d1e6931735",
            "categoryName": "Concert Hall"
          }
        },
        "webUrl": "http://www.eyeem.com/a/30201",
        "totalPhotos": 160,
        "totalLikers": 6,
        "totalContributors": 11
      },
      {
        "id": "409410",
        "name": "Startupbootcamp Berlin 2012",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/625c914e5d778e2131a20401614ae8bd50442100-1347611567",
        "updated": "2012-09-14T10:33:00+0200",
        "webUrl": "http://www.eyeem.com/a/409410",
        "totalPhotos": 135,
        "totalLikers": 11,
        "totalContributors": 10
      },
      {
        "id": "355",
        "name": "Berlin Tegel Airport (TXL)",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/4e13e714b10ec3b9db5a4df17f68fb8590623251-1347612087",
        "updated": "2012-09-14T10:42:33+0200",
        "location": {
          "latitude": "52.55437088",
          "longitude": "13.29028130",
          "cityAlbum": {
            "id": "17",
            "name": "Berlin",
            "type": "city",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          },
          "countryAlbum": {
            "id": "23",
            "name": "Germany",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          },
          "venueService": {
            "name": "foursquare",
            "id": "4adcda92f964a520f14b21e3",
            "category": "4bf58dd8d48988d1ed931735",
            "categoryName": "Airport"
          }
        },
        "webUrl": "http://www.eyeem.com/a/355",
        "totalPhotos": 132,
        "totalLikers": 10,
        "totalContributors": 55
      },
      {
        "id": "1",
        "name": "Berlin Award 2010",
        "type": "special",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/1274143464Kill_da_Wabbit.JPG",
        "updated": "2012-05-07T12:13:32+0200",
        "webUrl": "http://www.eyeem.com/a/1",
        "totalPhotos": 117,
        "totalLikers": 4,
        "totalContributors": 98
      },
      {
        "id": "352",
        "name": "Berlin Hauptbahnhof",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/7bb407e8e39b9e82ed67bf67f5c6453a1ddff9e8-1347417088",
        "updated": "2012-09-12T04:31:31+0200",
        "location": {
          "latitude": "52.52515030",
          "longitude": "13.36928844",
          "cityAlbum": {
            "id": "17",
            "name": "Berlin",
            "type": "city",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          },
          "countryAlbum": {
            "id": "23",
            "name": "Germany",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2d08ade2c4553c67f7a7a00a58f34cfb0957f094-1347620145",
            "updated": "2012-09-14T12:56:01+0200"
          },
          "venueService": {
            "name": "foursquare",
            "id": "4a1c8506f964a520457b1fe3",
            "category": "4bf58dd8d48988d129951735",
            "categoryName": "Train Station"
          }
        },
        "webUrl": "http://www.eyeem.com/a/352",
        "totalPhotos": 114,
        "totalLikers": 5,
        "totalContributors": 52
      }
    ]
  },
  "totalUsers": 109,
  "users": {
    "offset": 0,
    "limit": 10,
    "total": 109
  }
}

```
