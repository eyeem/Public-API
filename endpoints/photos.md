#Endpoint: Photos
***

These are the API calls that you can use to retrieve photos, comments and likes.

##Available endpoints
***

* `/photos`, [GET](photos/GET_photos.md#files), [POST](photos/POST_photos.md#files)
* `/photos/popular`, [GET](photos/GET_photos_popular.md#files)
* `/photos/upload`, [POST](photos/POST_photos_upload.md#files), [DELETE](photos/DELETE_photos_upload.md#files)
* `/photos/#{id}`, [GET](photos/GET_photos_id.md#files), [POST](photos/POST_photos_id.md#files), [PATCH](photos/PATCH_photos_id.md#files), [PUT](photos/PUT_photos_id.md#files), [DELETE](photos/DELETE_photos_id.md#files)
* `/photos/#{id}/people`, [GET](photos/GET_photos_id_people.md#files),[PUT](photos/PUT_photos_id_people.md#files),[DELETE](photos/DELETE_photos_id_people.md#files)
* `/photos/#{id}/likers`, [GET](photos/GET_photos_id_likers.md#files)
* `/photos/#{id}/likers/#{user_id}`, [GET](photos/GET_photos_id_likers_id.md#files), [PUT](#PUTphotosIdLikersId), [DELETE](photos/PUT_photos_id_likers_id.md#files)
* `/photos/#{id}/comments`, [GET](photos/GET_photos_id_comments.md#files), [POST](photos/POST_photos_id_comments.md#files)
* `/photos/#{id}/comments/#{comment_id}`, [GET](photos/GET_photos_id_comments_id.md#files), [PATCH](photos/PATCH_photos_id_comments_id.md#files), [POST](photos/PATCH_photos_id_comments_id.md#files), [PUT](photos/PATCH_photos_id_comments_id.md#files), [DELETE](photos/DELETE_photos_id_comments_id.md#files)
* `/photos/#{id}/share`, [POST](photos/POST_photos_id_share.md#files)
* `/photos/#{id}/albums`, [GET](photos/GET_photos_id_albums.md#files)
* `/photos/#{id}/flag`, [POST](photos/POST_photos_id_flag.md#files)
* `/photos/#{id}/mnemonic`, [POST](photos/POST_photos_id_mnemonic.md#files)