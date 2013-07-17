# GET /news 
***
`/news`

### Description
***
Retrieves the authenticated user's news items (aggregated), either the latest items, or any items newer than `newestId` or any items older than `oldestId`.


### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of news items to return|integer||30|
|**oldestId**|get X items older than this id|integer||0|
|**newestId**|get X items newer than this id|integer||0|

### Response
***

200 and a dictionary containing pagination info and an array of news items.