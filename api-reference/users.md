---
description: >-
  Modify and work with mtgbracket users' accounts to manage profile data,
  configuration, and other referential data related to an individual.
---

# Users

{% api-method method="get" host="https://api.mtgbracket.com" path="/users/:user\_id" %}
{% api-method-summary %}
Get User
{% endapi-method-summary %}

{% api-method-description %}
Returns the full account details of a single user by ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
User successfully retrieved.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "email": "brandin@mtgbracket.com",
    "first_name": "mtgbracket",
    "last_name": "mtgbracket",
    "birthday": 1554336000,
    "tier": {
        "id": 1,
        "name": "beta",
        "description": "A free tier allowing full, unrestricted access to all of the mtgbracket's features!",
        "rank": 1
    },
    "date_created": 1554404312,
    "date_updated": 1554404312,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```javascript
{
    "error": {
        "status_code": 404,
        "message": "User not found",
        "data": {
            "entity": "user"
        },
        "debug": null
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.mtgbracket.com" path="/users/:user\_id" %}
{% api-method-summary %}
Update User
{% endapi-method-summary %}

{% api-method-description %}
Update a user's profile data by ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="last\_name" type="string" required=false %}
User's new first name.
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
User's new last name.
{% endapi-method-parameter %}

{% api-method-parameter name="avatar\_url" type="string" required=false %}
URL pointing to a new profile avatar.
{% endapi-method-parameter %}

{% api-method-parameter name="status\_id" type="integer" required=false %}
User's new status ID.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```


```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/users/avatar?email=:email" %}
{% api-method-summary %}
Get User Avatar
{% endapi-method-summary %}

{% api-method-description %}
Retrieve a user's avatar URL from their email address.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
User's email address
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/users/activate?token=:activation\_token" %}
{% api-method-summary %}
Activate User
{% endapi-method-summary %}

{% api-method-description %}
Activates an account to confirm that the user has access to the email address they registered with.  Some _mtgbracket_ functionality is locked for unactivated accounts.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="activation\_token" type="string" required=true %}
Unique token to identify an account to activate.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/users/:user\_id/followers" %}
{% api-method-summary %}
Get Followers
{% endapi-method-summary %}

{% api-method-description %}
Get a list of users that are following a user.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/users/:user\_id/following" %}
{% api-method-summary %}
Get Following
{% endapi-method-summary %}

{% api-method-description %}
Get a list of users a user is following.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.mtgbracket.com" path="/users/:user\_id/follow/:following\_id" %}
{% api-method-summary %}
Follow User
{% endapi-method-summary %}

{% api-method-description %}
Adds a new user to a list of followed users.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="following\_id" type="integer" required=true %}
Unique ID of the user to be followed.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.mtgbracket.com" path="/users/:user\_id/follow/:following\_id" %}
{% api-method-summary %}
Unfollow User
{% endapi-method-summary %}

{% api-method-description %}
Remove a user from a list of followed users.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="following\_id" type="integer" required=true %}
Unique ID of the user to be unfollowed.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}
