# GET /photos/bgImages       
***
`/photos/bgImages`

### Description
***
Get a selection of images that is used in the existing apps as a start screen background.


### Response
***


200 and an array of bgImage png files. The images themselves can be retrieved using the standard /thumb url. 

[Errors](../../resources/errors.md#files)

### Examples
***

`https://www.eyeem.com/api/v2/photos/bgImages`

```javascript

{
  "bgImages": [
    "bgimage18.png",
    "bgimage19.png",
    "bgimage20.png",
    "bgimage13.png",
    "bgimage14.png",
    "bgimage15.png",
    "bgimage16.png",
    "bgimage17.png",
    "bgimage1.png",
    "bgimage2.png",
    "bgimage3.png",
    "bgimage4.png",
    "bgimage5.png",
    "bgimage6.png",
    "bgimage7.png",
    "bgimage8.png",
    "bgimage9.png",
    "bgimage10.png",
    "bgimage11.png",
    "bgimage12.png"
  ]
}

```