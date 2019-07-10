title: Requests | Academiclabs
title_string: Requests

# Requests

!!! info 
    All requests must be made over HTTPS. The API does not support HTTP.

## Environments

The host for Web API v1 requests is always `https://{{ env }}.academiclabs.co/v1/`. In our documentation we will refer to the variable `{{ env }}`. Once you start with implementing AcademicLabs you will receive first our Sandbox Mode API-Key. You only need to replace `{{ env }}` with the correct environment you want to connect with.

!!! warning 
    You will only receive your production API Key once AcademicLabs has confirmed that your integration is fully operational.

### Sandbox mode

```
https://staging-api.academiclabs.co/v1/

```

### Production
```
https://api.academiclabs.co/v1/

```

## HTTP Verbs
|  Verb   | Description |
| -------- |--------------|
| GET  |	Retrieve a resource or group of resources|
| POST  |Create a new resource|
| PUT  |Update an existing resource|
| DELETE  |Delete an existing resource|
| OPTIONS  |View allowed verbs against a specific resource|

