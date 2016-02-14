#Deliveries
##Get all deliveries
This endpoint retrives all the deliveies for a given project ID.

> Responce 200

```json
  [ 
    {
      "id"                : 1,
      "project_id"        : 5,
      "media"             : "trailer",
      "reference"         : "trl_0001",
      "quote_reference"   : "0001",
      "resolution"        : "HD 1920x1080",
      "apperture"         : "2.39",
      "letter_box"        : true,
      "frame_rate"        : "24",
      "file_format"       : "mxf",
      "color_space"       : "rec709",
      "compression"       : "DnXHD175",
      "anamorphic"        : false,
      "subtitle_stream"   : "",
      "audio_mapping"     : "5.1",
      "audio_format"      : "16 bit",
      "client_approved"   : false,
      "status"            : "pending",
      "cost"              : "£ 500,00",
      "delivery_method"   : "FTP",
      "version"           : "International",
      "created_by"        : "User Name",
      "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
      "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
  }, {

  }
]
```
### HTTP Request
`GET localhost:3000/api/projects/:project_id/deliveries/`

### URL Parameters
Parameter | Description
--------- | -----------
project_id | The ID of the project that contains deliveries


##Get a delivery
This endpoint retrives one delivery for a given project ID.

> Responce 200

```json
{
    "id"                : 2,
    "project_id"        : 5,
    "media"             : "trailer",
    "reference"         : "trl_0001",
    "quote_reference"   : "0001",
    "resolution"        : "HD 1920x1080",
    "apperture"         : "2.39",
    "letter_box"        : true,
    "frame_rate"        : "24",
    "file_format"       : "mxf",
    "color_space"       : "rec709",
    "compression"       : "DnXHD175",
    "anamorphic"        : false,
    "subtitle_stream"   : "",
    "audio_mapping"     : "5.1",
    "audio_format"      : "16 bit",
    "client_approved"   : false,
    "status"            : "pending",
    "cost"              : "£ 500,00",
    "delivery_method"   : "FTP",
    "version"           : "International",
    "created_by"        : "The current signed in user name",
    "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
}
```
### HTTP Request
`GET localhost:3000/api/projects/:project_id/deliveries/:id`


### URL Parameters
Parameter | Description
--------- | -----------
project_id | The ID of the project that contains deliveries
id | The ID of the delivery to retrive


##Create a delivery

> Request

```json
  { 
    "delivery": 
      { 
        "project_id": 5, 
        "media": "trailer", 
        "resolution": "2048x1080", 
        "frame_rate": "24"
      }
  }
```
> Responce 201

```json
{
    "id"                : 3,
    "project_id"        : 5,
    "media"             : "trailer",
    "reference"         : "",
    "quote_reference"   : "",
    "resolution"        : "2048x1080",
    "apperture"         : "0",
    "letter_box"        : false,
    "frame_rate"        : "24",
    "file_format"       : "",
    "color_space"       : "",
    "compression"       : "",
    "anamorphic"        : false,
    "subtitle_stream"   : "",
    "audio_mapping"     : "",
    "audio_format"      : "",
    "client_approved"   : false,
    "status"            : "",
    "cost"              : "",
    "delivery_method"   : "",
    "version"           : "",
    "created_by"        : "The current signed in user name",
    "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
}
```
This endpoint creates one company.
### HTTP Request
`POST localhost:3000/api/deliveries/`

Attributes | Data type
---------- | -------
project_id | Integer ( required )
media  | String
reference  | String
quote_reference  | String
resolution | String
apperture  | String
letter_box | String
frame_rate | String
file_format  | String
color_space  | String
compression  | String
anamorphic | Boolean
subtitle_stream  | String
audio_mapping  | String
audio_format | String
client_approved  | Boolean
status | String
cost | String
delivery_method  | String
version  | String
created_by | String


