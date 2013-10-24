# GET /search/albums    
***
`/search/albums`

### Description
***
Retrieves an array containing albums.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|the keyword to search|string|x||
|**limit**|num of items to return|integer||10|
|**offset**|(offset of items to start at|integer||0|
|**city_id**| filter by a specific city|string|||
|**album_type**| return albums of a specific type only (city,country,event,venue,tag) |string|||
|**detailed**|whether to include album details in the results (photos, contributors, etc)|boolean||0|

### Response
***

200 and an array containing albums