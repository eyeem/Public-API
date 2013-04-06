 #Endpoint: Albums
***

These are the API calls that you can use to retrieve albums, the photos in those albums, and further details



##Available endpoints
***

* `/albums`, [GET](albums/GET_albums.md#files), POST (not available yet)
* `/albums/recommended`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_recommended.md#files)
* `/albums/#{id}`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id.md#files)
* `/albums/#{id}/photos`, [GET](https://github.com/eyeem/API/blob/master/endpoints/albums/GET_albums_id_photos.md#files)
* `/albums/recommended`, [GET](albums/GET_albums_recommended.md#files)
* `/albums/#{id}`, [GET](albums/GET_albums_id.md#files)
* `/albums/#{id}/photos`, [GET](albums/GET_albums_id_photos.md#files)
* `/albums/#{id}/hide`, GET, POST, DELETE << will it stay HIDE or change to a different name?
* `/albums/#{id}/photos/#{photo_id}`, [PUT](albums/PUT_albums_id_photos_id.md#files),[DELETE](albums/DELETE_albums_id_photos_id.md#files) (see relevant endpoint in [photos](https://github.com/eyeem/API/blob/master/endpoints/photos.md#files))
* `/albums/#{id}/likers` [GET](albums/GET_albums_id_likers.md#files)
* `/albums/#{id}/likers/#{user_id}`, [GET](albums/GET_albums_id_likers_id.md#files), [PUT](albums/PUT_albums_id_likers_id.md#files), [DELETE](albums/DELETE_albums_id_likers_id.md#files)
* `/albums/#{id}/contributors`, [GET](albums/GET_albums_id_contributors.md#files)
* `/albums/#{id}/contributors/#{user_id}`, [GET](albums/GET_albums_id_contributors_id.md#files)
* `/albums/#{id}/share`, [POST](albums/POST_albums_id_share.md#files)
* `/albums/#{id}/discover`, POST
* `/albums/#{id}/view`, POST

Special endpoints (will be deprecated soon)

* popular album: `/albums/dynamic:10`
* radius album: `/albums/radius:#{latitude}:#{longitude}`


##Representation
***

The various possible representations of an album (simple,detailed) are presented and described in the [model](../resources/model.md#files) page.



##GET
***

* [`/albums`](albums/GET_albums.md#files)
* [`/albums/recommended`](albums/GET_albums_recommended.md#files)
* [`/albums/#{id}`](albums/GET_albums_id.md#files)
* [`/albums/#{id}/photos`](albums/GET_albums_id_photos.md#files)
* `/albums/#{id}/hide`
* [`/albums/#{id}/likers`](albums/GET_albums_id_likers.md#files)
* [`/albums/#{id}/likers/#{user_id}`](albums/GET_albums_id_likers_id.md#files)
* [`/albums/#{id}/contributors`](albums/GET_albums_id_contributors.md#files)
* [`/albums/#{id}/contributors/#{user_id}`](albums/GET_albums_id_contributors_id.md#files)
* [`/albums/#{id}/relatedAlbums`](albums/GET_albums_id_related_albums.md#files)
* [`/albums/#{id}/venueCategories`](albums/GET_albums_id_venue_categories.md#files)


##PUT
***

* [`/albums/#{id}/photos/#{photo_id}`](albums/PUT_albums_id_photos_id.md#files)
* [`/albums/#{id}/likers/#{user_id}`](albums/PUT_albums_id_photos_id.md#files)



##POST
***

* `/albums/#{id}/hide`
* [`/albums/#{id}/share`](albums/POST_albums_id_share.md#files)
* `/albums/#{id}/discover`
* `/albums/#{id}/view`

##DELETE
***


* `/albums/#{id}/hide`
* [`/albums/#{id}/photos/#{photo_id}`](albums/DELETE_albums_id_photos_id.md#files)
* [`/albums/#{id}/likers/#{user_id}`](albums/DELETE_albums_id_photos_id.md#files)
