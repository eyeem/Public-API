#EyeEm API
***
 **[Introduction](#introduction) | [API Documentation](#api-documentation) | [Basics](#basics) | [OAuth](#oauth) | [Request Headers](#request-headers) | [Pagination](#pagination) | [Images and Image Resolution](#images-and-image-resolutions) | [Contact](#contact)**

##Introduction
***

The EyeEm Public API is read-only by default, and covers the complete EyeEm functionality. We do offer write access on a case-by-case basis. We use the API ourselves for our mobile apps, and are actively developing and improving it. The API is currently in version 2.2.0. We are working on v3 and expect to release that soon.

You can register an app by going to [Your apps on EyeEm](http://eyeem.com/developers).

##API Documentation
***

###Endpoints

* **[Users](https://github.com/eyeem/public-API/tree/master/endpoints/users.md#files)**
* **[Photos](https://github.com/eyeem/public-API/tree/master/endpoints/photos.md#files)**
* **[Albums](https://github.com/eyeem/public-API/tree/master/endpoints/albums.md#files)**
* **[Discover](https://github.com/eyeem/public-API/tree/master/endpoints/discover.md#files)**
* **[Missions](https://github.com/eyeem/public-API/tree/master/endpoints/missions.md#files)**
* **[Invitations](https://github.com/eyeem/public-API/tree/master/endpoints/invitations.md#files)**
* **[News](https://github.com/eyeem/public-API/tree/master/endpoints/news.md#files)**
* **[Topics](https://github.com/eyeem/public-API/tree/master/endpoints/topics.md#files)**
* **[Search](https://github.com/eyeem/public-API/tree/master/endpoints/search.md#files)**
* **[Venues](https://github.com/eyeem/public-API/tree/master/endpoints/venues.md#files)**
* **[Auth](https://github.com/eyeem/public-API/tree/master/endpoints/auth.md#files)**
* **[Apps](https://github.com/eyeem/public-API/tree/master/endpoints/apps.md#files)**

###Resources
* **[Model](https://github.com/eyeem/public-API/tree/master/resources/model.md#files)**
* **[Errors](https://github.com/eyeem/public-API/tree/master/resources/errors.md#files)**


##Basics
***

Our API is RESTful, which means that requests are defined using the HTTP verbs `GET`, `PUT`, `DELETE` and `POST`.

To play around with the api calls, hop over to APIGee: `https://apigee.com/eyeem/embed/console/eyeem?v=2`

All API calls are SSL encrypted, and the API responses are in JSON. The base API url is `https://api.eyeem.com/v2`

  * content encoding: you SHOULD be able to handle gzip and set the `Accept-Encoding: gzip` HTTP header
  * content types:
    * requests:  `application/x-www-form-urlencoded` or `application/json`
    * responses:  `application/json` or `image/*`
  * string encoding: you MUST use [utf-8](http://tools.ietf.org/html/rfc3629) everywhere
  * date and time encoding:
    * [ISO 8601](http://www.w3.org/TR/NOTE-datetime) as a string (for now)
  * error handling:
    * error codes: [HTTP status codes](http://en.wikipedia.org/wiki/List_of_HTTP_status_codes)
    * error payload: `{"message":"...some human readable error message..."}`
  * Here's the [order and type of error codes](errors) returned by the API.

If you have any issues or any suggestions, please do not hesitate to [get in touch](mailto:api@eyeem.com).

A basic request using curl can look like this:

`$ curl https://api.eyeem.com/v2/users/1013?access_token=ACCESS_TOKEN`

```json
{
  "user": {
    "id": "1013",
    "fullname": "ramz",
    "nickname": "ramz",
    "thumbUrl": "http://cdn.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg",
    "description": "EyeEm Ramz. EyeEm Happy! Srsly. Choo choo!!",
    "photoUrl": "http://cdn.eyeem.com/thumb/sq/200/0a4a321f1806b00c668d111a314bd98a14985765.jpg",
    "totalPhotos": 1040,
    "totalFollowers": 282,
    "totalFriends": 477,
    "totalLikedAlbums": 43
  }
}
```

#OAuth
***
To authenticated requests, we use OAuth2, and we try to comply to the [latest draft] (http://tools.ietf.org/html/draft-ietf-oauth-v2-23). Access Tokens do not expire, at the moment, however, that may also change, and we may start sending `refresh_token` and an `expires` parameter with the `access_token`.

For the time being, you may pass a `client_id` parameter, or an `X-Client-Id` header instead of an `access_token` to most public `GET`. That is subject to change.

After your registered app is approved, you can use your `client_id` and `client_secret` to generate access tokens. Here's the OAuth2 authentication process:

1) Authorization code:
First, point the browser to `http://www.eyeem.com/oauth/authorize?response_type=code&client_id=Chi6ae5sLes9beCinae5sohM&redirect_uri=http://example.com/callback`
The user is prompted to allow/deny access to your app. If they allow access, EyeEm will redirect to the provided url with an authorization code
`http://example.com/callback?code=Yeenie1H`
otherwize, the user is redirected with an error message
` http://example.com/callback?error=access_denied&error_description=The+user+denied+access+to+your+application`

2) Access token:
From your backend call
 `curl -X POST "http://api.eyeem.com/v2/oauth/token?grant_type=authorization_code&client_id=Chi6ae5sLes9beCinae5sohM&client_secret=IeBai4eeloRoiw3e&redirect_uri=http://example.com/callback&code=Yeenie1H"`

The answer will look like:
```json
 {
 "access_token":"2b9b0ef6065e60f3cc81646f3a7622af68295afb",
 "expires_in":315360000,
 "token_type":"bearer"
 }
```
For now, EyeEm API `access_tokens` do not expire, that may change in the future.

3) Making Authenticated Request:

 To make authenticated requests you provide your access token as credentials. You should send it as a header:
` Authorization: Bearer 2b9b0ef6065e60f3cc81646f3a7622af68295afb`
however, for the time being, it's also possible to send it as a  URL query param:
`$ curl https://api.eyeem.com/v2/users/12345?access_token=2b9b0ef6065e60f3cc81646f3a7622af68295afb`

That's all you need to authenticate with EyeEm.

##Request Headers
***

In addition to your access token, the EyeEm API accepts the following headers (not required)
- X-Client-Id: Your app's `client_id` can be provided instead of an `access_token`. This is valid for any public `GET` calls, but is subject to change, and therefore not recommended.
- X-Api-Version: the current API version is 2.2.0, the default is 2.0.0. As indicated on the specific endpoints, the parameters and responses vary between API versions. It is recommended to always use the latest API version
- X-hourOfDay: Integer between 0 and 24. For venue and location related requests.
- Accept-Language: Currently, the following languages are supported ('en','de','ru','ar','es','fr','ja','pt','id','zh','nl','pl','th','tr','uk','vi'). The default is 'en'.

##Pagination
***

Some endpoints in the api return arrays of photos, users, or albums. Those endpoints always contain four fields: `offset`,`limit`,`total` and `items`. `items` is an array of the requested object, whereas the remaining parameters can be used to paginate the list.

##Images and Image Resolutions
***

You can request EyeEm photos in various sizes and formats. The default API endpoints return a `thumbUrl` and (optionally) a `photoUrl`
Both urls have the format `http://cdn.eyeem.com/thumb/sq/50/0a4a321f1806b00c668d111a314bd98a14985765.jpg` and return different size photos that you can simply plug into your app.

In case you want to display photos in a different resolution you can use the same filename and change the two middle parts of the url like so:
- `http://cdn.eyeem.com/thumb/h/{pixels}/filename` will return the image scaled to have a max height of {pixels}
- `http://cdn.eyeem.com/thumb/{width}/{height}/filename` will return the image scaled to fit into {width} and {height}
- `http://cdn.eyeem.com/thumb/sq/{pixels}/filename` will return the image cropped into a square with length {pixels}


##Contact
***

For feedback, questions, complaints and props, you can get in touch with us at [api@eyeem.com](mailto:api@eyeem.com) or [@eyeemapi](http://twitter.com/eyeemapi) on Twitter.