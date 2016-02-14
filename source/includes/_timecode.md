#Timecode
##to timecode
This endpoint converts a frames number to a timecode string.
> Request

```json
  { "fps" : 25, "frames" : 84600 }
```
> Responce 200

```json
  {
    "fps": 25,
    "timecode": "00:56:24:00"
  }
```
### HTTP Request
`POST localhost:3000/api/timecode/to_timecode/`

Attributes | Data type
---------- | -------
fps | Fixnum ( required )
frames  | Fixnum ( required )


##to frames
This endpoint converts a timecode string to a frames.
> Request

```json
  { "fps" : 25, "timecode" : "01:00:00:01" }
```
> Responce 200

```json
  {
    "fps": 25,
    "frames": 90001
  }
```
### HTTP Request
`POST localhost:3000/api/timecode/to_frames/`

Attributes | Data type
---------- | -------
fps | Fixnum ( required )
timecode  | String ( required )


##add
This endpoint adds timecodes.
> Request

```json
  { 
    "fps": 25, 
    "timecodes" : 
      ["02:00:00:01", "02:00:00:00", "02:00:00:00"]
  }
```
> Responce 200

```json
{
  "fps": 25,
  "timecode": "06:00:00:01",
  "frames": 540001
}
```
### HTTP Request
`POST localhost:3000/api/timecode/add/`

Attributes | Data type
---------- | -------
fps | Fixnum ( required )
timecode  | Array ( required )



