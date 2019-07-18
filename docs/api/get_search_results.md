title: GET Search Results | Academiclabs
title_string: <span class="t-get">GET</span> Search Results

# <span class="t-get">GET</span>  /search_results

This endpoint allows you to retrieve counts and a link per category for a given keyword query.

```
https://public.academiclabs.co/api/v1/search_results?keyword=aging
```

---

## Headers

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| Authorization  | string | optional | Your API_KEY received by AcademicLabs|

!!! info 
    This is a public endpoint. Authorization key is not required.

## Query String

|  Value   |      Type      |  Required | Description |
| -------- |:--------------:|-----------|-----------|
| keyword  | string | required | A string based value for a given keyword|

---

## Example

```curl
curl --location --request GET "https://api-production.academiclabs.co/v1/search_results?keyword=aging" -H "Content-Type: application/json"
```

## Responses

<span class="response-type" >application/json</span>

### <span class="circle-green"></span>200

```json
{
  "keyword": "aging",
  "results": {
    "clinical_trials": {
      "results": 2926,
      "link": "https://app.academiclabs.co/search/clinical_trials?keyword=aging"
    },
    "funding_calls": {
      "results": 78,
      "link": "https://app.academiclabs.co/search/funding_calls?keyword=aging"
    },
    "organisations": {
      "results": 0,
      "link": "https://app.academiclabs.co/search/organisations?keyword=aging"
    },
    "projects": {
      "results": 4525,
      "link": "https://app.academiclabs.co/search/projects?keyword=aging"
    },
    "publications": {
      "results": 1636733,
      "link": "https://app.academiclabs.co/search/publications?keyword=aging"
    },
    "research_topics": {
      "results": 2770,
      "link": "https://app.academiclabs.co/search/research_topics?keyword=aging"
    },
    "researchers": {
      "results": 35471,
      "link": "https://app.academiclabs.co/search/researchers?keyword=aging"
    },
    "services": {
      "results": 0,
      "link": "https://app.academiclabs.co/search/services?keyword=aging"
    },
    "units": {
      "results": 3907,
      "link": "https://app.academiclabs.co/search/units?keyword=aging"
    }
  }
}
```

### <span class="circle-red"></span>400

```json
{
   "error_msg": "failed to retrieve search results for keyword aging" 
}
```