# GET /users
***
`/useres`

### Description
***
Search for users or retrieve suggested users. either "suggested",or "q", or "ids".

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**suggested**|returns suggested users (replaces "q")|boolean||0|
|**q**|string to search users by|string|||
|**friends**|used when getting users from a search query, searches only among friends|boolean||0|
|**followers**|used when getting users from a search query, searches only among followers|boolean||0|
|**ids**|comma-separated list of ids (to be returned as users)|string|||
|**detailed**|rreturns a more detailed user object|boolean||1|
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|
|**action_id**|action id of the facebook action; returns the user who created that action|string|||


### Response
***
200, pagination params and a array of user objects (either those queried, or those suggested)

[Errors](../../resources/errors.md#files)

### Examples
***

`https://api.eyeem.com/v2/users?q=ramzi&limit=25`
