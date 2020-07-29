---
description: >-
  Events are managed and run by organizations.  Organizations are controlled by
  users, and maintain a separate profile for encapsulating necessary data.
---

# Organizations

{% api-method method="get" host="https://api.mtgbracket.com" path="/organizations/:organization\_id" %}
{% api-method-summary %}
Get Organization
{% endapi-method-summary %}

{% api-method-description %}
Returns the full details of an organization by ID.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
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
Successfully retrieved organization details.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 12,
    "name": "MisfitPixel",
    "date_created": 1585958400,
    "date_updated": 1585958400,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.mtgbracket.com" path="/organizations" %}
{% api-method-summary %}
Create Organization
{% endapi-method-summary %}

{% api-method-description %}
Create a new organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Organization's name.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully created a new organization.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 13,
    "name": "Acme Corp",
    "date_created": 1595965633,
    "date_updated": 1595965633,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.mtgbracket.com" path="/organizations/:organization\_id" %}
{% api-method-summary %}
Update Organization
{% endapi-method-summary %}

{% api-method-description %}
Update an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
Organization's name.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully updated an organization.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 13,
    "name": "Acme Corp 2",
    "date_created": 1595965633,
    "date_updated": 1595965675,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.mtgbracket.com" path="/organizations/:organization\_id" %}
{% api-method-summary %}
Delete Organization
{% endapi-method-summary %}

{% api-method-description %}
Delete an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
Successfully deleted an organization.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/users" %}
{% api-method-summary %}
Get Linked Users
{% endapi-method-summary %}

{% api-method-description %}
Return a list of users linked to this organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
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
Successfully retrieved a list of users linked to an organization.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 2,
            "user": {
                "id": 1,
                "email": "brandin@mtgbracket.com",
                "first_name": "brandin",
                "last_name": "mtgbracket",
                "birthday": 1554336000,
                "tier": {
                    "id": 1,
                    "name": "beta",
                    "description": "A free tier allowing full, unrestricted access to all of the mtgbracket's features!",
                    "rank": 1
                },
                "date_created": 1554404312,
                "date_updated": 1595961246,
                "status": {
                    "id": 1,
                    "name": "active"
                }
            },
            "role": {
                "id": 4,
                "name": "owner"
            },
            "date_created": 1595965634,
            "date_updated": 1595965634,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 4,
            "user": {
                "id": 2,
                "email": "john@mtgbracket.com",
                "first_name": "john",
                "last_name": "smith",
                "birthday": 1575158400,
                "tier": {
                    "id": 1,
                    "name": "beta",
                    "description": "A free tier allowing full, unrestricted access to all of the mtgbracket's features!",
                    "rank": 1
                },
                "date_created": 1595203200,
                "date_updated": 1595203200,
                "status": {
                    "id": 2,
                    "name": "inactive"
                }
            },
            "role": {
                "id": 1,
                "name": "user"
            },
            "date_created": 1595965782,
            "date_updated": 1595965782,
            "status": {
                "id": 1,
                "name": "active"
            }
        }
    ],
    "paging": {
        "prev": null,
        "next": null
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/users/:user\_id" %}
{% api-method-summary %}
Get Linked User Details
{% endapi-method-summary %}

{% api-method-description %}
Return the details of a single user linked to an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="string" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_id" type="string" required=true %}
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
Successfully retrieved a linked user's details.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 4,
    "user": {
        "id": 2,
        "email": "john@mtgbracket.com",
        "first_name": "john",
        "last_name": "smith",
        "birthday": 1575158400,
        "tier": {
            "id": 1,
            "name": "beta",
            "description": "A free tier allowing full, unrestricted access to all of the mtgbracket's features!",
            "rank": 1
        },
        "date_created": 1595203200,
        "date_updated": 1595203200,
        "status": {
            "id": 2,
            "name": "inactive"
        }
    },
    "role": {
        "id": 1,
        "name": "user"
    },
    "date_created": 1595965782,
    "date_updated": 1595965782,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/users" %}
{% api-method-summary %}
Add User
{% endapi-method-summary %}

{% api-method-description %}
Link a user to an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="role\_id" type="integer" required=true %}
Role ID.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully added a user to an organization.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 4,
    "user": {
        "id": 2,
        "email": "john@mtgbracket.com",
        "first_name": "john",
        "last_name": "smith",
        "birthday": 1575158400,
        "tier": {
            "id": 1,
            "name": "beta",
            "description": "A free tier allowing full, unrestricted access to all of the mtgbracket's features!",
            "rank": 1
        },
        "date_created": 1595203200,
        "date_updated": 1595203200,
        "status": {
            "id": 2,
            "name": "inactive"
        }
    },
    "role": {
        "id": 1,
        "name": "user"
    },
    "date_created": 1595965782,
    "date_updated": 1595965782,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/users/:user\_id" %}
{% api-method-summary %}
Update User
{% endapi-method-summary %}

{% api-method-description %}
Update a linked user's role with an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="role\_id" type="integer" required=false %}
Role ID.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully updated a linked user.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 4,
    "user": {
        "id": 2,
        "email": "john@mtgbracket.com",
        "first_name": "john",
        "last_name": "smith",
        "birthday": 1575158400,
        "tier": {
            "id": 1,
            "name": "beta",
            "description": "A free tier allowing full, unrestricted access to all of the mtgbracket's features!",
            "rank": 1
        },
        "date_created": 1595203200,
        "date_updated": 1595203200,
        "status": {
            "id": 2,
            "name": "inactive"
        }
    },
    "role": {
        "id": 2,
        "name": "organizer"
    },
    "date_created": 1595965782,
    "date_updated": 1595965966,
    "status": {
        "id": 1,
        "name": "active"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/users/:user\_id" %}
{% api-method-summary %}
Remove User
{% endapi-method-summary %}

{% api-method-description %}
Remove a linked user from an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}

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
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}
Successfully removed a user from an organization.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

