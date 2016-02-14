---
title: Datalab API Reference

language_tabs:
  - JSON

toc_footers:
  - <a href='http://github.com/tripit/slate'>Documentation Powered by Slate</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Datalab API! 

# API Versions

Specify the version of the API in the request header.

`Accept : apllication/json.v1`

<aside class="notice">
  If not set the the current version of the API will be used.
</aside>

# Companies
##Get all Companies
> Responce 200

```json
[
  {   
      "id":1,
      "name":"company_name", 
      "full_address" :null,
      "zip_code":null,
      "phone_number":null,
      "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
      "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
    },
    {
      "id":2,
      "name":"company2",
      "full_address":null,
      "zip_code":null,
      "phone_number":null,
      "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
      "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
    }
]
```

This endpoint retrieves all companies.
### HTTP Request
`GET localhost:3000/api/companies/`



##Get one company

> Responce 200

```json
{   
    "id":1,
    "name":"company_name", 
    "full_address" :null,
    "zip_code":null,
    "phone_number":null,
    "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
  }
```
This endpoint retrieves one company.
### HTTP Request
`GET localhost:3000/api/companies/:id`
### URL Parameters
Parameter | Description
--------- | -----------
id | The ID of the company to retrieve

##Create a company

> Resquest JSON 

```json
  { "company": { "name": "company_name" } }
```
> Responce 201

```json
{   
    "id":1,
    "name":"company_name", 
    "full_address" :null,
    "zip_code":null,
    "phone_number":null,
    "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
  }
```
This endpoint creates one company.
### HTTP Request
`POST localhost:3000/api/companies/`

Attributes | Data type
---------- | -------
name | String ( required )
full_address | String
zip_code | String
phone_number | String



##Update one company
> Responce 200

```json
{   
    "id":1,
    "name":"new_company_name", 
    "full_address" :null,
    "zip_code":null,
    "phone_number":null,
    "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
  }
```
This endpoint updateds one company.
### HTTP Request
`PUT localhost:3000/api/companies/:id`
### URL Parameters
Parameter | Description
--------- | -----------
id | The ID of the company to update

##Delete one company
> Responce no_content

This endpoint deletes a company.
### HTTP Request
`DELETE localhost:3000/api/companies/:id`
### URL Parameters
Parameter | Description
--------- | -----------
id | The ID of the company to delete



# Projects
##Get all Projects
> Responce 200

```json
[
   {
    "id": 1,
    "name": "My project",
    "frame_rate": "24",
    "color_space": null,
    "aspect_ratio": "2.39",
    "resolution": null,
    "production": null,
    "supervisor": null,
    "sound_studio": null,
    "status": null,
    "company_id": 1,
    "created_at": "Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at": "Sun, 07 Feb 2016 22:40:59 +0100"
  },
  {
    "id": 1,
    "name": "project_name",
    "frame_rate": "24",
    "color_space": null,
    "aspect_ratio": "1.85",
    "resolution": null,
    "production": null,
    "supervisor": null,
    "sound_studio": null,
    "status": null,
    "company_id": 1,
    "created_at": "Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at": "Sun, 07 Feb 2016 22:40:59 +0100"
  },
]
```

This endpoint retrieves all projects.
### HTTP Request
`GET localhost:3000/api/projects/?company_id`
### URL Parameters
Parameter | Description
--------- | -----------
company_id | The ID of company the projects belongs to.


##Get one project

> Responce 200

```json
 {
    "id": 1,
    "name": "My project",
    "frame_rate": "24",
    "color_space": null,
    "aspect_ratio": "2.39",
    "resolution": null,
    "production": null,
    "supervisor": null,
    "sound_studio": null,
    "status": null,
    "company_id": 1,
    "created_at": "Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at": "Sun, 07 Feb 2016 22:40:59 +0100"
  }
```
This endpoint retrieves one project.
### HTTP Request
`GET localhost:3000/api/projects/:id`
### URL Parameters
Parameter | Description
--------- | -----------
id | The ID of the project to retrieve

##Create a project

> Resquest JSON 

```json
  { "project": { "name": "project_name", "company_id" : 2 } }
```
> Responce 201

```json
 {
    "id": 1,
    "name": "My project",
    "frame_rate": "24",
    "color_space": null,
    "aspect_ratio": "2.39",
    "resolution": null,
    "production": null,
    "supervisor": null,
    "sound_studio": null,
    "status": null,
    "company_id": 2,
    "created_at": "Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at": "Sun, 07 Feb 2016 22:40:59 +0100"
  }
```
This endpoint creates one project.
### HTTP Request
`POST localhost:3000/api/projects/`

Attributes | Data type
---------- | -------
name | String ( required )
company_id  | Integer ( required )
frame_rate  | String
color_space  | String
aspect_ratio  | String
resolution  | String
production  | String
supervisor  | String
sound_studio  | String
status  | String



##Update one project

> Responce 200

```json
{   
    "id":1,
    "name":"new_company_name",


    "created_at":"Sun, 07 Feb 2016 22:40:59 +0100",
    "updated_at":"Sun, 07 Feb 2016 22:40:59 +0100"
  }
```
This endpoint updateds one project.
### HTTP Request
`PUT localhost:3000/api/projects/:id`
### URL Parameters
Parameter | Description
--------- | -----------
id | The ID of the project to update

##Delete one project

> Responce no_content

This endpoint deletes a project.
### HTTP Request
`DELETE localhost:3000/api/projects/:id`
### URL Parameters
Parameter | Description
--------- | -----------
id | The ID of the project to delete




#Timecode
##to timecode
This endpoint converts a frames number to a timecode string.
> Resquest JSON 

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
> Resquest JSON 

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
> Resquest JSON 

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



