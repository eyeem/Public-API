#Endpoint: Albums
***

These are the API calls that you can use to retrieve albums, the photos in those albums, and further details



##Available endpoints
***

* `/albums`, [GET](#GETalbums), POST (not available yet)
* `/albums/recommended`, [GET](#GETalbumsRecommended)
* `/albums/#{id}`, [GET](#GETalbumsId)
* `/albums/#{id}/photos`, [GET](#GETalbumsIdPhotos)
* `/albums/#{id}/hide`, GET, POST, DELETE << will it stay HIDE or change to a different name?
* `/albums/#{id}/photos/#{photo_id}`, [PUT](#PUTalbumsIdPhotosId),[DELETE](#DELETEalbumsIdPhotosId) (see relevant endpoint in [[photos| Endpoint: photos]])
* `/albums/#{id}/likers` [GET](#GETalbumsIdLikers)
* `/albums/#{id}/likers/#{user_id}`, [GET](#GETalbumsIdLikersId), [PUT](#PUTalbumsIdLikersId), [DELETE](#DELETEalbumsIdLikersId)
* `/albums/#{id}/contributors`, [GET](#GETalbumsIdContributors)
* `/albums/#{id}/contributors/#{user_id}`, [GET](#GETalbumsIdContributorsId)
* `/albums/#{album_id}/share`, [POST](#POSTalbumsIdShare)
* `/albums/#{album_id}/discover`, POST
* `/albums/#{album_id}/view`, POST

Special endpoints (will be deprecated soon)

* popular album: `/albums/dynamic:10`
* radius album: `/albums/radius:#{latitude}:#{longitude}`


##Representation
***

The various possible representations of an album (simple,detailed) are presented and described in the [model]() page.