#Existing Endpoints
****
Changes and notes on existing endpoints.

##Albums
***

##Apps
***
- `GET /users/{id}/apps`
    - replace with `GET /apps` since user is authed anyway?

- `POST /users/{id}/apps`
    - replace with `POST /apps` since user is authed anyway?

- `GET /users/{id}/tokens`
    - returns a user's own active access_tokens
    - undocumented and not active
    - requires authenticated user with native app access token

- `GET /users/{user_id}/linkedApps`
    - a case for using type="linked" in `GET /apps`

- `GET /users/{user_id}/linkedApps/{app_id}`
    - also for DELETE
    - rename to /apps/{id}/token (GET/DELETE/POST)

##Auth
***

##Default
****


##Discover
****


##Experimental
****


##Missions
****


##News
****


##Oauth
****


##Photos
****


##Search
****


##Topics
****


##Users
****


##Venues
****
- `GET /venues/search`
    - should be only available to native clients.
- `POST /venues`
    - categories not used if service=eyeem (which is now always the case!)
    - can we optimize this?
    - check for duplicates?
    - creation no longer allowed on foursquare - in this case the id provided must already be a valid venue on foursquare