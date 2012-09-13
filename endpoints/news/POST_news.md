# POST /news 
***
`/news`

### Description
***
Marks multiple news items as read.


### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the news.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**markAsRead**|comma separated ids of news to be marked|string|x||


### Response
***

200

[Errors](../../resources/errors.md)
### Examples
***

`http://www.eyeem.com/api/v2/news?markAsRead=1,2,3,4,5`




 