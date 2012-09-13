#Endpoint: Users
***

These are the API calls that you can use to retrieve users, their photos, friends and other data

**Note: #{id} can be replaced by "me" or by the user's vanity url ex: "ramz" - this applies to all user endpoints.**

##Available endpoints
***

* `/users`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users.md), POST (not available here)
* `/users/#{id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id.md), [POST](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id.md), DELETE (not available yet)
* `/users/#{id}/photos`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_photos.md)
* `/users/#{id}/likedPhotos`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_likedPhotos.md), PUT/POST/DELETE (via [photos](https://github.com/eyeem/API/blob/master/endpoints/photos.md) endpoint)
* `/users/#{id}/friendsPhotos`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_friendsPhotos.md)
* `/users/#{id}/likedAlbums`, GET
* `/users/#{id}/feed`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_feed.md)
* `/users/#{id}/discover`, GET
* `/users/#{id}/friends`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_friends.md), [POST](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_friends.md)
* `/users/#{id}/friends/#{friend_id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_friends_id.md),  [DELETE](https://github.com/eyeem/API/blob/master/endpoints/users/DELETE_users_id_friends_id.md)
* `/users/#{id}/followers`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_followers.md)
* `/users/#{id}/followers/#{friend_id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_followers_id.md)
* `/users/#{id}/topics`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_topics.md)
* `/users/#{id}/socialMedia`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_socialMedia.md)
* `/users/#{id}/socialMedia/{service}`, [POST](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_socialMedia_service.md), [PUT](https://github.com/eyeem/API/blob/master/endpoints/users/PUT_users_id_socialMedia_service.md), [DELETE](https://github.com/eyeem/API/blob/master/endpoints/users/DELETE_users_id_socialMedia_service.md)
* `/users/#{id}/newsSettings`, [GET](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_newsSettings.md), [POST](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_newsSettings.md)
* `/users/#{id}/share`, [POST](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_share.md)
* `/users/#{id}/smContacts`, GET
* `/users/#{id}/emailContacts`, GET, POST
* `/users/#{id}/hide`, POST

##Representation
***

The various possible representations of a user (simple,detailed) are presented and described in the [[model]] page.



##GET
***

* [`/users`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users.md)
* [`/users/#{id}`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id.md)
* [`/users/#{id}/photos`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_photos.md)
* [`/users/#{id}/likedPhotos`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_photos.md)
* [`/users/#{id}/friendsPhotos`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_friendsPhotos.md)
* `/users/#{id}/likedAlbums`
* [`/users/#{id}/feed`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_feed.md)
* `/users/#{id}/discover`
* [`/users/#{id}/friends`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_friend.md) 
* [`/users/#{id}/friends/#{friend_id}`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_friends_id.md) 
* [`/users/#{id}/followers`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_followers.md) 
* [`/users/#{id}/followers/#{friend_id}`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_followers_id.md) 
* [`/users/#{id}/topics`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_topics.md) 
* [`/users/#{id}/socialMedia`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_socialMedia.md) 
* [`/users/#{id}/socialMedia`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_socialMedia.md) 
* [`/users/#{id}/newsSettings`](https://github.com/eyeem/API/blob/master/endpoints/users/GET_users_id_newsSettings.md) 


##PUT
***

* [`/users/#{id}/socialMedia/{service}`](https://github.com/eyeem/API/blob/master/endpoints/users/PUT_users_id_socialMedia_service.md)

##POST
***

* [`/users/#{id}`](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id.md)
* [`/users/#{id}/friends`](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_friend.md) 
* [`/users/#{id}/socialMedia/{service}`](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_socialMedia_service.md) 
* [`/users/#{id}/newsSettings`](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_newsSettings.md) 
* [`/users/#{id}/share`](https://github.com/eyeem/API/blob/master/endpoints/users/POST_users_id_share.md) 

##DELETE
***

* [`/users/#{id}/friends/#{friend_id}`](https://github.com/eyeem/API/blob/master/endpoints/users/DELETE_users_id_friends_id.md) 
* [`/users/#{id}/socialMedia/{service}`](https://github.com/eyeem/API/blob/master/endpoints/users/DELETE_users_id_socialMedia_service.md) 