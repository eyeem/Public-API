# GET /albums/recommended
***
`/albums/recommended`

### Description
***
Retrieves albums recommended by the EyeEm community team.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of albums to return|integer||60|



### Response
***

200 and an array of album objects, includes pagination parameters


[Errors][]

### Examples
***

`https://www.eyeem.com/api/v2/albums/recommended?limit=20`









[Errors]: 