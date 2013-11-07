#Endpoint: Mission
***

Retrieves current ongoing photo missions

##Available endpoints
***
* `/missions/lightweight`, [GET](#GETMissionsLightweight)


### GET /missions/lightweight <a id="GETMissionsLightweight"></a>  

temporary endpoint returning wrapped albums until missions are properly implemented

DESCRIPTION
#### Headers

#### Parameters
- offset = int (default 0)
- limit = int (default 0)
- detailed = bool (default 1)
- includePhotos = bool (default 1)
- numPhotos = int (default 7, requires detailed=1 & includePhotos=1)
- includeLikers = bool (default 0, requires detailed=1)
- includeContributors = bool (default 0, requires detailed=1)

#### Response
 - 200 and an array of mission objects
 - error with code and message