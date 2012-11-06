#Endpoint: Users
***

These are the API calls that you can use to retrieve users, their photos, friends and other data

**Note: #{id} can be replaced by "me" or by the user's vanity url ex: "ramz" - this applies to all user endpoints.**

##Available endpoints
***

* `/users`, [GET](users/GET_users.md#files), POST (not available here)
* `/users/#{id}`, [GET](users/GET_users_id.md#files), [POST](users/POST_users_id.md#files), DELETE (not available yet)
* `/users/#{id}/photos`, [GET](users/GET_users_id_photos.md#files)
* `/users/#{id}/likedPhotos`, [GET](users/GET_users_id_likedPhotos.md#files), PUT/POST/DELETE (via [photos](https://github.com/eyeem/API/blob/master/endpoints/photos.md#files) endpoint)
* `/users/#{id}/friendsPhotos`, [GET](users/GET_users_id_friendsPhotos.md#files)
* `/users/#{id}/likedAlbums`, GET
* `/users/#{id}/feed`, [GET](users/GET_users_id_feed.md#files)
* `/users/#{id}/discover`, GET
* `/users/#{id}/friends`, [GET](users/GET_users_id_friends.md#files), [POST](users/POST_users_id_friends.md#files)
* `/users/#{id}/friends/#{friend_id}`, [GET](users/GET_users_id_friends_id.md#files),  [DELETE](users/DELETE_users_id_friends_id.md#files)
* `/users/#{id}/followers`, [GET](users/GET_users_id_followers.md#files)
* `/users/#{id}/followers/#{friend_id}`, [GET](users/GET_users_id_followers_id.md#files)
* `/users/#{id}/topics`, [GET](users/GET_users_id_topics.md#files)
* `/users/#{id}/socialMedia`, [GET](users/GET_users_id_socialMedia.md#files)
* `/users/#{id}/socialMedia/{service}`, [POST](users/POST_users_id_socialMedia_service.md#files), [PUT](users/PUT_users_id_socialMedia_service.md#files), [DELETE](users/DELETE_users_id_socialMedia_service.md#files)
* `/users/#{id}/facebookPage`, [POST](users/POST_users_id_facebookPage.md#files) 
* `/users/#{id}/newsSettings`, [GET](users/GET_users_id_newsSettings.md#files), [POST](users/POST_users_id_newsSettings.md#files)
* `/users/#{id}/share`, [POST](users/POST_users_id_share.md#files)
* `/users/#{id}/smContacts`, GET
* `/users/#{id}/emailContacts`, GET, POST
* `/users/#{id}/hide`, POST

##Representation
***

The various possible representations of a user (simple,detailed) are presented and described in the [model](../resources/model.md#files) page.



##GET
***

* [`/users`](users/GET_users.md#files)
* [`/users/#{id}`](users/GET_users_id.md#files)
* [`/users/#{id}/photos`](users/GET_users_id_photos.md#files)
* [`/users/#{id}/likedPhotos`](users/GET_users_id_photos.md#files)
* [`/users/#{id}/friendsPhotos`](users/GET_users_id_friendsPhotos.md#files)
* `/users/#{id}/likedAlbums`
* [`/users/#{id}/feed`](users/GET_users_id_feed.md#files)
* `/users/#{id}/discover`
* [`/users/#{id}/friends`](users/GET_users_id_friends.md#files) 
* [`/users/#{id}/friends/#{friend_id}`](users/GET_users_id_friends_id.md#files) 
* [`/users/#{id}/followers`](users/GET_users_id_followers.md#files) 
* [`/users/#{id}/followers/#{friend_id}`](users/GET_users_id_followers_id.md#files) 
* [`/users/#{id}/topics`](users/GET_users_id_topics.md#files) 
* [`/users/#{id}/socialMedia`](users/GET_users_id_socialMedia.md#files) 
* [`/users/#{id}/socialMedia`](users/GET_users_id_socialMedia.md#files) 
* [`/users/#{id}/newsSettings`](users/GET_users_id_newsSettings.md#files) 


##PUT
***

* [`/users/#{id}/socialMedia/{service}`](users/PUT_users_id_socialMedia_service.md#files)

##POST
***

* [`/users/#{id}`](users/POST_users_id.md#files)
* [`/users/#{id}/friends`](users/POST_users_id_friend.md#files) 
* [`/users/#{id}/socialMedia/{service}`](users/POST_users_id_socialMedia_service.md#files) 
* [`/users/#{id}/newsSettings`](users/POST_users_id_newsSettings.md#files) 
* [`/users/#{id}/share`](users/POST_users_id_share.md#files) 
* [`/users/#{id}/facebookPage`](users/POST_users_id_facebookPage.md#files) 


##DELETE
***

* [`/users/#{id}/friends/#{friend_id}`](users/DELETE_users_id_friends_id.md#files) 
* [`/users/#{id}/socialMedia/{service}`](users/DELETE_users_id_socialMedia_service.md#files) 