# POST /photos/upload 
***
`/photos/upload `

### Description
***
Upload a photo file and send back a filename that can then be use to call POST /photos and create a photo object..

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**photo**||file|x||

### Response
***

201 and filename

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/photos/upload`


