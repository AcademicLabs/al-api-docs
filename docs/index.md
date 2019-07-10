title: Authentication | Academiclabs
title_string: Authentication

# Getting an access token

You want to integrate AcademicLabs into your platform, awesome!

--- 

First step is getting your access token. To do that send an email to <a href="mailto:sales@academiclabs.co" target="_blank">sales@academiclabs.co</a>. We will contact you as soon as possible.

!!! info 
    It is also strongly advised creating an account on <a href="app.academiclabs.co" target="_blank">app.academiclabs.co</a> before contacting us.


## API Key
AcademicLabs’s Web API v1 supports the use of API Keys. API Keys allow you to use another method of authentication separate from your account username and password. API Keys add an additional layer of security for your account and can be assigned specific permissions to limit which areas of your account they may be used to access. You will be provided by AcademicLabs with an API-key. 


## Authorization Header
To use keys, you must set a plain text header named `Authorization` with the contents of the header being `Bearer XXX` where XXX is your API-key.

### Example

```
	GET https://api.academiclabs.co/v1/ HTTP/1.1
	Authorization: Bearer Your.API.Key-HERE
```

```curl
	curl -X "GET" "https://api.academiclabs.co/v1/" -H "Authorization: Bearer Your.API.Key-HERE" -H "Content-Type: application/json"
```


