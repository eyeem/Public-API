# GET /news/#{id} 
***
`/news/#{id}`

### Description
***
retrieve a single news item, requires authenticated user.


### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the news.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**


### Response
***

200 + news object
403 if requesting user isn't authorized to view the item
404 if the item doesn't exist