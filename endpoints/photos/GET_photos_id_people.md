# GET /photos/#{id}/people 
***
`/photos/#{id}/people `

### Description
***
Retrieves an array of people tagged in the photo

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of users to return|integer||20|
|**offset**|offset of users to start at|integer||0|



### Response
***


200 and and a dictionary containing limit, offset, total and an array of likers (users)
