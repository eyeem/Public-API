# GET /discover/albums   >> X-Api-Version 2.2.0 <<
***


### Description
***
Retrieves a dedicated discover feed (made up ONLY of albums) - tailored to the user's preferences (or a generic one for non-authed endpoints)

### Parameters
***

|parameter| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**limit**|num of items to return|integer||30|
|**offset**|(offset of items to start at|integer||0|
|**lat**|latitude|float| for geo discover ||
|**lng**|longitude|flaot| for geo discover ||
|**includePhotos**|If true, adds photo array to discover items inline|boolean||0|
|**numPhotos**|the number of photos to include for each item|integer||10|
|**includeContributors**|If true, adds album contributor array to discover items inline|boolean||0|
|**includeLikers**|If true, adds album favoriters array to discover items inline|boolean||1|
|**filter**|defines which types of items to return, any of "trending","nearby","favorited","contributed","friendsFavorite","friendsContributed"|string csv|||
|**detailed**|If true, allows for album details to be included|boolean||0|