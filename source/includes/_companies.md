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

> Request 

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






