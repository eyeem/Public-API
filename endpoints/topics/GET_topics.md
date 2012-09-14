# GET /topics    
***
`/topics`

### Description
***
Retrieves an array containing a users and an albums dictionary.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**autoComplete**||string|x||


### Response
***


200 and an array of topics.

[Errors](../../resources/errors.md#files)
### Examples
***

`http://www.eyeem.com/api/v2/topics?autoComplete=be`


```javascript


{
  "topics": {
    "offset": 0,
    "total": 30,
    "limit": 30,
    "items": [
      {
        "name": "beach",
        "totalPhotos": "1681"
      },
      {
        "name": "Berlin",
        "totalPhotos": "888"
      },
      {
        "name": "Beer",
        "totalPhotos": "879"
      },
      {
        "name": "summer vibes",
        "totalPhotos": "651"
      },
      {
        "name": "Beauty of decay",
        "totalPhotos": "369"
      },
      {
        "name": "Being adventurous",
        "totalPhotos": "317"
      },
      {
        "name": "EyeEm Berlin Meetup",
        "totalPhotos": "271"
      },
      {
        "name": "Beautiful",
        "totalPhotos": "169"
      },
      {
        "name": "Being creative",
        "totalPhotos": "161"
      },
      {
        "name": "Beautiful day",
        "totalPhotos": "156"
      },
      {
        "name": "Cerberus",
        "totalPhotos": "138"
      },
      {
        "name": "Startupbootcamp Berlin 2012",
        "totalPhotos": "136"
      },
      {
        "name": "Being entertained",
        "totalPhotos": "115"
      },
      {
        "name": "best friends",
        "totalPhotos": "99"
      },
      {
        "name": "Kreuzberg",
        "totalPhotos": "91"
      },
      {
        "name": "beauty",
        "totalPhotos": "89"
      },
      {
        "name": "somewhere i remember",
        "totalPhotos": "86"
      },
      {
        "name": "Febe",
        "totalPhotos": "83"
      },
      {
        "name": "Life is a beach",
        "totalPhotos": "77"
      },
      {
        "name": "urbex",
        "totalPhotos": "74"
      },
      {
        "name": "Lunch Beat",
        "totalPhotos": "67"
      },
      {
        "name": "on the beach",
        "totalPhotos": "66"
      },
      {
        "name": "VESPA Bella",
        "totalPhotos": "58"
      },
      {
        "name": "drinking beer",
        "totalPhotos": "56"
      },
      {
        "name": "beachphotography",
        "totalPhotos": "54"
      },
      {
        "name": "Fussball ist unser Leben",
        "totalPhotos": "53"
      },
      {
        "name": "Being Productive",
        "totalPhotos": "50"
      },
      {
        "name": "strawberry",
        "totalPhotos": "50"
      },
      {
        "name": "The world's best startup",
        "totalPhotos": "49"
      },
      {
        "name": "bebe moment",
        "totalPhotos": "48"
      }
    ]
  }
}


```


