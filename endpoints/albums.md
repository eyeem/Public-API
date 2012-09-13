#Endpoint: Albums
***

These are the API calls that you can use to retrieve albums, the photos in those albums, and further details



##Available endpoints
***

* `/albums`, [GET](albums/GET_albums.md), POST (not available yet)
* `/albums/recommended`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_recommended.md)
* `/albums/#{id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id.md)
* `/albums/#{id}/photos`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_photos.md)
* `/albums/#{id}/hide`, GET, POST, DELETE << will it stay HIDE or change to a different name?
* `/albums/#{id}/photos/#{photo_id}`, [PUT](https://github.com/eyeem/API/blob/master/endpoints/albums/PUT_albums_id_photos_id.md),[DELETE](https://github.com/eyeem/API/blob/master/endpoints/albums/DELETE_albums_id_photos_id.md) (see relevant endpoint in [photos](https://github.com/eyeem/API/blob/master/endpoints/photos.md))
* `/albums/#{id}/likers` [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_likers.md)
* `/albums/#{id}/likers/#{user_id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_likers_id.md), [PUT](https://github.com/eyeem/API/blob/master/endpoints/albums/PUT_albums_id_likers_id.md), [DELETE](https://github.com/eyeem/API/blob/master/endpoints/albums/DELETE_albums_id_likers_id.md)
* `/albums/#{id}/contributors`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_contributors.md)
* `/albums/#{id}/contributors/#{user_id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_contributors_id.md)
* `/albums/#{id}/share`, [POST](https://github.com/eyeem/API/blob/master/endpoints/albums/POST_albums_id_share.md)
* `/albums/#{id}/discover`, POST
* `/albums/#{id}/view`, POST

Special endpoints (will be deprecated soon)

* popular album: `/albums/dynamic:10`
* radius album: `/albums/radius:#{latitude}:#{longitude}`


##Representation
***

The various possible representations of an album (simple,detailed) are presented and described in the [model](https://github.com/eyeem/API/blob/master/resources/model.md) page.



##GET
***

* [`/albums`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums.md)
* [`/albums/recommended`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_recommended.md)
* [`/albums/#{id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id.md)
* [`/albums/#{id}/photos`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_photos.md)
* `/albums/#{id}/hide`
* [`/albums/#{id}/likers`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_likers.md)
* [`/albums/#{id}/likers/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_photos_id.md)
* [`/albums/#{id}/contributors`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_contributors.md)
* [`/albums/#{id}/contributors/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_contributors_id.md)


##PUT
***

* [`/albums/#{id}/photos/#{photo_id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/PUT_albums_id_photos_id.md)
* [`/albums/#{id}/likers/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/PUT_albums_id_photos_id.md)



##POST
***

* `/albums/#{id}/hide`
* [`/albums/#{id}/share`](https://github.com/eyeem/API/blob/master/endpoints/albums/POST_albums_id_share.md)
* `/albums/#{id}/discover`
* `/albums/#{id}/view`

##DELETE
***


* `/albums/#{id}/hide`
* [`/albums/#{id}/photos/#{photo_id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/DELETE_albums_id_photos_id.md)
* [`/albums/#{id}/likers/#{user_id}`](https://github.com/eyeem/API/blob/master/endpoints/albums/DELETE_albums_id_photos_id.md)
