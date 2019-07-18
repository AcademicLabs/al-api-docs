title: Responses | Academiclabs
title_string: Responses

# Responses

All responses are returned in JSON format. We specify this by sending the `Content-Type` header.

## Status Codes

Below is a table containing descriptions of the various status codes we currently support against various resources.

|  Status Code   | Description |
| -------- |--------------|
| 200  |No error|
| 201  |Successfully created|
| 204  |Successfully deleted|
| 400  |Bad request|
| 401  |Requires authentication|
| 422  |Unprocessable Entity|
| 429  |Too many requests/Rate limit exceeded|
| 500  |Internal server error|
