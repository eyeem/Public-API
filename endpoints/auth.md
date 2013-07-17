#Endpoint: Auth
***

These are the API calls available to native apps only. Note that all requests require authorization.

Furthermore, only native apps can access this endpoint, and it's preferable to always include the following headers with every request:


##Available endpoints
***
* `/auth/login`, [POST](#POSTlogin)
* `/auth/facebookLogin`, [POST](#POSTfacebookLogin)
* `/auth/logout`, [POST](#POSTlogout)
* `/auth/signUp`, [POST](#POSTsignUp)
* `/auth/checkNickname`, [GET](#GETcheckNickname)
* `/auth/checkEmail`, [GET](#GETcheckEmail)
* `/auth/confirmEmail`, [POST](#POSTconfirmEmail)
* `/auth/requestPassword`, [POST](#POSTrequestPassword)
* `/auth/resetPassword`, [GET](#GETresetPassword) [POST](#POSTresetPassword)
* `/auth/deleteUser`, [POST] (#POSTdeleteUser)[DELETE] (#POSTdeleteUser)
* `/auth/ping`, [POST](#POSTping)
* `/auth/push`, [POST](#POSTpush), [DELETE](#DELETEpush)
* `/auth/socialServiceKeys`, [GET](#GETsocialServiceKeys)


##API Calls
***


### POST /auth/login <a id="POSTlogin"></a>  

Logs a user in with email/password

DESCRIPTION
#### Headers
 - default required headers (X-buildVersion, X-clientDevice, X-clientFirmware)

#### Parameters
 - email (was also named 'username' before)
 - password
 - grant_type=password
 - client_id=hash
 - client_secret=hash

#### Response

 - 200 and an access_token, token_type and user object
 - error with code and message

#### Examples

`https://api.eyeem.com/v2/auth/login`

***


### POST /auth/ping <a id="POSTping"></a> 
Pings the server whenever the EyeEm app is started for the very first time on a device (used to track downloads)

#### Headers
 - default required headers here

#### Parameters
 - device (iPhone/Android/Winphone)
 - uuid (unique device identifier)
 - client_id
 - client_secret

#### Response

 - 200
 - error code

#### Examples

`https://api.eyeem.com/v2/auth/ping`

***

### POST /auth/push <a id="POSTpush"></a> 

description: registers a device for push notification

#### Headers
 - Authorization: Bearer [access_token]
 - Default required headers for auth endpoint.

#### Parameters
 - device (iPhone/Android/Winphone)
 - uuid (unique device identifier)
 - device_token (for iphone/android - equivalent for winphone)
 - environment (production or sandbox): optional parameter, in case the respective push service differentiates between the two 

#### Response
 - 200 if success
 - error codes if failed

#### Examples

`https://api.eyeem.com/v2/auth/push`

***

### DELETE /auth/push <a id="DELETEpush"></a> 

unregisters a device from push notification

#### Headers
 - Authorization: Bearer [access_token]
 - Default required headers for auth endpoint.

#### Parameters
 - device (iPhone/Android/Winphone)
 - uuid (unique device identifier)
 - device_token (for iphone/android - equivalent for winphone)

#### Response

 - 200 if success
 - error codes if failed

#### Examples

`https://api.eyeem.com/v2/auth/push`
***

### POST /auth/facebookLogin <a id="POSTfacebookLogin"></a> 

allow a user to signup OR login with their facebook credentials. This is called after the user connects with facebook and facebook returns the access_token and facebookId.

**TODO**: list the facebook permissions needed for facebook connect.

#### Headers
- default required headers (X-buildVersion, X-clientDevice, X-clientFirmware)

#### Parameters
 - fbUserId (the user's facebook Id - was also named 'username' before)
 - fbAccessToken (access_token retrieved from facebook - was also named 'password' before)
 - fbAccessTokenExpires (expires retrieved from facebook)
 - client_id=hash (native client id)
 - client_secret=hash (native client secret)

#### Response

 - 200 and an access_token, token_type and user object (including new=true/false to identify new accounts)
 - error code with human readable error message otherwise

#### Examples

`https://api.eyeem.com/v2/auth/facebookLogin`

***

### POST /auth/signUp <a id="POSTsignUp"></a> 
create a new account

#### Headers
- default required headers (X-buildVersion, X-clientDevice, X-clientFirmware)

#### Parameters
 - username (valid email address)
 - password (min. 6 characters)
 - grant_type=password
 - client_id=hash (native client id)
 - client_secret=hash (native client secret)
 - fullname (optional)
 - nickname (optional)
 - photo (optional profile photo)

#### Response

 - 200 and an access_token, token_type, and user object
 - error code with human readable error message otherwise

#### Examples

`https://api.eyeem.com/v2/auth/signUp`

***

### POST /auth/logout <a id="POSTlogout"></a> 

logs a user out and deletes their access_token

#### Headers
 - Authorization: Bearer [access_token]
 - default required headers for /auth

#### Parameters

#### Response

 - 200 if successfully logged out

#### Examples

`https://api.eyeem.com/v2/auth/logout`


***

### GET /auth/socialServiceKeys <a id="GETsocialServiceKeys"></a> 

get the keys for one of the supported social services

#### Headers
- default required headers for /auth (client_id)

#### Parameters
- service_name: flickr,facebook,twitter,tumblr or foursquare

#### Response

 - 200 and a json object named after the requested service, containing the appId and appSecret
 - 404 if the authentication is invalid
 - 404 if the service is not supported

#### Examples

`https://api.eyeem.com/v2/auth/socialServiceKeys?service_name=foursquare`

***

### GET /auth/checkNickname <a id="GETcheckNickname"></a> 

Checks if a nickname is available

#### Headers

#### Parameters
 - nickname = string

#### Response
 - 200 if available
 - error codes if failed

#### Examples

***

### GET /auth/checkEmail <a id="GETcheckEmail"></a> 

Checks if an email is valid & available

#### Headers

#### Parameters
 - email = string

#### Response
 - 200 if available
 - error codes if failed

#### Examples

***

### POST /auth/confirmEmail <a id="POSTconfirmEmail"></a> 

Confirms an email as valid.

#### Headers

#### Parameters
 - token = string (validation token sent in activation email)

#### Response
 - 200 if ok
 - error codes if failed

#### Examples

***

### POST /auth/requestPassword <a id="POSTrequestPassword"></a> 

Requests a password reset.

#### Headers

#### Parameters
 - email = string

#### Response
 - 200 if ok
 - error codes if failed

#### Examples

***


### POST /auth/resetPassword <a id="POSTresetPassword"></a> 

Resets a password using the provided token.

#### Headers

#### Parameters
 - token = string (reset token sent to user)

#### Response
 - 200 if ok
 - error codes if failed

#### Examples

***


### GET /auth/resetPassword <a id="GETresetPassword"></a> 

**NO IDEA WHAT THIS DOES**

#### Headers

#### Parameters
 - token = string

#### Response
 - 200 if ok
 - error codes if failed

#### Examples

***

### DELETE | POST /auth/deleteUser <a id="POSTdeleteUser"></a> 

completely and permanently deletes a user! Requires either the user's access token, or an admin.

#### Headers
 - Authorization: Bearer [access_token]

#### Parameters

#### Response

#### Examples

***