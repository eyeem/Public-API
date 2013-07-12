# GET /venues/search
***
`/venues/search`

### Description
***
Retrieves venues for a specific location and topics for each venue.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**lat**|latitude|integer|x||
|**lng**|longitude|integer|x||



### Response
***
200 and an array of venues of the specified location and the city

[Errors](../../resources/errors.md#files)

### Examples
***

`http://api.eyeem.com/v2/venues/search?lat=52.2&lng=14.4`

```json
{
  "suggestions": {
    "city": {
      "id": "53003",
      "name": "Frankfurt (Oder)",
      "type": "city",
      "thumbUrl": "http://cdn.eyeem.com/thumb/sq/200/3b8903f12f541f4a79c48e765312308653f1475b-1348416859",
      "webUrl": "http://www.eyeem.com/a/53003",
      "updated": "2012-09-23T18:15:37+0200",
      "location": {
        "latitude": "52.34714",
        "longitude": "14.55062",
        "countryCode": "DE",
        "countryAlbum": {
          "id": "23",
          "name": "Germany",
          "type": "country",
          "thumbUrl": "http://cdn.eyeem.com/thumb/sq/200/6b982ebb7aca0b5578b4cbf3ef83fd830c8fc63e-1351523338",
          "webUrl": "http://www.eyeem.com/a/23",
          "updated": "2012-10-29T16:09:12+0100"
        }
      },
      "totalPhotos": 9,
      "totalLikers": 0,
      "totalContributors": 7
    },
    "defaultTopics": [
      "Hanging out",
      "Taking photos",
      "Photo",
      "Smile",
      "Check this out",
      "That's me",
      "Hello world",
      "Cheese!",
      "Relaxing",
      "Hi!",
      "Enjoying life"
    ],
    "venues": {
      "offset": 0,
      "limit": 3,
      "total": 3,
      "items": [
        {
          "name": "Mixdorfer Stübchen",
          "serviceId": "4dea111845dd3993a880fa5e",
          "venueServiceName": "foursquare",
          "topics": [
            "German food",
            "Eating",
            "Schweinshaxe",
            "Having a beer",
            "Meat and potatoes",
            "Overdosing on Sauerkraut"
          ],
          "category": "4bf58dd8d48988d10d941735",
          "categoryName": "German Restaurant"
        },
        {
          "name": "Tor zum Schlaubetal",
          "serviceId": "4f11a2d0e4b0044a23655beb",
          "venueServiceName": "foursquare",
          "topics": [
            "On a hike",
            "Mountain goat",
            "Nature",
            "My feet hurt",
            "Walking",
            "Relaxing",
            "Enjoying the sights",
            "Nice views",
            "Take a break"
          ],
          "category": "4bf58dd8d48988d159941735",
          "categoryName": "Hiking Trail"
        },
        {
          "name": "Ragower Mühle",
          "serviceId": "50506182e4b0d81e12ee6988",
          "venueServiceName": "foursquare",
          "topics": [
            "Eating",
            "Great food",
            "Bangers and mash",
            "Pub grub",
            "Fish and chips",
            "Moules et Frites"
          ],
          "category": "4bf58dd8d48988d155941735",
          "categoryName": "Gastropub"
        }
      ]
    }
  }
}
```

 