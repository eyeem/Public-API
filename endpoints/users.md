#Endpoint: Users
***

These are the API calls that you can use to retrieve users, their photos, friends and other data

**Note: #{id} can be replaced by "me" or by the user's vanity url ex: "ramz" - this applies to all user endpoints.**

##Available endpoints
***

* `/users`, [GET](users/GET_users.md), POST (not available here)
* `/users/#{id}`, [GET](users/GET_users_id.md), [POST](users/POST_users_id.md), DELETE (not available yet)
* `/users/#{id}/photos`, [GET](users/GET_users_id_photos.md)
* `/users/#{id}/likedPhotos`, [GET](users/GET_users_id_likedPhotos.md), PUT/POST/DELETE (via [photos](https://github.com/eyeem/API/blob/master/endpoints/photos.md) endpoint)
* `/users/#{id}/friendsPhotos`, [GET](users/GET_users_id_friendsPhotos.md)
* `/users/#{id}/likedAlbums`, GET
* `/users/#{id}/feed`, [GET](users/GET_users_id_feed.md)
* `/users/#{id}/discover`, GET
* `/users/#{id}/friends`, [GET](users/GET_users_id_friends.md), [POST](users/POST_users_id_friends.md)
* `/users/#{id}/friends/#{friend_id}`, [GET](users/GET_users_id_friends_id.md),  [DELETE](users/DELETE_users_id_friends_id.md)
* `/users/#{id}/followers`, [GET](users/GET_users_id_followers.md)
* `/users/#{id}/followers/#{friend_id}`, [GET](users/GET_users_id_followers_id.md)
* `/users/#{id}/topics`, [GET](users/GET_users_id_topics.md)
* `/users/#{id}/socialMedia`, [GET](users/GET_users_id_socialMedia.md)
* `/users/#{id}/socialMedia/{service}`, [POST](users/POST_users_id_socialMedia_service.md), [PUT](users/PUT_users_id_socialMedia_service.md), [DELETE](users/DELETE_users_id_socialMedia_service.md)
* `/users/#{id}/newsSettings`, [GET](users/GET_users_id_newsSettings.md), [POST](users/POST_users_id_newsSettings.md)
* `/users/#{id}/share`, [POST](users/POST_users_id_share.md)
* `/users/#{id}/smContacts`, GET
* `/users/#{id}/emailContacts`, GET, POST
* `/users/#{id}/hide`, POST

##Representation
***

The various possible representations of a user (simple,detailed) are presented and described in the [model](../resources/model.md) page.



##GET
***

* [`/users`](users/GET_users.md)
* [`/users/#{id}`](users/GET_users_id.md)
* [`/users/#{id}/photos`](users/GET_users_id_photos.md)
* [`/users/#{id}/likedPhotos`](users/GET_users_id_photos.md)
* [`/users/#{id}/friendsPhotos`](users/GET_users_id_friendsPhotos.md)
* `/users/#{id}/likedAlbums`
* [`/users/#{id}/feed`](users/GET_users_id_feed.md)
* `/users/#{id}/discover`
* [`/users/#{id}/friends`](users/GET_users_id_friend.md) 
* [`/users/#{id}/friends/#{friend_id}`](users/GET_users_id_friends_id.md) 
* [`/users/#{id}/followers`](users/GET_users_id_followers.md) 
* [`/users/#{id}/followers/#{friend_id}`](users/GET_users_id_followers_id.md) 
* [`/users/#{id}/topics`](users/GET_users_id_topics.md) 
* [`/users/#{id}/socialMedia`](users/GET_users_id_socialMedia.md) 
* [`/users/#{id}/socialMedia`](users/GET_users_id_socialMedia.md) 
* [`/users/#{id}/newsSettings`](users/GET_users_id_newsSettings.md) 


##PUT
***

* [`/users/#{id}/socialMedia/{service}`](users/PUT_users_id_socialMedia_service.md)

##POST
***

* [`/users/#{id}`](users/POST_users_id.md)
* [`/users/#{id}/friends`](users/POST_users_id_friend.md) 
* [`/users/#{id}/socialMedia/{service}`](users/POST_users_id_socialMedia_service.md) 
* [`/users/#{id}/newsSettings`](users/POST_users_id_newsSettings.md) 
* [`/users/#{id}/share`](users/POST_users_id_share.md) 

##DELETE
***

* [`/users/#{id}/friends/#{friend_id}`](users/DELETE_users_id_friends_id.md) 
* [`/users/#{id}/socialMedia/{service}`](users/DELETE_users_id_socialMedia_service.md) 