# PUT /photos/#{id}  (also PATCH or POST)   >> X-Api-Version 2.2.0 <<
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
|**description**|String (could contain tag albums in the form of \[a:{id}\]|string|||
|**hide**|removes photo from popular album|boolean|||
|**deleteAlbumIds**|remove a photo from venue/city/country/tag|csv int|||

### Response
***



200 if success

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/photos/1234`




