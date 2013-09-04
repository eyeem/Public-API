#Endpoint: Mission
***

Retrieves current ongoing photo missions

##Available endpoints
***
* `/missions/lightweight`, [GET](#GETMissionsLightweight), [DELETE](#DELETEMissionsLightweight), [POST](#POSTMissionsLightweight)


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
 
***

### DELETE /missions/lightweight <a id="DELETEMissionsLightweight"></a>  

temporary endpoint deleting wrapped albums until missions are properly implemented. Only available to admins.

DESCRIPTION
#### Headers

#### Parameters
- id = int (required)

#### Response
 - 200 and an array of mission objects
 - error with code and message
 
***

### POST /missions/lightweight <a id="POSTMissionsLightweight"></a>  

temporary endpoint creating wrapped albums until missions are properly implemented

DESCRIPTION
#### Headers

#### Parameters
- id = int (required, album id)
- description = string (required, description of the mission)
- name = string (required, the label for the description)
- url = string (required, url to link to in the mission)
- filename = filename of the image to use as mission header (required)

#### Response
 - 200 and an array of mission objects
 - error with code and message
 
***
