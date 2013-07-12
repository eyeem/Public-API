# POST /photos/#{id}/flag      
***
`/photos/#{id}/flag`

### Description
***
Report a photo to EyeEm moderators.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|The id of the photo to flag.|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**offense**|The reason for flagging the photo (Pornographic, Terms of Service, Copyright).|string|x||


### Response
***


200 if success

[Errors](../../resources/errors.md#files)
### Examples
***

`https://api.eyeem.com/v2/photos/1234/flag?offense=Copyright`



