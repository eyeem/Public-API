# GET /users
***
`/useres`

### Description
***
Search for users or retrieve suggested users.

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**q**|string to search users by|string|||
|**suggested**|returns suggested users (replaces "q")|boolean||0|
|**ids**|comma-separated list of ids (to be returned as users)|string|||
|**detailed**|rreturns a more detailed user object|boolean||1|
|**friends**|used when getting users from a search query, searches only among friends|boolean||0|
|**limit**|num of search results to return|integer||30|
|**offset**|offset of search results to start at|integer||0|


### Response
***
200, pagination params and a array of user objects (either those queried, or those suggested)

[Errors](../../resources/errors.md)
### Examples
***

`https://www.eyeem.com/api/v2/users?q=ramzi&limit=25&offset=20`



