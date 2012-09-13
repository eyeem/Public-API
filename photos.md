#Endpoint: Photos
***

These are the API calls that you can use to retrieve photos, comments and likes. Note that all requests require authorization, either by including the access_token in the header, or the client_id as a URL query parameter (see [[home]])

##Available endpoints
***

* `/photos`, [GET](#GETphotos), [POST](#POSTphotos)
* `/photos/upload`, [POST](#POSTphotosUpload)
* `/photos/#{id}`, [GET](#GETphotosId), [PUT](#PUTphotosId), [DELETE](#DELETEphotosId)
* `/photos/#{id}/likers`, [GET](#GETphotosIdLikers)
* `/photos/#{id}/likers/#{user_id}`, [GET](#GETphotosIdLikersId), [PUT](#PUTphotosIdLikersId), [DELETE](#DELETEphotosIdLikersId)
* `/photos/#{id}/comments`, [GET](#GETphotosIdComments), [POST](#POSTphotosIdComments)
* `/photos/#{id}/comments/#{comment_id}`, [GET](#GETphotosIdCommentsId), [DELETE](#DELETEphotosIdCommentsId)
* `/photos/#{id}/albums`, GET
* `/photos/#{id}/albums/#{album_id}`, [PUT](#PUTphotosIdAlbumsId), [DELETE](#DELETEphotosIdAlbumsId)
* `/photos/#{id}/topics`, [POST](#POSTphotosIdTopics)
* `/photos/#{id}/flag`, [POST](#POSTphotosIdFlag)
* `/photos/#{id}/share`, [POST](#POSTphotosIdShare)
* `/photos/#{photo_id}/discover`, [POST](#POSTphotosIdDiscover)
* `/photos/#{photo_id}/hide`, [POST](#POSTphotosIdHide)
* `/photos/bgImages`, [GET](#GETphotosBg)
* `/api/popular/random`, GET >> special, returns a random photo object from the 50 current most popular photos.

##Representation
***

The various possible representations of a photo (simple,detailed) are presented and described in the [model]() page.