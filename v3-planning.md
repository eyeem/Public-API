#EyeEm API V3
***

This is a living document to describe the general API changes, as well as list endpoints that need to be broken up, removed, updated, etc. Some points in here are suggestions or open questions.

For reference, check out the list of [API Endpoints being actively called from clients] (api-used-endpoints.md)

##General Remarks
***

- API Versioning. Introduced in V2.1.0 (Requests should now always contain the X-Api-Version header).
- URL/Path Changes:
  - main API path is now https://api.eyeem.com/v3. API will reject non-https requests
  - images are now found under http://cdn.eyeem.com
- API responses should include a "meta" object by default. That object contains the following:
  - a notice if the endpoint is deprecated
  - http response code (optional)
  - human-readable error message
  - notice for native clients (new app version, message from eyeem, etc)
  - rate-limit information

##Changes to Parameters (AKA params gone wild) 
***

Request parameters need to be standardized. V3 will introduce the following (optional) parameter:
- `sort`: for album photos, this could be something like `chronological`, or `top`. General rule is that this returns the same content, just ordered differently.
- `filter`: returns a subset of the resultset. The value is typically comma-separated, and the results are the union of all filters. For discover, `filter=trending,nearby,favorited` returns all discover items that match any/all of the three filters.
- `type`: for endpoints that span multiple result sets - an example would be `/albums`. `type` in that case could be `ids`, `tags`, `city`, `country`. **stupid?**
- `fields`: This parameter will replace all the stupid `detailed=1,includeAlbums=1,includeLikers=1` etc... it defines what additional object info should be returned. For example, on `GET` `/photos/{id}` `fields=user,albums,likers` would additionally include the photographer object, the album details and the photo's likers. **how can we add more details here? for example, the number of likers to return?**
- `subFields`: In some endpoints, we can specify the fields required for child objects. For example, in `/albums/{id}` we can request that photos be included with certain fields. At the moment, we pass fields like `includePhotoLikers`. That's stupid. **what should we replace this with?**

Additionally, default values need to be normalized across all endpoints. Any endpoint that returns people (photo likers, album contributors, friends) should for example return the same number of people by default, same applies to pagination limits, etc.

###Pagination parameters
***
Pagination needs a facelift. Offset/Limit doesn't scale, and it can't reliably return all new items. Already in v2.2.0, some endpoints work with `before` and `after`. We should consider switching to either that, or possibly some timestamp based pagination.

