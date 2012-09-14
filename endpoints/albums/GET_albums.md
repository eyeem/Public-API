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

`http://www.eyeem.com/api/v2/albums?ids=35,3352`

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

`http://www.eyeem.com/api/v2/albums?q=berlin&limit=5&offset=20`

```javascript

{
  "albums": {
    "offset": 20,
    "limit": 5,
    "total": 1352,
    "items": [
      {
        "id": "1116",
        "name": "SAP Berlin",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/21366e5497dd95470615c45ac86457a8f316ff80-1347030228",
        "updated": "2012-09-07T17:04:44+0200",
        "location": {
          "latitude": "52.52593613",
          "longitude": "13.40338516",
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
            "id": "4b9fb129f964a5205f3537e3",
            "category": "4bf58dd8d48988d173941735",
            "categoryName": "Auditorium"
          }
        },
        "webUrl": "http://www.eyeem.com/a/1116",
        "totalPhotos": 44,
        "totalLikers": 2,
        "totalContributors": 8,
        "photos": {
          "offset": 0,
          "limit": 10,
          "total": 44,
          "items": [
            {
              "id": "913115",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/21366e5497dd95470615c45ac86457a8f316ff80-1347030228",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/21366e5497dd95470615c45ac86457a8f316ff80-1347030228",
              "width": 972,
              "height": 1296,
              "updated": "2012-09-07T17:04:44+0200"
            },
            {
              "id": "823883",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/9c6a41d26f753d7cb9f8f372b0f816c1ff5a2039-1344646295",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/9c6a41d26f753d7cb9f8f372b0f816c1ff5a2039-1344646295",
              "width": 1191,
              "height": 1296,
              "updated": "2012-08-11T02:51:36+0200"
            },
            {
              "id": "515746",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/f094475b601358687b9831f2ba0b9ca1f009ceb6-1337715922",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/f094475b601358687b9831f2ba0b9ca1f009ceb6-1337715922",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T21:45:24+0200"
            },
            {
              "id": "515662",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/1d742fdc9730bc8693151c7464713e68a5b38be0-1337714641",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/1d742fdc9730bc8693151c7464713e68a5b38be0-1337714641",
              "width": 2048,
              "height": 1530,
              "updated": "2012-05-22T21:24:02+0200"
            },
            {
              "id": "515594",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/9c91d8976c7acc55cccfce8bdaee199c1dd54cad-1337713756",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/9c91d8976c7acc55cccfce8bdaee199c1dd54cad-1337713756",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T21:09:17+0200"
            },
            {
              "id": "515584",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/627d644bddd1096b0bfa4f130dbf3bac4c610251-1337713623",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/627d644bddd1096b0bfa4f130dbf3bac4c610251-1337713623",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T21:07:09+0200"
            },
            {
              "id": "515579",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/d3b03847b68daf1073f11d286a55a62a52209969-1337713542",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/d3b03847b68daf1073f11d286a55a62a52209969-1337713542",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T21:05:51+0200"
            },
            {
              "id": "515541",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/8b639e01dd0dcdd2688ccb3990531098a498c6a0-1337712933",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/8b639e01dd0dcdd2688ccb3990531098a498c6a0-1337712933",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T20:55:42+0200"
            },
            {
              "id": "515528",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/f91876b2848ec8fff8a2f34680886cc485edabcf-1337712822",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/f91876b2848ec8fff8a2f34680886cc485edabcf-1337712822",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T20:53:43+0200"
            },
            {
              "id": "515515",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/d8408622bb3a7a1610a578f2cf00753df5a2b4eb-1337712677",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/d8408622bb3a7a1610a578f2cf00753df5a2b4eb-1337712677",
              "width": 612,
              "height": 816,
              "updated": "2012-05-22T20:51:24+0200"
            }
          ]
        }
      },
      {
        "id": "7298",
        "name": "Lomography Gallery Store Berlin",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/ac65ef9b120053ac5df3434d02b03681749eb00b-1347568679",
        "updated": "2012-09-13T22:38:08+0200",
        "location": {
          "latitude": "52.52360916",
          "longitude": "13.38733482",
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
            "id": "4b4b97b2f964a5204da126e3",
            "category": "4bf58dd8d48988d1f3941735",
            "categoryName": "Toy / Game Store"
          }
        },
        "webUrl": "http://www.eyeem.com/a/7298",
        "totalPhotos": 44,
        "totalLikers": 6,
        "totalContributors": 6,
        "photos": {
          "offset": 0,
          "limit": 10,
          "total": 44,
          "items": [
            {
              "id": 948122,
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/ac65ef9b120053ac5df3434d02b03681749eb00b-1347568679",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/ac65ef9b120053ac5df3434d02b03681749eb00b-1347568679",
              "width": 488,
              "height": 816,
              "updated": "2012-09-13T22:38:08+0200"
            },
            {
              "id": 947959,
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/25f0c9e16180819147f1b1ad6cbc21a9c50efa54-1347565905",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/25f0c9e16180819147f1b1ad6cbc21a9c50efa54-1347565905",
              "width": 1024,
              "height": 768,
              "updated": "2012-09-13T21:52:15+0200"
            },
            {
              "id": 947714,
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/a8a7020096d45014df4713ab0c4f4c633d4a5b58-1347562057",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/a8a7020096d45014df4713ab0c4f4c633d4a5b58-1347562057",
              "width": 1024,
              "height": 768,
              "updated": "2012-09-13T20:47:59+0200"
            },
            {
              "id": "819289",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/481a0dd414d73971d77e4084b8b1ab808f3e4b0f-1344533797",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/481a0dd414d73971d77e4084b8b1ab808f3e4b0f-1344533797",
              "width": 816,
              "height": 612,
              "updated": "2012-08-09T19:37:17+0200"
            },
            {
              "id": "799328",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/dd9b5fe5c0e08d635b7ac02b740d7a2fc610f97f-1344015860",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/dd9b5fe5c0e08d635b7ac02b740d7a2fc610f97f-1344015860",
              "width": 1024,
              "height": 613,
              "updated": "2012-08-03T19:44:55+0200"
            },
            {
              "id": "799308",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/1255055402ff854c9abbaf00dd6be87ceac15861-1344015387",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/1255055402ff854c9abbaf00dd6be87ceac15861-1344015387",
              "width": 1024,
              "height": 613,
              "updated": "2012-08-03T19:36:55+0200"
            },
            {
              "id": "766378",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/1b07e50f3471322e587906c1250947e47a56acb7-1343213593",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/1b07e50f3471322e587906c1250947e47a56acb7-1343213593",
              "width": 816,
              "height": 612,
              "updated": "2012-07-25T12:53:37+0200"
            },
            {
              "id": "736489",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/eabb21d2547d55caf1dc123cc9758c618c1d8d35-1342533040",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/eabb21d2547d55caf1dc123cc9758c618c1d8d35-1342533040",
              "width": 488,
              "height": 816,
              "updated": "2012-07-17T15:50:58+0200"
            },
            {
              "id": "694561",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/6de4398be83f594c47fbee78c42ef1645cc3648a-1341523354",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/6de4398be83f594c47fbee78c42ef1645cc3648a-1341523354",
              "width": 612,
              "height": 816,
              "updated": "2012-07-05T23:22:37+0200"
            },
            {
              "id": "694557",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/e9074f12dd22e841f443d85de9ed5ef4220a288f-1341523235",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/e9074f12dd22e841f443d85de9ed5ef4220a288f-1341523235",
              "width": 612,
              "height": 816,
              "updated": "2012-07-05T23:20:38+0200"
            }
          ]
        }
      },
      {
        "id": "309324",
        "name": "Berlin Paris",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/9c07b3a44fc19e1ba538ccf812f32cf0983ef5b3-1341163199",
        "updated": "2012-07-03T07:57:33+0200",
        "webUrl": "http://www.eyeem.com/a/309324",
        "totalPhotos": 44,
        "totalLikers": 3,
        "totalContributors": 1,
        "photos": {
          "offset": 0,
          "limit": 10,
          "total": 44,
          "items": [
            {
              "id": "679274",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/9c07b3a44fc19e1ba538ccf812f32cf0983ef5b3-1341163199",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/9c07b3a44fc19e1ba538ccf812f32cf0983ef5b3-1341163199",
              "width": 816,
              "height": 612,
              "updated": "2012-07-01T19:20:11+0200"
            },
            {
              "id": "679270",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/fab64c96e20e372f4cbec670dad45f46ecd1bc3d-1341163166",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/fab64c96e20e372f4cbec670dad45f46ecd1bc3d-1341163166",
              "width": 816,
              "height": 612,
              "updated": "2012-07-01T19:19:41+0200"
            },
            {
              "id": "679267",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/35e74c31e6e501eed52f4a0270c2f78f2034d5e5-1341163121",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/35e74c31e6e501eed52f4a0270c2f78f2034d5e5-1341163121",
              "width": 612,
              "height": 816,
              "updated": "2012-07-01T19:19:05+0200"
            },
            {
              "id": "679260",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/418f786835d3e5901fb51786658e88b0f0f9df79-1341163089",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/418f786835d3e5901fb51786658e88b0f0f9df79-1341163089",
              "width": 816,
              "height": 612,
              "updated": "2012-07-01T19:18:15+0200"
            },
            {
              "id": "679255",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/16bea99543a2d4c7ddf2615594592fb3833fef12-1341163039",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/16bea99543a2d4c7ddf2615594592fb3833fef12-1341163039",
              "width": 816,
              "height": 612,
              "updated": "2012-07-01T19:17:23+0200"
            },
            {
              "id": "679244",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/d12183e04562c81994655e6a2d186e7c7b55cb97-1341162942",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/d12183e04562c81994655e6a2d186e7c7b55cb97-1341162942",
              "width": 612,
              "height": 816,
              "updated": "2012-07-01T19:15:46+0200"
            },
            {
              "id": "679243",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/20ac22b8517b3c0542f9a2286eb5a4620de913f1-1341162872",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/20ac22b8517b3c0542f9a2286eb5a4620de913f1-1341162872",
              "width": 612,
              "height": 816,
              "updated": "2012-07-01T19:15:20+0200"
            },
            {
              "id": "679224",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/1eeb20c9eb315bab3d8657bdde5f1dfe5816c9de-1341162733",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/1eeb20c9eb315bab3d8657bdde5f1dfe5816c9de-1341162733",
              "width": 612,
              "height": 816,
              "updated": "2012-07-01T19:12:14+0200"
            },
            {
              "id": "679220",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/2e0ef471be6dbf43944e94b693d7b5945acf2dad-1341162620",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/2e0ef471be6dbf43944e94b693d7b5945acf2dad-1341162620",
              "width": 612,
              "height": 816,
              "updated": "2012-07-01T19:10:28+0200"
            },
            {
              "id": "679217",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/592658c4c23039a859004f7ae411e1ecf0dc3377-1341162560",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/592658c4c23039a859004f7ae411e1ecf0dc3377-1341162560",
              "width": 612,
              "height": 816,
              "updated": "2012-07-01T19:09:26+0200"
            }
          ]
        }
      },
      {
        "id": "4394",
        "name": "o2 World Berlin",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/4ad54c54f14bf03593d6221fc98d21e32867f569-1346535035",
        "updated": "2012-09-01T23:30:47+0200",
        "location": {
          "latitude": "52.50616455",
          "longitude": "13.44168663",
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
            "id": "4ba33a3cf964a520c03038e3",
            "category": "4bf58dd8d48988d1e6931735",
            "categoryName": "Concert Hall"
          }
        },
        "webUrl": "http://www.eyeem.com/a/4394",
        "totalPhotos": 38,
        "totalLikers": 5,
        "totalContributors": 17,
        "photos": {
          "offset": 0,
          "limit": 10,
          "total": 38,
          "items": [
            {
              "id": "895467",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/4ad54c54f14bf03593d6221fc98d21e32867f569-1346535035",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/4ad54c54f14bf03593d6221fc98d21e32867f569-1346535035",
              "width": 1024,
              "height": 576,
              "updated": "2012-09-01T23:30:47+0200"
            },
            {
              "id": "799701",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/155a7f7317f676b2ecc15eabef0603882e4a1366-1344023111",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/155a7f7317f676b2ecc15eabef0603882e4a1366-1344023111",
              "width": 1296,
              "height": 969,
              "updated": "2012-08-03T21:45:12+0200"
            },
            {
              "id": "799482",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/6a6300043196ade0a434ef57b857c2ade6ed197a-1344018843",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/6a6300043196ade0a434ef57b857c2ade6ed197a-1344018843",
              "width": 1296,
              "height": 969,
              "updated": "2012-08-03T20:34:37+0200"
            },
            {
              "id": "764768",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/802419e4ee1b0ae10ad899472bde5990e9de4c1b-1343165158",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/802419e4ee1b0ae10ad899472bde5990e9de4c1b-1343165158",
              "width": 1296,
              "height": 972,
              "updated": "2012-07-24T23:26:02+0200"
            },
            {
              "id": "675798",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/2ab8be6cbe7420a7679f90964d67512d9c42b756-1341091470",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/2ab8be6cbe7420a7679f90964d67512d9c42b756-1341091470",
              "width": 1296,
              "height": 972,
              "updated": "2012-06-30T23:24:57+0200"
            },
            {
              "id": "646315",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/f5755c5b4c206e37e4ac355fdbc5911871bbff40-1340454530",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/f5755c5b4c206e37e4ac355fdbc5911871bbff40-1340454530",
              "width": 1296,
              "height": 1296,
              "updated": "2012-06-23T14:28:57+0200"
            },
            {
              "id": "613846",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/996e486a15c5ffd59eaa53068efdc3aa331fc77c-1339786951",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/996e486a15c5ffd59eaa53068efdc3aa331fc77c-1339786951",
              "width": 1296,
              "height": 972,
              "updated": "2012-06-15T21:03:04+0200"
            },
            {
              "id": "399349",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/9bc2a3680f89558ad45e8b7de883888f326957de-1335460885",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/9bc2a3680f89558ad45e8b7de883888f326957de-1335460885",
              "width": 3264,
              "height": 2448,
              "updated": "2012-04-26T17:21:27+0200"
            },
            {
              "id": "230809",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/46977ef1d029844b222c6d5d600926dd6abb60df-1329589353",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/46977ef1d029844b222c6d5d600926dd6abb60df-1329589353",
              "width": 1024,
              "height": 771,
              "updated": "2012-02-18T18:23:21+0100"
            },
            {
              "id": "178821",
              "thumbUrl": "http://www.eyeem.com/thumb/h/100/5e4d58e86722e8231dbef754e107bacc3d5ded45-1325341695",
              "photoUrl": "http://www.eyeem.com/thumb/640/480/5e4d58e86722e8231dbef754e107bacc3d5ded45-1325341695",
              "width": 1224,
              "height": 1632,
              "updated": "2011-12-31T14:28:24+0100"
            }
          ]
        }
      }
    ]
  }
}
```

 