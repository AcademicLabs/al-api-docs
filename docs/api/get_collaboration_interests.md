title: GET Collaboration Interests | Academiclabs
title_string: <span class="t-get">GET</span> Collaboration Interests

# <span class="t-get">GET</span>  /collaboration_interests

This endpoint allows you to retrieve a list of collaboration interests

```
https://{{ env }}.academiclabs.com/api/v1/collaboration_interests
```

---

## Headers

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| Authorization  | string | required | Your API_KEY received by AcademicLabs|


## Example

```curl
curl --location --request GET "https://sandbox.academiclabs.com/api/v1/collaboration_interests" \
  --header "Content-Type: application/json" \
  --header "Authorization: Bearer Your.API.Key-HERE"
```

## Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>200

```json
[
    {
        "id": 1,
        "name": "Academics"
    },
    {
        "id": 2,
        "name": "Corporate"
    },
    {
        "id": 3,
        "name": "SME"
    },
    {
        "id": 4,
        "name": "Government"
    },
    {
        "id": 5,
        "name": "Nonprofit"
    },
    {
        "id": 6,
        "name": "Education"
    }
]
```