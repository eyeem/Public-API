# PUT /photos/#{id} 
***
`/photos/#{id}`

### Description
***
Edits a photo by id (has to be a photo belonging to the authenticated user or admin).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want to edit.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**caption**|The new caption of the photo|string|||
|**title**|The new title of the photo|string|||
|**hide**|removes photo from popular album|boolean|||


### Response
***



200 if success


[Errors][]

### Examples
***

`https://www.eyeem.com/api/v2/photos/1234`







[Errors]: 