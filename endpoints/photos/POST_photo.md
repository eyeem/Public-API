# POST /photos
***
`/photos`

### Description
***
Create a photo object, either by uploading a file or passing a filename (the result of a POST on /photos/upload).

### Parameters
***

|header| description| type |required? |default|
|:---------|:--------------|:----------:|:------------:|:------------:|
|**photo**||file|if no filename is sent with the request||
|**filename**||string|if no photo is sent with the request||
|**parameter**| **description**| **type** |**required?** |**default**|
|**caption**| created, client-side, from "topic" at "venue" or "topic" in "city"|string|||
|**topic**|  the user's chosen topic(s), comma-separated|string|||
|**city**|the city name where the photo was taken|string|||
|**country**|the country name where the photo was taken|string|||
|**filter**| the eyeem filter that the user chose to use|string|||
|**venueId**|the foursquare venue ID that the user selected|integer| ||
|**venueServiceName**|"foursquare""|string|if venueId provided||
|**albumIds**| the IDs of albums we want to automatically add the photo to, comma-separated|string|||
|**noLocation**|tells the server not to save the photo's geodata|boolean| |0|

### Response
***

201 and a photo object

[Errors](https://github.com/eyeem/API/blob/master/resources/errors.md)

### Examples
***

`https://www.eyeem.com/api/v2/photos`



