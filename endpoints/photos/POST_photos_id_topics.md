# POST /photos/#{id}/topics       
***
`/photos/#{id}/topics `

### Description
***
Add a photo to a new topic (which automatically adds it to the album associated with that topic).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**name**| the name of the topic |string|x||


### Response
***


200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/photos/1234/topics?name=funfunfun`


