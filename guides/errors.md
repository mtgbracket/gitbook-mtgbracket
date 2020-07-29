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
| [200/201/204](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/200) | Successful request. |
| [400](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/400) | Bad Request.  There was an issue with the request input. |
| [401](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/401) | Unauthorized.  This API requires authentication. |
| [403](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/403) | Forbidden. The authenticated user does not have permission to execute this API. |
| [404](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/404) | Not Found.  There was an attempt to access a resource that does not exist. |
| [500](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500) | Server Error. There was a problem caused by the mtgbracket service. |

Each _mtgbracket_ error object includes an optional `data` property.  In some cases, this array will be populated with additional information in the form of key:value pairs that may provide additional context into the encountered error.

These values could represent things such as the offending field in an HTTP 400 response, or an internal status code that can be useful to us for helping you debug a recurring issue.

For example, given a request:

{% tabs %}
{% tab title="HTTP" %}
```javascript
PUT /users/1 HTTP/1.1
Host: https://accounts.mtgbracket.com
Authorization: Bearer 80a9a2a83e26965424d383f588cea4144f6afaa9304f3d2cf1e0946122d6e65d7dfc0f9bc1f34230
Content-Type: application/json

{
	"status_id": "polkadot hippo"
}
```
{% endtab %}

{% tab title="cURL" %}
```bash
curl --location --request PUT 'https://accounts.mtgbracket.com/users/1' \
--header 'Authorization: Bearer 80a9a2a83e26965424d383f588cea4144f6afaa9304f3d2cf1e0946122d6e65d7dfc0f9bc1f34230' \
--header 'Content-Type: application/json' \
--data-raw '{
	"status_id": "polkadot hippo"
}'
```
{% endtab %}
{% endtabs %}

You would receive the following error:

```javascript
{
    "error": {
        "status_code": 400,
        "message": "Invalid field value for status_id; must be one of 1, 2",
        "data": {
            "field": "status_id"
        },
        "debug": null
    }
}
```

In this particular case, our `data` field helps inform us which API field key generated our error.

