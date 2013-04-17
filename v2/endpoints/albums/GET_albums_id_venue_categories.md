# GET /albums/id/venueCategories
***
`/albums/#{id}/venueCategories`

### Description
***
Retrieves the venueCategories available for a certain city

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**| the id of the album|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|



### Response
***

200 and an array of album objects, includes pagination parameters


[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/albums/17/venueCategories`

```json

{
  "categories": [
    {
      "id": "4bf58dd8d48988d103941735",
      "parent_id": "4e67e38e036454776db1fb3a",
      "name": "Home (private)",
      "depth": 2,
      "count": 312
    },
    {
      "id": "4bf58dd8d48988d16d941735",
      "parent_id": "4d4b7105d754a06374d81259",
      "name": "Café",
      "depth": 2,
      "count": 311
    },
    {
      "id": "4bf58dd8d48988d124941735",
      "parent_id": "4d4b7105d754a06375d81259",
      "name": "Office",
      "depth": 2,
      "count": 293
    },
    {
      "id": "4bf58dd8d48988d116941735",
      "parent_id": "4d4b7105d754a06376d81259",
      "name": "Bar",
      "depth": 2,
      "count": 238
    }
  ]
}
```



