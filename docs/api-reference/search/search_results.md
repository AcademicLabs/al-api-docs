# GET /v1/search_results
The search results API returns the number of results found for the given keyword parameter.

## Authentication
This is a public endpoint, hence no authentication is required.

## Request parameters
```
keyword string
```

## Example request
```curl
curl https://api.academiclabs.co/v1/search_results?keyword=aging
```

## Example status 200 response
```json
{
  "units": {
    "results": 10,
    "link": "https://app.academiclabs.co/search/units?keyword=aging"
  },
  "people": {
    "results": 3,
    "link": "https://app.academiclabs.co/search/people?keyword=aging"
  },
  "research_topics": {
    "results": 100,
    "link": "https://app.academiclabs.co/search/research_topics?keyword=aging"
  },
  "publications": {
    "results": 10000,
    "link": "https://app.academiclabs.co/search/publications?keyword=aging"
  },
  "projects": {
    "results": 999,
    "link": "https://app.academiclabs.co/search/projects?keyword=aging"
  }
}
```

## Example status 400 response
```json
{
   "error_msg": "failed to retrieve search results for keyword aging" 
}
```