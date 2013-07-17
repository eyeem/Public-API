#New Endpoints
****
Endpoints to be introduced in V3

##Albums
***
- separate endpoints instead of `onlyId` param.
    - `GET /albums/{id}/favoriterIds`
    - `GET /albums/{id}/contributorIds`
    - `GET /albums/{id}/photoIds`
 
##Apps
***

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
- `POST /missions/{id}/share`
    - params:
        - services = comma-separated (facebook, twitter, tumblr)
        - message = string

##News
****


##Oauth
****


##Photos
****
- separate endpoints instead of `onlyId` param.
    - `GET /photos/{id}/commentsIds`
    - `GET /photos/{id}/albumsIds`

- implement, and call it "people" not "person"
    - `GET /photos/{photo_id}/person/{person_id}`
    - `PUT /photos/{photo_id}/person/{person_id}`
    - `DELETE /photos/{photo_id}/person/{person_id}`

##Search
****


##Topics
****


##Users
****


##Venues
****
