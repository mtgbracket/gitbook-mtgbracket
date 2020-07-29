---
description: >-
  Decks are a collection of cards that are arbitrarily organized by their
  owners. Decks are required to participate in events.
---

# Decks

{% api-method method="get" host="https://api.mtgbracket.com" path="/decks" %}
{% api-method-summary %}
Get Decks
{% endapi-method-summary %}

{% api-method-description %}
Return a list of decks
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully returned a list of decks.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 42,
            "user_id": 1,
            "name": "Icy Ded Ppl",
            "code": "syypdt",
            "date_created": 1595961088,
            "date_updated": 1595961088,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 1,
            "user_id": 1,
            "name": "Super Secret Tech",
            "code": "9dj7ry",
            "date_created": 1586217600,
            "date_updated": 1586217600,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 34,
            "user_id": 4,
            "name": "Ninja Death Squad of Death",
            "code": "hdg461",
            "date_created": 1586217600,
            "date_updated": 1586217600,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 35,
            "user_id": 5,
            "name": "Spilled the Salt",
            "code": "ueh637",
            "date_created": 1586217600,
            "date_updated": 1586217600,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 2,
            "user_id": 9,
            "name": "Flying Pinjata",
            "code": "iyzwmv",
            "date_created": 1585755223,
            "date_updated": 1585755223,
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

{% api-method method="get" host="https://api.mtgbracket.com" path="/decks/:deck\_code" %}
{% api-method-summary %}
Get Deck Details
{% endapi-method-summary %}

{% api-method-description %}
Return the details of a particular deck including all cards.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="deck\_code" type="string" required=true %}
Deck's unique alphanumeric code.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved deck details.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "user_id": 1,
    "name": "Super Secret Tech",
    "code": "9dj7ry",
    "date_created": 1586217600,
    "date_updated": 1586217600,
    "status": {
        "id": 1,
        "name": "active"
    },
    "data": [],
    "cards": [
        {
            "card": {
                "id": 608,
                "multiverse_id": 234,
                "name": "Balance",
                "text": "Each player chooses a number of lands they control equal to the number of lands controlled by the player who controls the fewest, then sacrifices the rest. Players discard cards and sacrifice creatures the same way.",
                "power": null,
                "toughness": null,
                "mana_cost": "{1}{W}",
                "converted_mana_cost": 2,
                "color_identity": "w",
                "flavor": null,
                "number": 3,
                "loyalty": null,
                "expansion": {
                    "id": 1,
                    "code": "LEA",
                    "name": "Limited Edition Alpha",
                    "release_date": 744508800,
                    "parent": null,
                    "featured_card": null
                },
                "rarity": {
                    "id": 3,
                    "name": "rare"
                },
                "artist": {
                    "id": 7,
                    "user_id": null,
                    "credit": "Mark Poole",
                    "first_name": null,
                    "last_name": null,
                    "homepage_url": null,
                    "date_created": 1584318168,
                    "date_updated": 1584318168,
                    "status": {
                        "id": 1,
                        "name": "active"
                    }
                }
            },
            "quantity": 1,
            "is_sideboard": false
        },
        ...
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://api.mtgbracket.com" path="/decks" %}
{% api-method-summary %}
Create Deck
{% endapi-method-summary %}

{% api-method-description %}
Create a new deck.  If no `Authorization` header is provided, the deck is created under an anonymous user and will not be editable.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Deck's name.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully created deck.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 43,
    "user_id": 1,
    "name": "Faeries OP",
    "code": "wuyksj",
    "date_created": 1595964874,
    "date_updated": 1595964874,
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

{% api-method method="put" host="https://api.mtgbracket.com" path="/decks/:deck\_code" %}
{% api-method-summary %}
Update Deck
{% endapi-method-summary %}

{% api-method-description %}
Update a deck.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="deck\_code" type="string" required=true %}
Deck's unique alphanumeric code.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
Deck's name.
{% endapi-method-parameter %}

{% api-method-parameter name="data" type="string" required=false %}
Deck structural and configuration metadata.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully updated a deck
{% endapi-method-response-example-description %}

```javascript
{
    "id": 43,
    "user_id": 1,
    "name": "Faeries Rediculously OP",
    "code": "wuyksj",
    "date_created": 1595964874,
    "date_updated": 1595964968,
    "status": {
        "id": 1,
        "name": "active"
    },
    "data": {
        "columns": [
            {
                "name": "lands",
                "cards": []
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.mtgbracket.com" path="/decks/:deck\_code" %}
{% api-method-summary %}
Delete Deck
{% endapi-method-summary %}

{% api-method-description %}
Delete a deck.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="deck\_code" type="string" required=true %}
Deck's unique alphanumeric code.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=204 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/events/:event\_id/decks/:deck\_code/validity" %}
{% api-method-summary %}
Check Deck Validity
{% endapi-method-summary %}

{% api-method-description %}
Check if a deck meets an event's eligibility requirements.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=false %}
Event's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="deck\_code" type="string" required=true %}
Deck's unique alphanumeric code.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully determined deck's eligibility status for an event.
{% endapi-method-response-example-description %}

```javascript
{
    "valid": false,
    "rules": {
        "banned": [],
        "restricted": [],
        "whitelisted": [],
        "has_commander": true,
        "allow_sideboards": true,
        "max_library_size": true,
        "min_library_size": false,
        "number_of_copies": [],
        "total_power_level": true,
        "enforce_color_identity": true
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

