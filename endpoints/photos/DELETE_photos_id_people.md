# DELETE /photos/#{id}/people   
***
`/photos/#{id}/people`

### Description
***
Removes a tagged person(s) from a photo. acting user is photo owner, tagged person, or Admin.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo we want post a comment.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**person**| key:value ("eyeem":"eyeem_id","facebook":"fb_id","twitter":"tw_id") |string (person obj)|x||
|**offense**| reason for removing ("other","spam","don't like") |string|x||

### Response
***


200 and a comment object