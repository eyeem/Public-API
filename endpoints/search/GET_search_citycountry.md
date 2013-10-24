# GET /search/citycountry    
***
`/search/citycountry`

### Description
***
Retrieves an array containing cities and/or countries

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|the keyword to search|string|x||
|**limit**|num of items to return|integer||10|
|**offset**|(offset of items to start at|integer||0|

### Response
***

200 and an array containing cities and/or countries