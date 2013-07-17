#Deprecated and unused endpoints
****
All these endpoinds need to be removed from codebase in API V3

what's the status with these two headers?
- X-GEO-closestVenueFsIds
- X-GEO-cityName 

looks like they're needed in `/users/{id}/feed`. Anywhere else? that endpoint still relevant?


##Albums
***
- `POST /albums/{album_id}/invites`
    - deprecated. remove!

- `POST /albums/{album_id}/discover`
    - no longer doing facebook discovery

- `POST | GET /albums/{id}/likers`
    - should now be called favoriters. no need to support both any more.
    - deprecate `POST /users/{id}/likedAlbums`

- `POST | PUT | DELETE /albums/{id}/likers/{user_id}`
    - should now be called favoriters. no need to support both any more.

- `GET /albums/{id}/activities`
    - not implemented. not needed. kill

- `GET /albums/{id}/comments`
    - not implemented. not needed. kill

- `GET /collections/{radius}`
    - implement proper collections, in a separate module!

- `POST /albums`
    - non-existent. kill.

* popular album: `/albums/dynamic:10`
* radius album: `/albums/radius:#{latitude}:#{longitude}`

- GET | POST /albums/{id}/favoriters
    - implementation should be in there, not forwarded to likers
    - user_id param is unnecessary since this endpoints requires an authenticated user

- `POST /albums/#{id}/favoriters`
    - redundant, use PUT. kill.
    - removed from documentation. needs removal from code.

- `DELETE /albums/{album_id}/likers/{user_id}`
    - replaced with `/albums/{album_id}/favoriters/{user_id}`

- `PUT | DELETE /albums/#{id}`
    - don't really exist. remove from codebase.

- `GET /albums/{id}`
    - rename likers to favoriters.

- `GET /albums/recommended`
    - no longer in use (was for old topic recommendations in onboarding)

- `POST /albums/#{id}/photos`
    - just use the PUT equivalent.


##Apps
***

##Auth
***
- `POST /auth/signin` : duplicate
- `POST /auth/signOut`: duplicate
- `POST /auth/ok`: better ways to track!
- `GET /auth/ok`: better ways to ping server!
- `POST /auth/error`: shouldn't be in use.


##Default
****


##Discover
****

##Invitations
****
- endpoint out of use. remove completely.

##Experimental
****


##Missions
****


##News
****

- deprecate the current `GET /news` > model doesn't relate
- deprecate "oldAggregatedNews"

##Oauth
****


##Photos
****
- `GET /photos/bgImages`
    - kill this!

- `POST /photos/{id}/topics`
    - deprecated. kill this

- `POST /photos/{id}/discover`
    - no longer posting discover actions. kill.

- `POST /users/{user_id}/likedPhotos`
- `POST /photos/{id}/likers`
    - need only one endpoint for liking photos. `PUT /photos/{id}/likers/{user_id}`

- renamed `taggedPeople` to `people`. remove:
    - GET /photos/{photo_id}/taggedPeople
    - PUT /photos/{photo_id}/taggedPeople
    - DELETE /photos/{photo_id}/taggedPeople
- `GET | PUT | DELETE /photos/{id}/albums/{id}` should be in `/albums` where it's actually implemented.


##Search
****


##Topics
****

- remove "topics" from internal lexicon!
- completely remove this endpoint. search via /albums or /search!

##Users
****

- `POST | PATCH | PUT /users/#{id}`
    - notifications and timeline parameters are dead.

- `POST /users/{user_id}/photos`
    - is duplicate to `POST /photos`: remove here!
- `POST | PATCH | PUT /users/{id}`
    - don't need all of these!

- remove `/users/{id}/likedAlbums` from codebase (now called "favoritedAlbums")

- `GET | PUT | DELETE /users/{follower_id}/followers/{user_id}`
    - kill this retarded routing: '/*/followers/*' => array('action' => 'follow', 'follower_id' => '$1', 'user_id' => '$2')

- `GET /users/{id}/followings`
    - duplicate, forwards to `friends`. kill.

- POST | DELETE /users/{id}/likedPhotos >> kill or keep for batch posts/deletes?

- `GET /users/{id}/settings` and `POST /users/{id}/settings`
    - doc says they're deprecated, traffic shows they're still getting called.

- /users/{id}/discover ???

- `/users/#{id}/newsSettings` deprecated (GET/PATCH/PUT/POST) > forwards to users.flags

- `POST /users/{id}/emailContacts`
    - identical to GET

- `POST /users/{id}/likedPhotos`
    - this forwards to photos.addLiker
    - remove it. unless we want to do batch!

- https://api.eyeem.com/v2/users/me/feed
    -   deprecated, isn't it?




##Venues
****
- `POST /venues/foursquare`
 - note: reintroduce for users with foursquare tokens?