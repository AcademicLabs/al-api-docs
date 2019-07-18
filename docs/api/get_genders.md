title: GET /genders | Academiclabs
title_string: <span class="t-get">GET</span> Genders

# <span class="t-get">GET</span>  /genders

This endpoint allows you to retrieve a list of genders

```
https://api.academiclabs.co/v1/genders
```

---

## Headers

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| Authorization  | string | required | Your API_KEY received by AcademicLabs|


## Example

```curl
curl --location --request GET "{{url}}/api/v1/genders" \
  --header "Content-Type: application/json" \
  --header "Authorization: Bearer YOUR_API_KEY"
```

## Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>200

```json
[
    {
        "id": 1,
        "name": "Male"
    },
    {
        "id": 2,
        "name": "Female"
    },
    {
        "id": 3,
        "name": "Trans*"
    },
    {
        "id": 4,
        "name": "Prefer not to answer"
    }
]
```