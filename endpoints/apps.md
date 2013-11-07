#Endpoint: Apps
***

Retrieves and creates Apps that use the EyeEm API. **All endpoints below require an authenticated user with a native app access token.**

##Available endpoints
***
* `/users/#{id}/apps`, [GET](#GETUsersIdApps)
* `/apps/id`, [GET](#GETAppsId)
* `/users/#{id}/linkedApps`, [GET](#GETUsersIdLinkedApps)
* `/users/#{id}/linkedApps/#{id}`, [GET](#GETUsersIdLinkedAppsId),[DELETE](#DELETEUsersIdLinkedApps)

##API Calls
****

### GET /users/{id}/apps <a id="GETUsersIdApps"></a>  

Gets a user's created apps

DESCRIPTION
#### Headers
 - 

#### Parameters
 - 

#### Response
 - 200 and an array of App objects
 - error with code and message
 
***

### GET /apps/{id} <a id="GETAppsId"></a>  

Gets the details of a specific app. **Available to native clients w/out authentication.**

DESCRIPTION
#### Headers
 - 

#### Parameters
 - 

#### Response
 - 200 and an app object
 - error with code and message
 
***

### GET /users/{id}/linkedApps <a id="GETUsersIdLinkedApps"></a>

Gets a user's linked apps

DESCRIPTION
#### Headers
 - 

#### Parameters
 - 

#### Response
 - 200 and an array of App objects
 - error with code and message
 
***

### GET /users/{id}/linkedApps/{id} <a id="GETUsersIdLinkedAppsId"></a>

Checks if a user has linked a certain app.

DESCRIPTION
#### Headers
 - 

#### Parameters
 - 

#### Response
 - 200 if linked
 - 400 if not linked
 - error with code and message
 
***