# PUT /photos/#{id}/people   
***
`/photos/#{id}/people`

### Description
***
Adds a new tagged person(s) to a photo.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want post a comment.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**person**| key:value ("eyeem":"eyeem_id","facebook":"fb_id","twitter":"tw_id") |string (person obj)|x||

### Response
***


200 and a comment object