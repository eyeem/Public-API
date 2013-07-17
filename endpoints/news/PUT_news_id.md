# GET /news/#{id} 
***
`/news/#{id}`

### Description
***
Updates a news item by id and sets it (and optionally, all items older than it) to "seen".


### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the news.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**include_older**|if true, marks all older news items as "seen"|boolean|||




### Response
***


200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/news/1234`



 