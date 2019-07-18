title: GET /function_titles | Academiclabs
title_string: <span class="t-get">GET</span> Function Titles

# <span class="t-get">GET</span>  /function_titles

This endpoint allows you to retrieve a list of function titles for a given keyword

```
https://api.academiclabs.co/v1/function_titles
```

---

## Headers

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| Authorization  | string | required | Your API_KEY received by AcademicLabs|


## Query String

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| q  | string | required | A string based value for a given keyword|
| limit  | integer | optional | Number of results that will be fetched (default: 20)|


## Example

```curl
curl --location --request GET "{{url}}/api/v1/function_titles?q=dev&limit=5" \
  --header "Content-Type: application/json" \
  --header "Authorization: Bearer YOUR_API_KEY"
```


### Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>200

```json
[
    {
        "id": 64,
        "name": "Developer"
    },
    {
        "id": 65,
        "name": "Development Technologist"
    },
    {
        "id": 276,
        "name": "Web Developer"
    },
    {
        "id": 245,
        "name": "Software Developer"
    },
    {
        "id": 18,
        "name": "Business Developer"
    }
]
```

### <span class="circle-red"></span>400

```json
{
    "errors": [
        "Parameter q not found"
    ]
}
```