#Endpoint: Photos
***

These are the API calls that you can use to retrieve photos, comments and likes. Note that all requests require authorization, either by including the access_token in the header, or the client_id as a URL query parameter (see [home](https://github.com/eyeem/API/blob/master/README.md))

##Available endpoints
***

* `/photos`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photo.md), [POST](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photo.md)
* `/photos/upload`, [POST](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photo_upload.md)
* `/photos/#{id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id.md), [PUT](https://github.com/eyeem/API/blob/master/endpoints/photos/PUT_photos_id.md), [DELETE](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id.md)
* `/photos/#{id}/likers`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_likers.md)
* `/photos/#{id}/likers/#{user_id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_likers_id.md), [PUT](#PUTphotosIdLikersId), [DELETE](https://github.com/eyeem/API/blob/master/endpoints/photos/PUT_photos_id_likers_id.md)
* `/photos/#{id}/comments`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_comments.md), [POST](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_comments.md)
* `/photos/#{id}/comments/#{comment_id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_comments_id.md), [DELETE](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id_comments_id.md)
* `/photos/#{id}/albums`, GET
* `/photos/#{id}/albums/#{album_id}`, [PUT](https://github.com/eyeem/API/blob/master/endpoints/photos/PUT_photos_id_albums_id.md), [DELETE](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id_albums_id.md)
* `/photos/#{id}/topics`, [POST](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_topics.md)
* `/photos/#{id}/flag`, [POST](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_flag.md)
* `/photos/#{id}/share`, [POST](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_share.md)
* `/photos/#{id}/discover`, POST
* `/photos/#{id}/hide`, POST
* `/photos/bgImages`, [GET](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_bgImages.md)
* `/api/popular/random`, GET >> special, returns a random photo object from the 50 current most popular photos.

##Representation
***

The various possible representations of a photo (simple,detailed) are presented and described in the [model](https://github.com/eyeem/API/blob/master/resources/model.md) page.



##GET
***

* [`/photos`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photo.md)
* [`/photos/#{id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id.md)
* [`/photos/#{id}/likers`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_likers.md)
* [`/photos/#{id}/likers/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_likers_id.md)
* [`/photos/#{id}/comments`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_comments.md)
* [`/photos/#{id}/comments/#{comment_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_id_comments_id.md)
* `/photos/#{id}/albums`
* [`/photos/bgImages`](https://github.com/eyeem/API/blob/master/endpoints/photos/GET_photos_bgImages.md)
* `/api/popular/random`

##PUT
***
* [`/photos/#{id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/PUT_photos_id.md)
* [`/photos/#{id}/likers/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/PUT_photos_id_likers_id.md)
* [`/photos/#{id}/albums/#{album_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/PUT_photos_id_albums_id.md)

##POST
***

* [`/photos`](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photo.md)
* [`/photos/upload`](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photo_upload.md)
* [`/photos/#{id}/comments`](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_comments.md)
* [`/photos/#{id}/topics`](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_topics.md)
* [`/photos/#{id}/flag`](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_flag.md)
* [`/photos/#{id}/share`](https://github.com/eyeem/API/blob/master/endpoints/photos/POST_photos_id_share.md)
* `/photos/#{id}/discover`
* `/photos/#{id}/hide`


##DELETE
***

* [`/photos/#{id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id.md)
* [`/photos/#{id}/likers/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id_likers_id.md)
* [`/photos/#{id}/comments/#{comment_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id_comments_id.md)
* [`/photos/#{id}/albums/#{album_id}`](https://github.com/eyeem/API/blob/master/endpoints/photos/DELETE_photos_id_albums_id.md)