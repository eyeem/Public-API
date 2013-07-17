# GET /venues/search    >>X-Api-Version 2.2.0<<
***
`/venues/search`

### Description
***
Retrieves venues for a specific location and topics for each venue. Additionally, the current city album is returned. If the X-hourOfDay header is provided, topic suggestions are filtered according to their relevance (ex: breakfast in the morning, dinner at night)

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**lat**|latitude|integer|x||
|**lng**|longitude|integer|x||
|**cityName**|current city name(from device)|String|||
|**cc**|current country code (from device)|String|||
|**query**|string to search for|String|||

### Response
***
200 and an array of venues of the specified location and the city

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/venues/search?lat=52.2&lng=14.4`

```json
{
  "suggestions": {
    "city": {
      "id": "53003",
      "name": "Frankfurt (Oder)",
      "type": "city",
      "thumbUrl": "http://www.eyeem.com/thumb/sq/200/81649975a52da803fa22e4e0aaa656bf5972728d-1359237811",
      "webUrl": "http://www.eyeem.com/a/53003",
      "updated": "2013-07-15T07:56:55+0200",
      "location": {
        "latitude": "52.34714",
        "longitude": "14.55062",
        "countryCode": "DE",
        "countryAlbum": {
          "id": "23",
          "name": "Germany",
          "type": "country",
          "thumbUrl": "http://cdn.eyeem.com/thumb/sq/200/4fbf551231917efbc913d5a689c982f8db2c5f7a-1358438528",
          "webUrl": "http://www.eyeem.com/a/23",
          "updated": "2013-07-17T13:42:18+0200"
        }
      },
      "totalPhotos": 266,
      "totalLikers": 2,
      "totalContributors": 57,
      "hidden": false
    },
    "defaultTopics": {
      "16": "hanging out",
      "12422": "taking photos"
    },
    "defaultSentences": [
      "[a:16] with my friends",
      "hate [a:12422]"
    ],
    "venues": {
      "offset": 0,
      "limit": 30,
      "total": 30,
      "items": [
        {
        "name": "Tor zum Schlaubetal",
        "serviceId": "4f11a2d0e4b0044a23655beb",
        "venueServiceName": "foursquare",
        "topics": [],
        "category": "4bf58dd8d48988d159941735",
        "categoryName": "Hiking Trail"
        },
        {
          "name": "Bahnhof Mixdorf",
          "serviceId": "511ac86da629ec8f68cf4fce",
          "venueServiceName": "foursquare",
          "topics": {
            "851": "sleeping",
            "911": "subway",
            "7131": "commuting",
            "197636": "public transportation"
          },
          "category": "4bf58dd8d48988d129951735",
          "categoryName": "Train Station",
          "sentences": [
            "I love [a:197636]",
            "running to catch the [a:911]",
            "almost [a:851]",
            "[a:7131] again?"
          ]
        },
        {
          "name": "Mixdorfer Stübchen",
          "serviceId": "4dea111845dd3993a880fa5e",
          "venueServiceName": "foursquare",
          "topics": [],
          "category": "4bf58dd8d48988d10d941735",
          "categoryName": "German Restaurant"
        },
        {
          "name": "Bahnhof Beeskow",
          "serviceId": "511ac86da629ec8f68cf4f7d",
          "venueServiceName": "foursquare",
          "topics": {
            "851": "sleeping",
            "911": "subway",
            "7131": "commuting",
            "197636": "public transportation"
          },
          "category": "4bf58dd8d48988d129951735",
          "categoryName": "Train Station",
          "sentences": [
            "I love [a:197636]",
            "running to catch the [a:911]",
            "almost [a:851]",
            "[a:7131] again?"
          ]
        }
      ]
    }
  }
}
```

 