#Endpoint: Apps
***

Retrieves and creates Apps that use the EyeEm API. **All endpoints below require an authenticated user with a native app access token.**

##Available endpoints
***
* `/users/#{id}/apps`, [GET](#GETUsersIdApps), [POST](#POSTUsersIdApps)
* `/apps/id`, [GET](#GETAppsId),[PATCH](#PATCHAppsId),[POST](#PATCHAppsId),[PUT](#PATCHAppsId),[DELETE](#DELETEAppsId)
* `/users/#{id}/linkedApps`, [GET](#GETUsersIdLinkedApps)
* `/users/#{id}/linkedApps/#{id}`, [GET](#GETUsersIdLinkedAppsId),[DELETE](#DELETEUsersIdLinkedApps)

##API Calls
****

### GET /users/{id}/apps <a id="wiki-GETUsersIdApps"></a>  

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

### POST /users/{id}/apps <a id="wiki-POSTUsersIdApps"></a>  

Creates a new App.

DESCRIPTION
#### Headers
 - 

#### Parameters
 - name: string (app name), required
 - url: string (app url)
 - redirectUrl: string (oauth redirectUrl)
 - icon: file (app icon), sent in request body

#### Response
 - 200 and an app object
 - error with code and message
 
***

### GET /apps/{id} <a id="wiki-GETAppsId"></a>  

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

### POST|PATCH|PUT /apps/{id} <a id="wiki-PATCHAppsId"></a>  

Updates an app details. Authed user must be app owner. 

DESCRIPTION
#### Headers
 - 

#### Parameters
 - name: string (app name)
 - url: string (app url)
 - redirectUrl: string (oauth redirectUrl)
 - icon: file (app icon)

#### Response
 - 200 and an app object
 - error with code and message
 
***

### DELETE /apps/{id} <a id="wiki-DELETEAppsId"></a>  

Deletes an App. Authed user must be app owner. 

DESCRIPTION
#### Headers
 - 

#### Parameters
 -

#### Response
 - 200
 - error with code and message

***

### GET /users/{id}/linkedApps <a id="wiki-GETUsersIdLinkedApps"></a>

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

### GET /users/{id}/linkedApps/{id} <a id="wiki-GETUsersIdLinkedAppsId"></a>

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


### DELETE /users/{id}/linkedApps/{id} <a id="wiki-DELETEUsersIdLinkedAppsId"></a>

Unlinks an app (invalidates its access token)

DESCRIPTION
#### Headers
 - 

#### Parameters
 - 

#### Response
 - 200 if success
 - error with code and message
