# GET /albums/id/weather
***
`/albums/#{id}/weather`

### Description
***
Retrieves the weather in a certain city. works only for city/venue albums.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**date**|returns photos taken on a specific date (YYYY-MM-DD)|date||TODAY|



### Response
***

200 and a dictionary containing temperature and weather code.