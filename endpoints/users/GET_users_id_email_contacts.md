# GET /users/#{id}/smContacts
***
`/users/#{id}/smContacts`

### Description
***
check social media accounts for friends (in eyeem, or to invite them)

requires authed user w/ **native** client.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the id of the user to share|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**service**|service to check (facebook,twitter)|string|x||
|**matchContacts**|1=all, 0=eyeem users|boolean||0|
|**type**|defaults to "friends"|string|||
|**detailed**|returns detailed profiles of matches|boolean||1|

### Response
***