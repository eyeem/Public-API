# GET /albums/#{id}/relatedAlbums
***
`/albums/#{id|/relatedAlbums`

### Description
***
Retrieves albums related to the one specified in the id URL query parameter. useful for finding popular topics at specific venues, cities in a country, etc...

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| The id of the album|integer|x||
|**type**|only returns related albums of a specific type (city,country,event,venue,tag)|string|||
|**venueCategory**|search for venues that belong to a particular Foursquare venue category (requires type=venue)|string||0|
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|

### Response
***
200 and an array of album objects, optionally (for search) includes pagination parameters

[Errors](../../resources/errors.md#files)

### Examples
***

`http://www.eyeem.com/api/v2/albums/17/relatedAlbums`

```json


{
  "album": {
    "id": "17",
    "name": "Berlin",
    "type": "city",
    "thumbUrl": "http://www.eyeem.com/thumb/sq/200/4fbf551231917efbc913d5a689c982f8db2c5f7a-1358438528",
    "webUrl": "http://www.eyeem.com/a/17",
    "updated": "2013-04-06T22:00:00+0200"
  },
  "relatedAlbums": {
    "offset": 0,
    "limit": 30,
    "total": 59238,
    "items": [
      {
        "id": "23",
        "name": "Germany",
        "type": "country",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/4fbf551231917efbc913d5a689c982f8db2c5f7a-1358438528",
        "webUrl": "http://www.eyeem.com/a/23",
        "updated": "2013-04-06T22:10:03+0200",
        "count": 76853
      },
      {
        "id": "16",
        "name": "Hanging out",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/e0d77179ade1a2cc57626e8d98c50d5c374cc750-1361916123",
        "webUrl": "http://www.eyeem.com/a/16",
        "updated": "2013-04-06T22:10:07+0200",
        "count": 4798
      },
      {
        "id": "24",
        "name": "EyeEm HQ",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/4fbf551231917efbc913d5a689c982f8db2c5f7a-1358438528",
        "webUrl": "http://www.eyeem.com/a/24",
        "updated": "2013-04-06T12:39:23+0200",
        "count": 4543
      },
      {
        "id": "18",
        "name": "Deutschland",
        "type": "country",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/6ec5c0af2c06a6a7bea67b318f51e427c9910efd-1323859645",
        "webUrl": "http://www.eyeem.com/a/18",
        "updated": "2013-01-27T00:16:01+0100",
        "count": 3422
      },
      {
        "id": "12422",
        "name": "Taking Photos",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/6319be47b458d70b95d1b81d038d2e3fcde5b309-1361139690",
        "webUrl": "http://www.eyeem.com/a/12422",
        "updated": "2013-04-06T22:09:42+0200",
        "count": 1917
      },
      {
        "id": "4454",
        "name": "blackandwhite",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/c9d15812b5502fe8660d5248108f06f2be61e2b2-1356127389",
        "webUrl": "http://www.eyeem.com/a/4454",
        "updated": "2013-04-06T22:09:57+0200",
        "count": 1849
      },
      {
        "id": "626",
        "name": "Berlin",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/7b50f6582fe853d6e709b39aa4f7679474cb50a8-1356363387",
        "webUrl": "http://www.eyeem.com/a/626",
        "updated": "2013-04-06T21:47:07+0200",
        "count": 1812
      },
      {
        "id": "14",
        "name": "Checking in",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2f6971141a9fc9e32508fef7d66c894bcdfa8b22-1358783096",
        "webUrl": "http://www.eyeem.com/a/14",
        "updated": "2013-04-06T21:56:41+0200",
        "count": 1511
      },
      {
        "id": "563",
        "name": "streetphotography",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/37170af02b29cf176a9234b6ba24814cb5d3338b-1356169547",
        "webUrl": "http://www.eyeem.com/a/563",
        "updated": "2013-04-06T22:09:42+0200",
        "count": 1083
      },
      {
        "id": "20",
        "name": "Relaxing",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/7ada60321dd1a55374ae777eedc78fc0af3cd328-1360269392",
        "webUrl": "http://www.eyeem.com/a/20",
        "updated": "2013-04-06T22:09:55+0200",
        "count": 985
      },
      {
        "id": "33",
        "name": "Architecture",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/ca09f79dea89e798af13d3bf1e8398218e946e9f-1360701529",
        "webUrl": "http://www.eyeem.com/a/33",
        "updated": "2013-04-06T21:46:39+0200",
        "count": 971
      },
      {
        "id": "19230",
        "name": "Changing the world",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/68cc4ba4caa4f90c814e1af56a6e835f72f20f0e-1356537555",
        "webUrl": "http://www.eyeem.com/a/19230",
        "updated": "2013-04-06T21:23:48+0200",
        "count": 798
      },
      {
        "id": "148",
        "name": "Walking around",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/f293c60cd904a664ccc5eeb7e354ca4a015c9d66-1315760896",
        "webUrl": "http://www.eyeem.com/a/148",
        "updated": "2013-04-06T20:30:00+0200",
        "count": 788
      },
      {
        "id": "252588",
        "name": "EyeEm Masterclass",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/b1d25c7348d3e22c747ab76ab2c32deada4558e9-1357053404",
        "webUrl": "http://www.eyeem.com/a/252588",
        "updated": "2013-04-06T20:19:26+0200",
        "count": 696
      },
      {
        "id": "69",
        "name": "Having fun",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/44c0bd9ddd1c07c58654547720be91e550fe3ac7-1362809659",
        "webUrl": "http://www.eyeem.com/a/69",
        "updated": "2013-04-06T21:28:15+0200",
        "count": 679
      },
      {
        "id": "2399",
        "name": "streetart",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/2ad1161320c941406ae454d31660f5d7d618e1ca-1358881157",
        "webUrl": "http://www.eyeem.com/a/2399",
        "updated": "2013-04-06T21:46:03+0200",
        "count": 564
      },
      {
        "id": "696",
        "name": "Lunch",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/94a5edd5ab87a4e96e7eeda5721a166e43632d1b-1358775946",
        "webUrl": "http://www.eyeem.com/a/696",
        "updated": "2013-04-06T21:54:16+0200",
        "count": 564
      },
      {
        "id": "51",
        "name": "Coffee",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/db4e28223e4d8dd76c9edcfdcfb59c3cf2ceb789-1358445612",
        "webUrl": "http://www.eyeem.com/a/51",
        "updated": "2013-04-06T22:10:05+0200",
        "count": 547
      },
      {
        "id": "612",
        "name": "Working hard",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/309ba81e3ee60d9eef1c463ebfb558178985467c-1357905252",
        "webUrl": "http://www.eyeem.com/a/612",
        "updated": "2013-04-06T21:54:02+0200",
        "count": 517
      },
      {
        "id": "6772",
        "name": "Quality time",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/3c1c5f09f1da492d9fc94c85a1bf6720af83d9de-1362002202",
        "webUrl": "http://www.eyeem.com/a/6772",
        "updated": "2013-04-06T21:57:18+0200",
        "count": 491
      },
      {
        "id": "250",
        "name": "Working",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/bcd76962fe8a3a19676257954a609499f5babfc1-1364899444",
        "webUrl": "http://www.eyeem.com/a/250",
        "updated": "2013-04-06T22:07:00+0200",
        "count": 488
      },
      {
        "id": "190",
        "name": "Dinner",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/01cddd127c264a4f103439cc454c1a31b03a52b7-1360386065",
        "webUrl": "http://www.eyeem.com/a/190",
        "updated": "2013-04-06T19:46:22+0200",
        "count": 460
      },
      {
        "id": "306",
        "name": "Waiting",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/8dce71910cf748ea0fafd3e6147de13224a99951-1358968480",
        "webUrl": "http://www.eyeem.com/a/306",
        "updated": "2013-04-06T22:09:06+0200",
        "count": 450
      },
      {
        "id": "914",
        "name": "Alexanderplatz",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/401e3cd3682d8606c00937803289339f064f4dea-1362615786",
        "webUrl": "http://www.eyeem.com/a/914",
        "updated": "2013-04-06T01:22:55+0200",
        "count": 436
      },
      {
        "id": "53920",
        "name": "enjoying life",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/0098b4bb131f7e6ee5a53391022054d88c7c8ac5-1360776125",
        "webUrl": "http://www.eyeem.com/a/53920",
        "updated": "2013-04-06T22:09:20+0200",
        "count": 413
      },
      {
        "id": "58",
        "name": "Meeting",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/e5bf07b987bacb0450f460ff6346f5c8a3de7df9-1364482349",
        "webUrl": "http://www.eyeem.com/a/58",
        "updated": "2013-04-06T22:09:22+0200",
        "count": 389
      },
      {
        "id": "911",
        "name": "subway",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/967b61ff22718351a4afec83953fb2fed21d61ef-1359039046",
        "webUrl": "http://www.eyeem.com/a/911",
        "updated": "2013-04-06T20:53:12+0200",
        "count": 377
      },
      {
        "id": "5093",
        "name": "art",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/514751a9550cc13e44b93ca63aafd1e770a24dc4-1359808857",
        "webUrl": "http://www.eyeem.com/a/5093",
        "updated": "2013-04-06T22:07:04+0200",
        "count": 376
      },
      {
        "id": "308954",
        "name": "PLATOON KUNSTHALLE",
        "type": "venue",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/dab7823619042347a790696fe138db874adfdde1-1348259550",
        "webUrl": "http://www.eyeem.com/a/308954",
        "updated": "2013-03-24T21:47:12+0100",
        "count": 368
      },
      {
        "id": "409410",
        "name": "Startupbootcamp Berlin 2012",
        "type": "tag",
        "thumbUrl": "http://www.eyeem.com/thumb/sq/200/67be5509b0aa0322913775cf99ea6604f27a437c-1347052741",
        "webUrl": "http://www.eyeem.com/a/409410",
        "updated": "2013-03-10T22:31:50+0100",
        "count": 366
      }
    ]
  }
}

```