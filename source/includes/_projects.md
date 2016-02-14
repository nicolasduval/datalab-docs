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

> Request

```json
  { "project": { "name": "project_name", "company_id" : 2 } }
```
> Responce 201

```json
 {
    "id": 1,
    "name": "My project",
    "company_id": 2,
    "frame_rate": "24",
    "color_space": null,
    "aspect_ratio": "2.39",
    "resolution": null,
    "production": null,
    "supervisor": null,
    "sound_studio": null,
    "status": null,
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
sound_studios  | String
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
