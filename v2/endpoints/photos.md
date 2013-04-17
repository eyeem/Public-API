#Endpoint: Photos
***

These are the API calls that you can use to retrieve photos, comments and likes. Note that all requests require authorization, either by including the access_token in the header, or the client_id as a URL query parameter (see [home](../../README.md#files))

##Available endpoints
***

* `/photos`, [GET](photos/GET_photo.md#files), [POST](photos/POST_photo.md#files)
* `/photos/upload`, [POST](photos/POST_photo_upload.md#files)
* `/photos/#{id}`, [GET](photos/GET_photos_id.md#files), [PUT](photos/PUT_photos_id.md#files), [DELETE](photos/DELETE_photos_id.md#files)
* `/photos/#{id}/likers`, [GET](photos/GET_photos_id_likers.md#files)
* `/photos/#{id}/likers/#{user_id}`, [GET](photos/GET_photos_id_likers_id.md#files), [PUT](#PUTphotosIdLikersId), [DELETE](photos/PUT_photos_id_likers_id.md#files)
* `/photos/#{id}/comments`, [GET](photos/GET_photos_id_comments.md#files), [POST](photos/POST_photos_id_comments.md#files)
* `/photos/#{id}/comments/#{comment_id}`, [GET](photos/GET_photos_id_comments_id.md#files), [DELETE](photos/DELETE_photos_id_comments_id.md#files)
* `/photos/#{id}/albums`, GET
* `/photos/#{id}/albums/#{album_id}`, [PUT](photos/PUT_photos_id_albums_id.md#files), [DELETE](photos/DELETE_photos_id_albums_id.md#files)
* `/photos/#{id}/topics`, [POST](photos/POST_photos_id_topics.md#files)
* `/photos/#{id}/flag`, [POST](photos/POST_photos_id_flag.md#files)
* `/photos/#{id}/share`, [POST](photos/POST_photos_id_share.md#files)
* `/photos/#{id}/discover`, POST
* `/photos/#{id}/hide`, POST
* `/photos/bgImages`, [GET](photos/GET_photos_bgImages.md#files)
* `/api/popular/random`, GET >> special, returns a random photo object from the 50 current most popular photos.

##Representation
***

The various possible representations of a photo (simple,detailed) are presented and described in the [model](../resources/model.md#files) page.



##GET
***

* [`/photos`](photos/GET_photo.md#files)
* [`/photos/#{id}`](photos/GET_photos_id.md#files)
* [`/photos/#{id}/likers`](photos/GET_photos_id_likers.md#files)
* [`/photos/#{id}/likers/#{user_id}`](photos/GET_photos_id_likers_id.md#files)
* [`/photos/#{id}/comments`](photos/GET_photos_id_comments.md#files)
* [`/photos/#{id}/comments/#{comment_id}`](photos/GET_photos_id_comments_id.md#files)
* `/photos/#{id}/albums`
* [`/photos/bgImages`](photos/GET_photos_bgImages.md#files)
* `/api/popular/random`

##PUT
***
* [`/photos/#{id}`](photos/PUT_photos_id.md#files)
* [`/photos/#{id}/likers/#{user_id}`](photos/PUT_photos_id_likers_id.md#files)
* [`/photos/#{id}/albums/#{album_id}`](photos/PUT_photos_id_albums_id.md#files)

##POST
***

* [`/photos`](photos/POST_photo.md#files)
* [`/photos/upload`](photos/POST_photo_upload.md#files)
* [`/photos/#{id}/comments`](photos/POST_photos_id_comments.md#files)
* [`/photos/#{id}/topics`](photos/POST_photos_id_topics.md#files)
* [`/photos/#{id}/flag`](photos/POST_photos_id_flag.md#files)
* [`/photos/#{id}/share`](photos/POST_photos_id_share.md#files)
* `/photos/#{id}/discover`
* `/photos/#{id}/hide`


##DELETE
***

* [`/photos/#{id}`](photos/DELETE_photos_id.md#files)
* [`/photos/#{id}/likers/#{user_id}`](photos/DELETE_photos_id_likers_id.md#files)
* [`/photos/#{id}/comments/#{comment_id}`](photos/DELETE_photos_id_comments_id.md#files)
* [`/photos/#{id}/albums/#{album_id}`](photos/DELETE_photos_id_albums_id.md#files)