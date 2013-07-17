# POST /photos  >> X-Api-Version 2.2.0 <<
***
`/photos`

### Description
***
Create a photo object, either by uploading a file or passing a filename (the result of a POST on /photos/upload).

Requires authed user (write access needed)

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**photo**||file|if no filename is sent with the request||
|**filename**||string|if no photo is sent with the request||
|**parameter**| **description**| **type** |**required?** |**default**|
|**description**|  the user's chosen description, may contain encoded albums in the form \[a:{album_id}\]|string|||
|**city**|the city name where the photo was taken|string|||
|**cc**|the country code where the photo was taken|string|||
|**filter**| the eyeem filter that the user chose to use|string|||
|**frame**| the eyeem filter that the user chose to use|string|||
|**pimped**|whether the user used the pimp filter feature|boolean| |0|
|**cropped**|whether the user cropped the photo feature|boolean| |0|
|**instagram_id**|if imported from IG, the matching IG id.|string|||
|**venueId**|the foursquare/eyeem venue ID that the user selected|integer| ||
|**venueServiceName**|"foursquare|eyeem""|string|if venueId provided||
|**albumIds**| the IDs of albums we want to automatically add the photo to, comma-separated (city/country/venue)|csv int|||
|**noLocation**|tells the server not to save the photo's geodata|boolean| |0|
|**timestamp**|is set as created_at (for importing older photos, etc|timestamp| |0|
|**people**| the people to tag in a photo. format: "service":"serviceId" (ex: "eyeem":"1013")|csv people obj|||

### Response
***

201 and a photo object

[Errors](../../resources/errors.md#files)
