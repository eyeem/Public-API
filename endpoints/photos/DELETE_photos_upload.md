# DELETE /photos/upload/{filename} 
***
`/photos/upload/#{filename}`

### Description
***
Deletes an uploaded filename (only if it hasn't been attached to a photo yet). Used to rollback the `POST /photos/upload` if the upload isn't completed.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**filename**|The filename to be deleted.|string|x||


### Response
***



200 if success

[Errors](../../resources/errors.md#files)
