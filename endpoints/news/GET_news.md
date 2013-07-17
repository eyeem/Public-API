# GET /news 
***
`/news`

### Description
***
Retrieves the authenticated user's latest twenty news items.


### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of news items to return|integer||20|
|**offset**|offset of news imtes to start at|integer||0|
|**aggregated**|returns aggregated news if set|boolean||0|
|**countUnseen**|returns only the number of unread news|boolean||0|

### Response
***

200 and a dictionary containing pagination info and an array of news items.


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/news?offset=0&limit=20`

 