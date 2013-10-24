# GET /users/#{id}/facebookPages    
***
`/users/#{id}/facebookPages`

### Description
***
Only available for the authenticated user, this call returns a service object with the Facebook pages of the user.

### Parameters
***
|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to retrieve information from|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**page_id**|id of the page or "me"|string|x||

### Response
***

200 and a services object


[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users/me/facebookPages`


```json
{
  "services": {
    "facebook": {
      "third_party_id": "4Ci6GTRNyX8vIWfBBM1n09m9JdQ",
      "id": "100000492297860",
      "upload": false,
      "photolike": true,
      "photodiscover": false,
      "photocomment": false,
      "albumlike": false,
      "userfollow": false,
      "timelinepopup": true,
      "managedPages": [
        {
          "id": "154793581210614",
          "name": "Halö",
          "posting": 0
        }
      ],
      "status": "active"
    },
    "twitter": {
      "id": "19140455",
      "nickname": "ksslng",
      "status": "active"
    },
    "tumblr": {
      "status": "inactive"
    },
    "foursquare": {
      "status": "active"
    },
    "flickr": {
      "status": "inactive"
    }
  }
}

```