title: GET /research_interests | Academiclabs
title_string: <span class="t-get">GET</span> Research Interests

# <span class="t-get">GET</span>  /research_interests

This endpoint allows you to retrieve a list of research interests for a given keyword

```
https://api.academiclabs.co/v1/research_interests
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
curl --location --request GET "{{url}}/api/v1/research_interests?q=bel" \
  --header "Content-Type: application/json" \
  --header "Authorization: Bearer YOUR_API_KEY"
```

## Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>200

```json
[
    {
        "id": 42456,
        "name": "Humans"
    },
    {
        "id": 42462,
        "name": "Humanism"
    },
    {
        "id": 42463,
        "name": "Humanities"
    },
    {
        "id": 53284,
        "name": "Human Body"
    },
    {
        "id": 42461,
        "name": "Human Rights"
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