# GET /albums/onboarding 
***
`/albums/onboarding`

### Description
***
Retrieves an array of onboarding sets (of generic topics for onboarding)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**parameter**| **description**| **type** |**required?** |**default**|
|**limit**|num of sets to return|integer||20|
|**offset**|offset of sets to start at|integer||0|



### Response
***

200 and and a dictionary containing limit, offset, total and an array of collections