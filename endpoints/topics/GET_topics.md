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
|**offset**|num of topics to return|integer||20|
|**limit**|offset of topics to start at|integer||0|

### Response
***


200 and an array of topics.



[Errors][]

### Examples
***

`http://www.eyeem.com/api/v2/topics?autoComplete=berl&offset=0&limit=20`







[Errors]: 