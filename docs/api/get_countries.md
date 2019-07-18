title: GET /countries | Academiclabs
title_string: <span class="t-get">GET</span> Countries

# <span class="t-get">GET</span>  /countries

This endpoint allows you to retrieve a list of countries for a given keyword

```
https://api.academiclabs.co/v1/countries
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
curl --location --request GET "{{url}}/api/v1/countries?q=bel" \
  --header "Content-Type: application/json" \
  --header "Authorization: Bearer YOUR_API_KEY"
```

## Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>200

```json
[
    {
        "id": 30,
        "name": "Belize"
    },
    {
        "id": 19,
        "name": "Belgium"
    },
    {
        "id": 29,
        "name": "Belarus"
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