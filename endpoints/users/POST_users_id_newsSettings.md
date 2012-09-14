# POST /users/#{id}/newsSettings     
***
`/users/#{id}/newsSettings`

### Description
***
Only available for the authenticated user, this call edits a user's push and email notification settings.

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**id**|the user id to edit|integer|x||
|**parameter**| **description**| **type** |**required?** |**default**|
|**push_photo_like**|boolean|||
|**push_photo_comment**||boolean|||
|**push_user_follower**||boolean|||
|**push_user_joined**||boolean|||
|**push_album_contributor**| |boolean|||
|**push_photo_comment_mention**||boolean|||
|**email_photo_like**|boolean|||
|**email_photo_comment**||boolean|||
|**email_user_follower**||boolean|||
|**email_user_joined**||boolean|||
|**email_album_contributor**| |boolean|||
|**email_photo_comment_mention**||boolean|||



### Response
***


200 and confirmation message

[Errors](../../resources/errors.md#files)


### Examples
***

`https://www.eyeem.com/api/v2/users/me/newsSettings`


