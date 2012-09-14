# GET /albums
***
`/albums`

### Description
***
Retrieves albums specified in the id URL query parameter, or searches for albums based on their names.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|a comma-separated list of album ids to retrieve|string|||
|**q**|search albums by (renders the ids parameter invalid)|string|||
|**trending**|returns 30 new and growing topical albums|boolean|||
|**geoSearch**|"city" or "nearbyVenues" or "foursquareVenue"|string|||
|**lat**|latitude|integer| for "city" and "nearbyVenues" geoSearch||
|**lng**|longitude|integer| for "city" and "nearbyVenues" geoSearch||
|**foursquareId**||string|for "foursquareVenue" geoSearch||
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|
|**minPhotos**|return albums only with at least the specified number of photos (works when "q" is specified)|integer|||
|**type**|only returns albums of a specific type (city,country,event,venue,tag) (works when "q" is specified)|string|||


### Response
***
200 and an array of album objects, optionally (for search) includes pagination parameters

[Errors](../../resources/errors.md#files)

### Examples
***

`http://www.eyeem.com/api/v2/albums?ids=35,123,3352,3563`

```javascript
{
  "albums": {
    "offset": 0,
    "limit": 2,
    "total": 2,
    "items": [
      {
        "id": "35",
        "name": "Readmill HQ",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/d412cf8ae4a2bef9f5a5aca0400f36bcb366fd77-1347135084",
        "updated": "2012-09-08T22:15:16+0200",
        "location": {
          "latitude": "52.53112030",
          "longitude": "13.40054035",
          "cityAlbum": {
            "id": "17",
            "name": "Berlin",
            "type": "city",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/621b0d81ce1fa3212a36219f2d3d91fa2a6784cb-1347617496",
            "updated": "2012-09-14T12:11:38+0200"
          },
          "countryAlbum": {
            "id": "23",
            "name": "Germany",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/621b0d81ce1fa3212a36219f2d3d91fa2a6784cb-1347617496",
            "updated": "2012-09-14T12:11:38+0200"
          },
          "venueService": {
            "name": "foursquare",
            "id": "4d73e7c9ec07548104239dbf",
            "category": "4bf58dd8d48988d125941735",
            "categoryName": "Tech Startup"
          }
        },
        "webUrl": "http://www.eyeem.com/a/35",
        "totalPhotos": 79,
        "totalLikers": 5,
        "totalContributors": 29,
        "photos": {
          "offset": 0,
          "limit": 10,
          "total": 79,
          "items": [
            {
              "id": "921635",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/d412cf8ae4a2bef9f5a5aca0400f36bcb366fd77-1347135084",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/d412cf8ae4a2bef9f5a5aca0400f36bcb366fd77-1347135084",
              "width": 1296,
              "height": 969,
              "updated": "2012-09-08T22:15:16+0200"
            },
            {
              "id": "784140",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/d8b4bab002af0b2687d3400754fc281c17d43987-1343646058",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/d8b4bab002af0b2687d3400754fc281c17d43987-1343646058",
              "width": 1024,
              "height": 682,
              "updated": "2012-07-30T13:01:09+0200"
            },
            {
              "id": "784135",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/26f6932df646d694c6a351467253433928c91f65-1343645987",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/26f6932df646d694c6a351467253433928c91f65-1343645987",
              "width": 1024,
              "height": 682,
              "updated": "2012-07-30T13:00:00+0200"
            },
            {
              "id": "775428",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/8d49a57bbca581698bcb14855fde96f339ac6210-1343431225",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/8d49a57bbca581698bcb14855fde96f339ac6210-1343431225",
              "width": 960,
              "height": 960,
              "updated": "2012-07-28T01:20:26+0200"
            },
            {
              "id": "775427",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/262c769f060a091df323ee80eb5dc1314c482a31-1343431203",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/262c769f060a091df323ee80eb5dc1314c482a31-1343431203",
              "width": 799,
              "height": 799,
              "updated": "2012-07-28T01:20:04+0200"
            },
            {
              "id": "775426",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/7d93560daa21a2486f9b8fef25a3b7a3d8296284-1343431188",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/7d93560daa21a2486f9b8fef25a3b7a3d8296284-1343431188",
              "width": 960,
              "height": 960,
              "updated": "2012-07-28T01:19:49+0200"
            },
            {
              "id": "775424",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/b0f23372d25b0124064e90623cc476e713a69f56-1343431169",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/b0f23372d25b0124064e90623cc476e713a69f56-1343431169",
              "width": 722,
              "height": 722,
              "updated": "2012-07-28T01:19:29+0200"
            },
            {
              "id": "775421",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/15b426b3c3153142aa13d468903a8b865d6c64f1-1343431139",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/15b426b3c3153142aa13d468903a8b865d6c64f1-1343431139",
              "width": 713,
              "height": 713,
              "updated": "2012-07-28T01:19:02+0200"
            },
            {
              "id": "775419",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/4e5d6c0d2ed4a74cb2437853185246dbfc31429c-1343431121",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/4e5d6c0d2ed4a74cb2437853185246dbfc31429c-1343431121",
              "width": 841,
              "height": 841,
              "updated": "2012-07-28T01:18:42+0200"
            },
            {
              "id": "775417",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/9eff1e6943f76d72938718b744281df0ce7b5beb-1343431100",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/9eff1e6943f76d72938718b744281df0ce7b5beb-1343431100",
              "width": 580,
              "height": 580,
              "updated": "2012-07-28T01:18:21+0200"
            }
          ]
        }
      },
      {
        "id": "3352",
        "name": "Cafe karlfranz",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/",
        "updated": "2011-07-22T15:37:05+0200",
        "location": {
          "latitude": "47.07585144",
          "longitude": "15.44952393",
          "cityAlbum": {
            "id": "3353",
            "name": "Graz",
            "type": "city",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/6b7ef97acbd1c0da9f69f2cd44a9ad642f0d2123-1347384743",
            "updated": "2012-09-11T19:32:25+0200"
          },
          "countryAlbum": {
            "id": "33516",
            "name": "Austria",
            "type": "country",
            "thumbUrl": "http://www.eyeem.com/thumb/sq/200/21c648cfdf4622569eb532b64a7fcf73c6393145-1347617096",
            "updated": "2012-09-14T12:05:01+0200"
          },
          "venueService": {
            "name": "foursquare",
            "id": "4b9285c7f964a520a80034e3",
            "category": "4bf58dd8d48988d16d941735",
            "categoryName": "Cafe"
          }
        },
        "webUrl": "http://www.eyeem.com/a/3352",
        "totalPhotos": 0,
        "totalLikers": 0,
        "totalContributors": 0,
        "photos": {
          "offset": 0,
          "limit": 10,
          "total": 0,
          "items": []
        }
      }
    ]
  }
}
```

`http://www.eyeem.com/api/v2/albums?q=berlin&limit=25&offset=20`

 