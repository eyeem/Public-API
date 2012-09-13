# GET /photos/#{id}/likers 
***
`/photos/#{id}/likers `

### Description
***
Retrieves an array of the users who like the photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want information about.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of users to return|integer||20|
|**offset**|offset of users to start at|integer||0|
|**onlyId**| if true, returns only the likers ids|boolean|||



### Response
***


200 and and a dictionary containing limit, offset, total and an array of likers (users)


[Errors][]

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234/likers?offset=0&limit=5`







[Errors]: 