# GET /users/#{id}/likedPhotos  
***
`/users/#{id}/likedPhotos`

### Description
***
Get all the photos that a user has liked.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to get information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of photos to return|integer||20|
|**offset**|offset of photos to start at|integer||0|
|**onlyId**| returns a json array photoIds containing just the ids|boolean||0|


### Response
***

200 and and a dictionary containing limit, offset, total and an array of photo objects


[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/users/1013/likedPhotos`

```javascript


{
  "likedPhotos": {
    "offset": 0,
    "limit": 20,
    "total": 3978,
    "items": [
      {
        "id": 950041,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/8026e645a6fef14c2ef91a49f8545af9a9f1fa41-1347614735",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/8026e645a6fef14c2ef91a49f8545af9a9f1fa41-1347614735",
        "width": 612,
        "height": 816,
        "updated": "2012-09-14T11:26:24+0200",
        "webUrl": "http://www.eyeem.com/p/950041",
        "user": {
          "id": "82222",
          "nickname": "VM",
          "fullname": "Victor Mark",
          "webUrl": "http://www.eyeem.com/u/VM",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/f51fa2aa8ec84533106c5c8c64977f2bb412f026.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/f51fa2aa8ec84533106c5c8c64977f2bb412f026.jpg"
        },
        "title": "",
        "caption": "Gen's poses at EyeEm Studio",
        "latitude": "52.53118896",
        "longitude": "13.40087414",
        "totalLikes": 4,
        "totalComments": 0
      },
      {
        "id": 949235,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/007f94d8aaa5e257b1179b4b0f1be61919d7bd11-1347593188",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/007f94d8aaa5e257b1179b4b0f1be61919d7bd11-1347593188",
        "width": 969,
        "height": 1296,
        "updated": "2012-09-14T05:26:39+0200",
        "webUrl": "http://www.eyeem.com/p/949235",
        "user": {
          "id": "86389",
          "nickname": "errantpixel",
          "fullname": "errant_pixel",
          "webUrl": "http://www.eyeem.com/u/errantpixel",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/3f51ee0bc8f268de30f8eef5f417006ddde8a1b7-1347263971",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/3f51ee0bc8f268de30f8eef5f417006ddde8a1b7-1347263971"
        },
        "title": "",
        "caption": "Architecture in San Francisco",
        "latitude": "",
        "longitude": "",
        "totalLikes": 17,
        "totalComments": 1
      },
      {
        "id": 948831,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/7828a4470da95fa6270143f9718c9d72763d14a8-1347580007",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/7828a4470da95fa6270143f9718c9d72763d14a8-1347580007",
        "width": 1280,
        "height": 1024,
        "updated": "2012-09-14T01:46:47+0200",
        "webUrl": "http://www.eyeem.com/p/948831",
        "user": {
          "id": "3895",
          "nickname": "RemainsUNedITED",
          "fullname": "Re:main(s) UNedITED",
          "webUrl": "http://www.eyeem.com/u/RemainsUNedITED",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/e3f6e8a129e381744afbd100312bde91537f3366.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/e3f6e8a129e381744afbd100312bde91537f3366.jpg"
        },
        "title": "In a #Hospital in #Pest, #Budapest, #Hungary - #mobile #photo shot with #SonyEricsson #K510i mobile phone - remains #unedited",
        "caption": "",
        "latitude": "",
        "longitude": "",
        "totalLikes": 14,
        "totalComments": 1
      },
      {
        "id": 948772,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/d94b604018d590cf594abd3cbee6495db1e83573-1347578852",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/d94b604018d590cf594abd3cbee6495db1e83573-1347578852",
        "width": 1024,
        "height": 1024,
        "updated": "2012-09-14T01:28:11+0200",
        "webUrl": "http://www.eyeem.com/p/948772",
        "user": {
          "id": "97800",
          "nickname": "PocoLoco",
          "fullname": "PocoLoco",
          "webUrl": "http://www.eyeem.com/u/PocoLoco",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/93269a2c6bc72f4b8e4eddb0711d744c29dee74c.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/93269a2c6bc72f4b8e4eddb0711d744c29dee74c.jpg"
        },
        "title": "",
        "caption": "Nature at Venåshytta",
        "latitude": 59.152935,
        "longitude": 11.41718,
        "totalLikes": 16,
        "totalComments": 1
      },
      {
        "id": 948892,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/1d4033c150d32ac47052a6ea9beee55b24872187-1347581921",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/1d4033c150d32ac47052a6ea9beee55b24872187-1347581921",
        "width": 1152,
        "height": 432,
        "updated": "2012-09-14T02:18:41+0200",
        "webUrl": "http://www.eyeem.com/p/948892",
        "user": {
          "id": "3895",
          "nickname": "RemainsUNedITED",
          "fullname": "Re:main(s) UNedITED",
          "webUrl": "http://www.eyeem.com/u/RemainsUNedITED",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/e3f6e8a129e381744afbd100312bde91537f3366.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/e3f6e8a129e381744afbd100312bde91537f3366.jpg"
        },
        "title": "Soap & Skin on Solo Concert in the Concert Venue (and btw The Best Club of Europe) Ship A38 on the Danube in #Budapest, #Hungary, 20 October, 2011 - #experimental #two-frame #panoramic #mobile #photo shot with #SonyEricsson #K510i mobile phone - remains #unedited",
        "caption": "",
        "latitude": "",
        "longitude": "",
        "totalLikes": 16,
        "totalComments": 1
      },
      {
        "id": 948462,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/e69d2c33f448617a80631e8facb13b3819756b6a-1347573354",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/e69d2c33f448617a80631e8facb13b3819756b6a-1347573354",
        "width": 969,
        "height": 1296,
        "updated": "2012-09-13T23:57:14+0200",
        "webUrl": "http://www.eyeem.com/p/948462",
        "user": {
          "id": "87217",
          "nickname": "SandraL",
          "fullname": "Sandra L",
          "webUrl": "http://www.eyeem.com/u/SandraL",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/8a58109c69efa9c6f81c6f72061ae90658994cb0.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/8a58109c69efa9c6f81c6f72061ae90658994cb0.jpg"
        },
        "title": "",
        "caption": "Shadows to Remember",
        "latitude": "",
        "longitude": "",
        "totalLikes": 31,
        "totalComments": 5
      },
      {
        "id": 948468,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/0ab577054da5e94d042b9bad05e73c84c9f3f3cd-1347573222",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/0ab577054da5e94d042b9bad05e73c84c9f3f3cd-1347573222",
        "width": 1296,
        "height": 1296,
        "updated": "2012-09-13T23:59:48+0200",
        "webUrl": "http://www.eyeem.com/p/948468",
        "user": {
          "id": "77664",
          "nickname": "avenueone",
          "fullname": "M K",
          "webUrl": "http://www.eyeem.com/u/avenueone",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/4bf459dba2a0bcf7be56b5a13f6149437549589c.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/4bf459dba2a0bcf7be56b5a13f6149437549589c.jpg"
        },
        "title": "",
        "caption": "streetphotography in Pontevedra",
        "latitude": "",
        "longitude": "",
        "totalLikes": 90,
        "totalComments": 4
      },
      {
        "id": 948219,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/86e9643505bba2e1cfd37780011303f7fa222ad6-1347569721",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/86e9643505bba2e1cfd37780011303f7fa222ad6-1347569721",
        "width": 1297,
        "height": 1297,
        "updated": "2012-09-13T22:55:33+0200",
        "webUrl": "http://www.eyeem.com/p/948219",
        "user": {
          "id": "766",
          "nickname": "dragonpeace",
          "fullname": "Hiroshi M",
          "webUrl": "http://www.eyeem.com/u/dragonpeace",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/2ca22c722e6755197ff09c981cdeb66d4e20931b.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/2ca22c722e6755197ff09c981cdeb66d4e20931b.jpg"
        },
        "title": "",
        "caption": "Good Morning!",
        "latitude": "",
        "longitude": "",
        "totalLikes": 3,
        "totalComments": 0
      },
      {
        "id": 948253,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/bbe003e176e38e69828b76140aefbfa2dcceba30-1347570103",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/bbe003e176e38e69828b76140aefbfa2dcceba30-1347570103",
        "width": 1296,
        "height": 969,
        "updated": "2012-09-13T23:02:18+0200",
        "webUrl": "http://www.eyeem.com/p/948253",
        "user": {
          "id": "2390",
          "nickname": "mrgoodkat",
          "fullname": "mr. goodkat",
          "webUrl": "http://www.eyeem.com/u/mrgoodkat",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/97806e13649005551e4eab4eeaed4c8defffc46a.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/97806e13649005551e4eab4eeaed4c8defffc46a.jpg"
        },
        "title": "",
        "caption": "pre cinema at Neptunbrunnen",
        "latitude": 52.52,
        "longitude": 13.408166666667,
        "totalLikes": 4,
        "totalComments": 0
      },
      {
        "id": 948417,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/8131a2954ef32398f6b12a832f14e7dab6498fa1-1347572723",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/8131a2954ef32398f6b12a832f14e7dab6498fa1-1347572723",
        "width": 1280,
        "height": 1280,
        "updated": "2012-09-13T23:46:04+0200",
        "webUrl": "http://www.eyeem.com/p/948417",
        "user": {
          "id": "7946",
          "nickname": "liro",
          "fullname": "Lila",
          "webUrl": "http://www.eyeem.com/u/liro",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/5538ed236de2948f71ea5fce795f124b3a1c3c02.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/5538ed236de2948f71ea5fce795f124b3a1c3c02.jpg"
        },
        "title": "",
        "caption": "Beauty of Underwater",
        "latitude": "",
        "longitude": "",
        "totalLikes": 2,
        "totalComments": 1
      },
      {
        "id": 948430,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/91430a5da225fdd40d03017f2a589453bd729c2e-1347572874",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/91430a5da225fdd40d03017f2a589453bd729c2e-1347572874",
        "width": 972,
        "height": 1296,
        "updated": "2012-09-13T23:48:12+0200",
        "webUrl": "http://www.eyeem.com/p/948430",
        "user": {
          "id": "130396",
          "nickname": "micoh",
          "fullname": "Micha Oh",
          "webUrl": "http://www.eyeem.com/u/micoh",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/80b3e9aa4526d5933da5aeb3aa9cdd227446f169.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/80b3e9aa4526d5933da5aeb3aa9cdd227446f169.jpg"
        },
        "title": "",
        "caption": "Out of Control at Cassiopeia",
        "latitude": 52.507333333333,
        "longitude": 13.454833333333,
        "totalLikes": 3,
        "totalComments": 0
      },
      {
        "id": 948437,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/106533f20c2e6f82e6fc06c7dffec3e44bee364e-1347573023",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/106533f20c2e6f82e6fc06c7dffec3e44bee364e-1347573023",
        "width": 972,
        "height": 1296,
        "updated": "2012-09-13T23:50:30+0200",
        "webUrl": "http://www.eyeem.com/p/948437",
        "user": {
          "id": "125205",
          "nickname": "ntljk",
          "fullname": "Natalie",
          "webUrl": "http://www.eyeem.com/u/ntljk",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/6ece45cff289f0349acd6e76fd2ce17bd257fd50.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/6ece45cff289f0349acd6e76fd2ce17bd257fd50.jpg"
        },
        "title": "",
        "caption": "Yoga at Erich Weinert Straße",
        "latitude": 52.5485,
        "longitude": 13.427166666667,
        "totalLikes": 3,
        "totalComments": 0
      },
      {
        "id": 948439,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/d1dcc6cf427da0af9c2c091c581eb2ec87011295-1347573039",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/d1dcc6cf427da0af9c2c091c581eb2ec87011295-1347573039",
        "width": 816,
        "height": 612,
        "updated": "2012-09-13T23:50:49+0200",
        "webUrl": "http://www.eyeem.com/p/948439",
        "user": {
          "id": "82222",
          "nickname": "VM",
          "fullname": "Victor Mark",
          "webUrl": "http://www.eyeem.com/u/VM",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/f51fa2aa8ec84533106c5c8c64977f2bb412f026.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/f51fa2aa8ec84533106c5c8c64977f2bb412f026.jpg"
        },
        "title": "",
        "caption": "Urban nature in Berlin",
        "latitude": "52.523522",
        "longitude": "13.4511022",
        "totalLikes": 9,
        "totalComments": 0
      },
      {
        "id": 948469,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/3c834cfa73154468e1273925bef411e52a7a489a-1347573514",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/3c834cfa73154468e1273925bef411e52a7a489a-1347573514",
        "width": 969,
        "height": 1296,
        "updated": "2012-09-13T23:59:50+0200",
        "webUrl": "http://www.eyeem.com/p/948469",
        "user": {
          "id": "87217",
          "nickname": "SandraL",
          "fullname": "Sandra L",
          "webUrl": "http://www.eyeem.com/u/SandraL",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/8a58109c69efa9c6f81c6f72061ae90658994cb0.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/8a58109c69efa9c6f81c6f72061ae90658994cb0.jpg"
        },
        "title": "",
        "caption": "Shadows to Remember",
        "latitude": "",
        "longitude": "",
        "totalLikes": 28,
        "totalComments": 0
      },
      {
        "id": 948457,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/5ba46f2cc84e1881a76faf63d6c9f74ec050285b-1347573352",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/5ba46f2cc84e1881a76faf63d6c9f74ec050285b-1347573352",
        "width": 985,
        "height": 1296,
        "updated": "2012-09-13T23:56:19+0200",
        "webUrl": "http://www.eyeem.com/p/948457",
        "user": {
          "id": "1177",
          "nickname": "photo444",
          "fullname": "photo444.com",
          "webUrl": "http://www.eyeem.com/u/photo444",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/d14c69eea9d295bfbbfacdede4799406184fd84b.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/d14c69eea9d295bfbbfacdede4799406184fd84b.jpg"
        },
        "title": "",
        "caption": "portrait at Santiago Dominican Republic",
        "latitude": 19.399361009664,
        "longitude": -70.616262322226,
        "totalLikes": 48,
        "totalComments": 2
      },
      {
        "id": 948179,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/94684270321afbd5f7516175b4cbf32e6deda3ff-1347569226",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/94684270321afbd5f7516175b4cbf32e6deda3ff-1347569226",
        "width": 972,
        "height": 1296,
        "updated": "2012-09-13T22:47:27+0200",
        "webUrl": "http://www.eyeem.com/p/948179",
        "user": {
          "id": "24330",
          "nickname": "ftrc",
          "fullname": "Felipe Tofani",
          "webUrl": "http://www.eyeem.com/u/ftrc",
          "thumbUrl": "https://graph.facebook.com/701787268/picture?type=square",
          "photoUrl": "https://graph.facebook.com/701787268/picture?type=large"
        },
        "title": "",
        "caption": "Taking Photos at Biergarten | Tempelhofer Park",
        "latitude": 52.482166666667,
        "longitude": 13.405166666667,
        "totalLikes": 3,
        "totalComments": 0
      },
      {
        "id": 947952,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/f62ce9c28b9342d0a80b479444d66347fec67f4d-1347565830",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/f62ce9c28b9342d0a80b479444d66347fec67f4d-1347565830",
        "width": 960,
        "height": 720,
        "updated": "2012-09-13T21:50:51+0200",
        "webUrl": "http://www.eyeem.com/p/947952",
        "user": {
          "id": "120687",
          "nickname": "nar",
          "fullname": "NAR",
          "webUrl": "http://www.eyeem.com/u/nar",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/21373c19ac14df53d14990271ad3fffb8cf2eae9.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/21373c19ac14df53d14990271ad3fffb8cf2eae9.jpg"
        },
        "title": "",
        "caption": "Nature",
        "latitude": "",
        "longitude": "",
        "totalLikes": 4,
        "totalComments": 0
      },
      {
        "id": 947699,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/a6355c96ccc05d13b493e0af75410896f739a24b-1347561871",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/a6355c96ccc05d13b493e0af75410896f739a24b-1347561871",
        "width": 972,
        "height": 1296,
        "updated": "2012-09-13T20:44:52+0200",
        "webUrl": "http://www.eyeem.com/p/947699",
        "user": {
          "id": "1015",
          "nickname": "Gen",
          "fullname": "Gen Sadakane",
          "webUrl": "http://www.eyeem.com/u/Gen",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/f39a693bdc2f09a8af61ecf003e448e8482755a8.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/f39a693bdc2f09a8af61ecf003e448e8482755a8.jpg"
        },
        "title": "",
        "caption": "happy socks at EyeEm Studio",
        "latitude": 52.531166666667,
        "longitude": 13.400833333333,
        "totalLikes": 32,
        "totalComments": 8
      },
      {
        "id": 947326,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/c176ff9bd90d2bc5ed2460fb1bbf92496b310ce3-1347556775",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/c176ff9bd90d2bc5ed2460fb1bbf92496b310ce3-1347556775",
        "width": 972,
        "height": 1296,
        "updated": "2012-09-13T19:19:49+0200",
        "webUrl": "http://www.eyeem.com/p/947326",
        "user": {
          "id": "9274",
          "nickname": "daniellereid",
          "fullname": "Danielle Reid",
          "webUrl": "http://www.eyeem.com/u/daniellereid",
          "thumbUrl": "http://www.eyeem.com/thumb/sq/50/7fd5c77dfffb9aee2e1c8c7f7792894af8d4547d.jpg",
          "photoUrl": "http://www.eyeem.com/thumb/sq/200/7fd5c77dfffb9aee2e1c8c7f7792894af8d4547d.jpg"
        },
        "title": "",
        "caption": "Taking Photos at EyeEm Studio",
        "latitude": "52.53118896",
        "longitude": "13.40087414",
        "totalLikes": 9,
        "totalComments": 0
      },
      {
        "id": 947448,
        "thumbUrl": "http://www.eyeem.com/thumb/h/100/acec54b075d89104664bbf23c5c3a8d79dba0127-1347558446",
        "photoUrl": "http://www.eyeem.com/thumb/640/480/acec54b075d89104664bbf23c5c3a8d79dba0127-1347558446",
        "width": 972,
        "height": 1296,
        "updated": "2012-09-13T19:47:43+0200",
        "webUrl": "http://www.eyeem.com/p/947448",
        "user": {
          "id": "142558",
          "nickname": "sophiehechinger",
          "fullname": "Sophie Hechinger",
          "webUrl": "http://www.eyeem.com/u/sophiehechinger",
          "thumbUrl": "https://graph.facebook.com/581701239/picture?type=square",
          "photoUrl": "https://graph.facebook.com/581701239/picture?type=large"
        },
        "title": "",
        "caption": "grey lollipop at EyeEm Studio",
        "latitude": 52.531333333333,
        "longitude": 13.401,
        "totalLikes": 1,
        "totalComments": 1
      }
    ]
  }
}

```


