# GET /albums/collections 
***
`/albums/collections`

### Description
***
Retrieves an array of collections (of generic topics for onboarding)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of favoriters to return|integer||20|
|**offset**|offset of favoriters to start at|integer||0|



### Response
***

200 and and a dictionary containing limit, offset, total and an array of collections