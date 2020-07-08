---
description: >-
  The mtgbracket API will return error responses in a consistent format to help
  you better understand how to solve any problems you may encounter.
---

# Errors

The _mtgbracket_ API returns data in JSON.  Whenever an error occurs as part of a request, the error content will be returned as JSON as well.

Our errors will be presented in the following structure:

```javascript
{
    "error": {
        "status_code": 500,
        "message": "Error encountered during api request",
        "data": [],
        "debug": null
    }
}
```

In addition, they will include a relevant HTTP status code.  Some common examples of codes used by our service include:

| Code | Description |
| :--- | :--- |
| [200/201/204](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/200) | Successful request |
| [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400) | Bad Request.  There was an issue with the request input. |
| [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404) | Not Found.  There was an attempt to access a resource that does not exist. |
| [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500) | Server Error. There was a problem caused by the mtgbracket service. |

Each _mtgbracket_ error object includes an optional `data` property.  In some cases, this array will be populated with additional information in the form of key:value pairs that may provide additional context into the encountered error.

These values could represent things such as the offending field in an HTTP 400 response, or an internal status code that can be useful to us for helping you debug a recurring issue.

