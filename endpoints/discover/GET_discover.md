# GET /discover   >> X-Api-Version 2.2.0 <<
***


### Description
***
Retrieves a dedicated discover feed - tailored to the user's preferences (or a generic one for non-authed endpoints)

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of items to return|integer||30|
|**user_id**|return a different user's discover (admins only)|integer|||
|**offset**|(offset of items to start at|integer||0|
|**lat**|latitude|float| for geo discover ||
|**lng**|longitude|flaot| for geo discover ||
|**includePhotos**|If true, adds photo array to discover items inline|boolean||1|
|**numPhotos**|the number of photos to include for each item|integer||6|
|**city**|current city name (from client device)|string|||
|**cc**|current country code (from client device)|string|||
|**filter**|defines which types of items to return, any of "trending","nearby","favorited","contributed","friendsFavorite","friendsContributed"|string csv|||