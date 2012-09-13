#Endpoint: Users
***

These are the API calls that you can use to retrieve users, their photos, friends and other data

**Note: #{id} can be replaced by "me" or by the user's vanity url ex: "ramz" - this applies to all user endpoints.**

##Available endpoints
***

* `/users`, [GET](#GETusers), POST (not available here)
* `/users/#{id}`, [GET](#GETusersId), [PUT](#PUTusersId), DELETE (not available yet)
* `/users/#{id}/photos`, [GET](#GETusersIdPhotos)
* `/users/#{id}/likedPhotos`, [GET](#GETusersIdLikedPhotos), PUT/POST/DELETE (via [[photos|Endpoint: photos]] endpoint)
* `/users/#{id}/friendsPhotos`, [GET](#GETusersIdfriendsPhotos)
* `/users/#{id}/likedAlbums`, [GET](#GETusersIdLikedAlbums)
* `/users/#{id}/feed`, [GET](#GETusersIdFeed)
* `/users/#{id}/discover`, GET
* `/users/#{id}/friends`, [GET](#GETusersIdFriends), [POST](#POSTusersIdFriends)
* `/users/#{id}/friends/#{friend_id}`, [GET](#GETusersIdFriendsId), [PUT](#PUTusersIdFriendsId), [DELETE](#DELETEusersIdFriendsId)
* `/users/#{id}/followers`, [GET](#GETusersIdFollowers)
* `/users/#{id}/followers/#{friend_id}`, [GET](#GETusersIdFollowersId)
* `/users/#{id}/topics`, [GET](#GETusersIdTopics)
* `/users/#{id}/socialMedia`, [GET](#GETusersIdSocialMedia)
* `/users/#{id}/socialMedia/{service}`, [POST](#POSTusersIdSocialMediaService),[PUT](#PUTusersIdSocialMediaService), [DELETE](#DELETEusersIdSocialMediaService)
* `/users/#{id}/newsSettings`, [GET](#GETusersIdNewsSettings),[POST](#POSTusersIdNewsSettings)
* `/users/#{id}/smContacts`, [GET](#GETusersIdsmContacts)
* `/users/#{id}/emailContacts`, [GET](#GETusersIdEmailContacts), [POST](#POSTusersIdEmailContacts)
* `/users/#{id}/share`, [POST](#POSTusersIdShare)
* `/users/#{id}/hide`, POST

##Representation
***

The various possible representations of a user (simple,detailed) are presented and described in the [[model]] page.