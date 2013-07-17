#Existing Endpoints
****
Changes and notes on existing endpoints.

##Albums
***

- `GET /albums`
    - introduce types
        - 'trending'    
        - 'ids', requires values= CSV album ids
        - 'search' requires values = search string
        - 'top' (forwards to experimental.topAlbums)
        - 'venueCategory' (forwards to experimental.albumVenuesByCategory)
        - top forwards to experimental.topAlbums => is that clear?
        - top also optionally makes use of `type` 


- separate endpoint for onlyId
    - `GET /albums/{id}/favoriters`
    - `GET /albums/{id}/photos`
    - `GET /albums/{id}/contributors`

- `GET /albums/{id}/photos`
    - merge `order` and `sort` params

- `GET /albums/{id}/venueCategories`
    - forwards to experimental.albumVenueCategories, promote to main endpoint

- `GET /albums/{id}/relatedAlbums`
    - forwards to experimental.relatedAlbums, promote to main endpoint
    - rename according to REST principles.

- `GET /collections`
    - move to separate endpoints
    - more types: radius, popular, etc

- `PUT | DELETE /albums/{id}/photos/{photo_id}`
    - make available to admins as well


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

- everywhere: transforming parameters is stupid
    - /auth/facebook/login, /auth/login, /auth/signup

- `GET /auth/socialServiceKeys`
    - feels unsafe - we're sending important keys over the air!

- `POST|DELETE /auth/deleteUser`
    - requires authed admin, or own user.
    - is this safe? getTargetUser returns the active user (if not provided with user_id)

- `GET /auth/resetPassword`
    - what's the point of this endpoint?

- `POST /auth/push`
    - gcm should be default everywhere
    - check logic here - is it all still ok?
- remove `POST /auth/checkEmail` and `POST /auth/checkNickname`: better as GET
- remove `POST /auth/confirmEmail`: better as POST
- `DELETE | POST /auth/deleteUser`: formatting not optimal.
    - also, safe? getTargetUser()???

##Default
****


##Discover
****
- `GET /discover`
    - `GET /users/{id}/discover` forwards here > deprecate duplicate endpoint
    - better pagination
    - introduce fields

- `GET /discover/albums`
    - better pagination
    - introduce fields
    - album favoriters instead of album likers
    - standardized defaults (For fields/sub-fields)
    - deduplicate code from `GET /discover`
    - `GET /users/{id}/discoverAlbums` forwards here > deprecate duplicate endpoint
    
##Experimental
****


##Missions
****


##News
****
- move /news/aggregated to /news

##Oauth
****


##Photos
****

- stop parameter transition in v3 (ex for comments)

- `PATCH photos/{id}/comments/{id}`
    - necessary? if so, does it update mentioned people etc properly?

- @mentions: standardize formatting (make the same as albums in photo description? or other way round?)

- `PATCH | POST | PUT /photos/{id}`
    - bizarre endpoint. `hide` doesn't belong here
    - people handling doesn't really work
    - deleteAlbumIds ???

- `GET /photos`
    - type = bool (!!!!! should be type="popular")
    - if frames and/or filter param is set, forwards to experimental.searchPhotosByFrameFilter
    - if date is set, forwards to experimental.searchPhotosByDate
    - eventually move to collections endpoint?
    - introduce types (popular(?),date,ids, frame/filter)
    - List Filter/Frame names. (in documentation?)

- `POST /photos`
    - add original photo creation timestamp (from exif)
    - timezone?

- `GET /photos/{id}/people`
    - better logic for the "person" object in v3 (can't keep making fb/tw ids public)

- `PUT /photos/{id}/people` >> or should this be a POST


##Search
****


##Topics
****


##Users
****

- settings vs flags vs newssettings?!

- `/users/#{id}/favoritedAlbums` 
    - `POST` is redundant (available in `/albums`)
        - but what to do with favoriting multiple albums at once (csv album_ids)
    - `GET` remove `subtitle` from codebase.

- separate endpoint for onlyId:
    -  likedPhotos
    -  photos
    -  friendPhotos
    -  favoritedAlbums
    -  followers
    -  friends

- public endpoints that can be blocked: (from francois)
    - `users/{id}/friends`
    - `/users/{id}/favoritedAlbums`
    - `/users/{id}/followers`
    - `/users/{id}/friendsPhotos`

- `POST /users`
    - native scope
    - nickname required

- `GET /users`
    - action_ids needs to be somewhere else
    - unify params!
    - introduce fields/subfields
    - introduce filters
    - better pagination!
    - introduce types (q,suggested,ids,etc)

- sm_contacts and email_contacts are disgusting!

- `GET /users/{id}/emailContacts`
    - more secure implementation of this

- `GET /users/{id}/smContacts`
    - what do the params do?

- `GET /users/{id}/topics`
    - replace with albums
    - add album Ids

- need to cleanup /socialMedia/{service} endpoints.... too complicated

- move all endpoints dealing with external services to "native" app scope.

- `GET /users/{id}/photos`
    - merge `order` and `sort` params (?)

- https://api.eyeem.com/v2/users/me/feed
    -   deprecated, isn't it?


##Venues
****
- `GET /venues/search`
    - should be only available to native clients.
- `POST /venues`
    - categories not used if service=eyeem (which is now always the case!)
    - can we optimize this?
    - check for duplicates?
    - creation no longer allowed on foursquare - in this case the id provided must already be a valid venue on foursquare