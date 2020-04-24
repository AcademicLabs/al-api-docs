title: POST Create Researcher | Academiclabs
title_string: <span class="t-post">POST</span> Create Researcher

# <span class="t-post">POST</span>  /researchers

This endpoint allows you to create a researcher.  
If your API key is linked to a community on the platform, the researcher will be added automatically to that community.

```
https://{{ env }}.academiclabs.com/api/v1/researchers
```

---

## Headers

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| Authorization  | string | required | Your API_KEY received by AcademicLabs|


## Request body

<span class="response-type" >application/json</span>

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| first_name  | string | required | First name|
| last_name  | string | required | Last name|
| email  | string | required | Email|
| about  | string | optional | Biography|
| gender_id  | integer | optional | Gender|
| country_id  | integer | optional | Country|
| function_title_id  | integer | optional | Function title|
| collaboration_interest_ids  | array | optional | List of collaboration interests|
| research_interest_ids  | array | optional | List of research interests|


---

## Example

```curl
curl --location --request POST "https://sandbox.academiclabs.com/api/v1/researchers" \
  --header "Content-Type: application/json" \
  --header "Authorization: Bearer Your.API.Key-HERE" \
  --data "{
	\"researcher\": {
		\"first_name\": \"Frodo\",
		\"last_name\": \"Baggins\",
		\"about\": \"I will take the Ring, he said, though I do not know the way.\",
		\"email\": \"frodo@theshire.com\",
		\"gender_id\": 1,
		\"country_id\": 173,
		\"function_title_id\": 421,
		\"collaboration_interest_ids\": [5],
		\"research_interest_ids\": [37749,49544]
	}
}"
```

## Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>201

```json

```

### <span class="circle-red"></span>400

```json
{
   "errors": [
        "Email is invalid"
    ]
}
```

### <span class="circle-red"></span>422

```json
{
    "errors": [
        "Invalid ID found in function_title_id",
        "Invalid ID found in research_interest_ids"
    ]
}
```