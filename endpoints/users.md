#Endpoint: Users
***

These are the API calls that you can use to retrieve users, their photos, friends and other data

**Note: #{id} can be replaced by "me" or by the user's vanity url ex: "ramz" - this applies to all user endpoints.**

##Available endpoints
***

* `/users`, [GET](users/GET_users.md#files), [POST](users/POST_users.md#files)
* `/users/#{id}`, [GET](users/GET_users_id.md#files), [PATCH](users/POST_users_id.md#files),[POST](users/POST_users_id.md#files),[PUT](users/POST_users_id.md#files), [DELETE](users/DELETE_users_id.md#files)
* `/users/#{id}/favoritedAlbums`, [GET](users/GET_users_id_favorited_albums.md#files), [POST](users/POST_users_id_favorited_albums.md#files)
* `/users/#{id}/feed`, [GET](users/GET_users_id_feed.md#files)
* `/users/#{id}/share`, [POST](users/POST_users_id_share.md#files)
* `/users/#{id}/followers`, [GET](users/GET_users_id_followers.md#files)
* `/users/#{id}/suggestions`, [GET](users/GET_users_id_suggestions.md#files)
* `/users/#{id}/blocked/#{id}`, [GET](users/GET_users_id_blocked_id.md#files),[PUT](users/PUT_users_id_blocked_id.md#files),[DELETE](users/DELETE_users_id_blocked_id.md#files)
* `/users/#{id}/friends/#{friend_id}`, [GET](users/GET_users_id_friends_id.md#files),  [PUT](users/PUT_users_id_friends_id.md#files),  [DELETE](users/DELETE_users_id_friends_id.md#files)
* `/users/#{id}/friends`, [GET](users/GET_users_id_friends.md#files), [POST](users/POST_users_id_friends.md#files)
* `/users/#{id}/followers/#{friend_id}`, [GET](users/GET_users_id_followers_id.md#files)
* `/users/#{id}/photos`, [GET](users/GET_users_id_photos.md#files)
* `/users/#{id}/likedPhotos`, [GET](users/GET_users_id_likedPhotos.md#files), [POST](users/POST_users_id_likedPhotos.md#files)
* `/users/#{id}/friendsPhotos`, [GET](users/GET_users_id_friendsPhotos.md#files)
* `/users/#{id}/socialMedia`, [GET](users/GET_users_id_socialMedia.md#files)
* `/users/#{id}/flags`, [GET](users/GET_users_id_flags.md#files), [POST](users/POST_users_id_flags.md#files), [PATCH](users/POST_users_id_flags.md#files), [PUT](users/POST_users_id_flags.md#files)
* `/users/#{id}/socialMedia/{service}`, [POST](users/POST_users_id_socialMedia_service.md#files),[PATCH](users/POST_users_id_socialMedia_service.md#files), [PUT](users/PUT_users_id_socialMedia_service.md#files), [DELETE](users/DELETE_users_id_socialMedia_service.md#files)
* `/users/#{id}/facebookPage`, [GET](users/GET_users_id_facebookPage.md#files), [POST](users/POST_users_id_facebookPage.md#files) 
* `/users/#{id}/topics`, [GET](users/GET_users_id_topics.md#files)
* `/users/#{id}/smContacts`, [GET](users/GET_users_id_sm_contacts.md#files)
* `/users/#{id}/emailContacts`, [GET](users/GET_users_id_email_contacts.md#files)
* `/users/#{id}/hide`, [POST](users/POST_users_id_hide.md#files)
