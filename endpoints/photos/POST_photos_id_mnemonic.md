# POST /photos/#{id}/mnemonic      
***
`/photos/#{id}/mnemonic`

### Description
***
Return the mnemonic rating results of flagged photos

The endpoint is only available for requests from X-Client-Id of App 291.
The params are in the body (json)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo to be rated.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**result**|The result of rating ("rejected","approved")|string|x||


### Response
***


200 if success

[Errors](../../resources/errors.md#files)
### Examples
***

`https://api.eyeem.com/v2/photos/1234/flag?offense=Copyright`



