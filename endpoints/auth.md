#Endpoint: Auth
***

These are the API calls available to native apps only. Note that all requests require authorization, either by including the access_token in the header, or the client_id and client_secret as a URL query parameter (see [home](https://github.com/eyeem/API/blob/master/README.md)).

Furthermore, only native apps can access this endpoint, and it's preferable to always include the following headers with every request:

* X-buildVersion: the current version of the EyeEm app
* X-clientDevice: iPhone 4, Samsung Galaxy S, Nokia Slide, whatever the device name is
* X-clientFirmware: the current OS version running on the device.

These are used for both our error-tracking as well as our internal metrics.

##Available endpoints
***
* `/auth/login`, [POST](#POSTlogin)
* `/auth/ping`, [POST](#POSTping)
* `/auth/error`, [POST](#POSTerror)
* `/auth/push`, [POST](#POSTpush), [DELETE](#DELETEpush)
* `/auth/facebookLogin`, [POST](#POSTfacebookLogin)
* `/auth/signUp`, [POST](#POSTsignUp)
* `/auth/logout`, [POST](#POSTlogout)
* `/auth/ok`, [GET](#GETok)
* `/auth/socialServiceKeys`, [GET](#GETsocialServiceKeys)


##Representation
***

There is no `auth` object, the various calls return either `user` objects or simple confirmations.


##API Calls
***


### POST /auth/login <a id="wiki-POSTlogin"></a>  

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

`http://www.eyeem.com/api/v2/auth/login`

***


### POST /auth/ping <a id="wiki-POSTping"></a> 
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

`http://www.eyeem.com/api/v2/auth/ping`

***

### POST /auth/error <a id="wiki-POSTerror"></a> 
posts an error message for the devs to look into. typically, this is called after some endpoint returns a 500 status, and the message supplied contains the entire request, so that the dev team can try to recreate and fix the error. 

#### Headers
 - default required headers here

#### Parameters
 - message (the error message the client wants to log)

#### Response

 - 200
 - error code

#### Examples

`http://www.eyeem.com/api/v2/auth/error`

***

### POST /auth/push <a id="wiki-POSTpush"></a> 

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

`http://www.eyeem.com/api/v2/auth/push`

***

### DELETE /auth/push <a id="wiki-DELETEpush"></a> 

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

`http://www.eyeem.com/api/v2/auth/push`
***

### POST /auth/facebookLogin <a id="wiki-POSTfacebookLogin"></a> 

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

`http://www.eyeem.com/api/v2/auth/facebookLogin`

***

### POST /auth/signUp <a id="wiki-POSTsignUp"></a> 
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

`http://www.eyeem.com/api/v2/auth/signUp`

***

### POST /auth/logout <a id="wiki-POSTlogout"></a> 

logs a user out and deletes their access_token

#### Headers
 - Authorization: Bearer [access_token]
 - default required headers for /auth

#### Parameters

#### Response

 - 200 if successfully logged out

#### Examples

`http://www.eyeem.com/api/v2/auth/logout`

--------------------------------------------------------------------------------

### GET /auth/ok <a id="wiki-GETok"></a> 

check that the user is still logged in with a valid account

#### Headers
- Authorization: Bearer [access_token]
- default required headers for /auth

#### Parameters

#### Response

 - 200 and a user object
 - 404 if the authentication is invalid

#### Examples

`http://www.eyeem.com/api/v2/auth/ok`

***

### GET /auth/socialServiceKeys <a id="wiki-GETsocialServiceKeys"></a> 

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

`http://apitest.eyeem.com/api/v2/auth/socialServiceKeys?service_name=foursquare`