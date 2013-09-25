# GET /users/#{id}/contacts
***
`/users/#{id}/contacts`

### Description
***
finds eyeem and social media (facebook, twitter) friends.

requires authed user.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the id of the user to share|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**sm**|search for sm friends (facebook,twitter)|boolean||0|
|**eyeem**|search for eyeem users|boolean||0|
|**limit**|num of contacts to return|integer||20|
|**offset**|offset of contacts to start at|integer||0|
|**q**|string to search for (min 3 chars)|string|||

### Response
***