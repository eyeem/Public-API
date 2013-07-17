# POST /users/#{id}/flags     
***
`/users/#{id}/flags`

### Description
***
Only available for the authenticated user, this call edits a user's push and email notification settings, among others

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
|**email_weekly_newsletter**||boolean|||
|**push_album_invite**||boolean|||
|**email_album_invite**||boolean|||
|**facebook_photolike**||boolean|||
|**facebook_photodiscover**||boolean|||
|**facebook_albumfavorite**||boolean|||
|**facebook_userfollow**||boolean|||
|**facebook_timeline_popup**||boolean|||
|**facebook_albumcontribution**||boolean|||
|**email_newsletter**||boolean|||
|**web_onboarded**||boolean|||
|**web_banner_shown**||boolean|||
|**push_photo_tagged_person**||boolean|||
|**email_photo_tagged_person**||boolean|||


### Response
***


200 and confirmation message

[Errors](../../resources/errors.md#files)


### Examples
***

`https://api.eyeem.com/v2/users/me/flags`


