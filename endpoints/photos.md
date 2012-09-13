#Endpoint: Photos
***

These are the API calls that you can use to retrieve photos, comments and likes. Note that all requests require authorization, either by including the access_token in the header, or the client_id as a URL query parameter (see [home](../../README.md))

##Available endpoints
***

* `/photos`, [GET](photos/GET_photo.md), [POST](photos/POST_photo.md)
* `/photos/upload`, [POST](photos/POST_photo_upload.md)
* `/photos/#{id}`, [GET](photos/GET_photos_id.md), [PUT](photos/PUT_photos_id.md), [DELETE](photos/DELETE_photos_id.md)
* `/photos/#{id}/likers`, [GET](photos/GET_photos_id_likers.md)
* `/photos/#{id}/likers/#{user_id}`, [GET](photos/GET_photos_id_likers_id.md), [PUT](#PUTphotosIdLikersId), [DELETE](photos/PUT_photos_id_likers_id.md)
* `/photos/#{id}/comments`, [GET](photos/GET_photos_id_comments.md), [POST](photos/POST_photos_id_comments.md)
* `/photos/#{id}/comments/#{comment_id}`, [GET](photos/GET_photos_id_comments_id.md), [DELETE](photos/DELETE_photos_id_comments_id.md)
* `/photos/#{id}/albums`, GET
* `/photos/#{id}/albums/#{album_id}`, [PUT](photos/PUT_photos_id_albums_id.md), [DELETE](photos/DELETE_photos_id_albums_id.md)
* `/photos/#{id}/topics`, [POST](photos/POST_photos_id_topics.md)
* `/photos/#{id}/flag`, [POST](photos/POST_photos_id_flag.md)
* `/photos/#{id}/share`, [POST](photos/POST_photos_id_share.md)
* `/photos/#{id}/discover`, POST
* `/photos/#{id}/hide`, POST
* `/photos/bgImages`, [GET](photos/GET_photos_bgImages.md)
* `/api/popular/random`, GET >> special, returns a random photo object from the 50 current most popular photos.

##Representation
***

The various possible representations of a photo (simple,detailed) are presented and described in the [model](../resources/model.md) page.



##GET
***

* [`/photos`](photos/GET_photo.md)
* [`/photos/#{id}`](photos/GET_photos_id.md)
* [`/photos/#{id}/likers`](photos/GET_photos_id_likers.md)
* [`/photos/#{id}/likers/#{user_id}`](photos/GET_photos_id_likers_id.md)
* [`/photos/#{id}/comments`](photos/GET_photos_id_comments.md)
* [`/photos/#{id}/comments/#{comment_id}`](photos/GET_photos_id_comments_id.md)
* `/photos/#{id}/albums`
* [`/photos/bgImages`](photos/GET_photos_bgImages.md)
* `/api/popular/random`

##PUT
***
* [`/photos/#{id}`](photos/PUT_photos_id.md)
* [`/photos/#{id}/likers/#{user_id}`](photos/PUT_photos_id_likers_id.md)
* [`/photos/#{id}/albums/#{album_id}`](photos/PUT_photos_id_albums_id.md)

##POST
***

* [`/photos`](photos/POST_photo.md)
* [`/photos/upload`](photos/POST_photo_upload.md)
* [`/photos/#{id}/comments`](photos/POST_photos_id_comments.md)
* [`/photos/#{id}/topics`](photos/POST_photos_id_topics.md)
* [`/photos/#{id}/flag`](photos/POST_photos_id_flag.md)
* [`/photos/#{id}/share`](photos/POST_photos_id_share.md)
* `/photos/#{id}/discover`
* `/photos/#{id}/hide`


##DELETE
***

* [`/photos/#{id}`](photos/DELETE_photos_id.md)
* [`/photos/#{id}/likers/#{user_id}`](photos/DELETE_photos_id_likers_id.md)
* [`/photos/#{id}/comments/#{comment_id}`](photos/DELETE_photos_id_comments_id.md)
* [`/photos/#{id}/albums/#{album_id}`](photos/DELETE_photos_id_albums_id.md)