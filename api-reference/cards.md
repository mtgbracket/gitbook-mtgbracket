---
description: >-
  Cards are read-only resources that are primarily linked to decks.  We provide
  a number of different ways to browse card data in order to help users link
  cards to their decks.
---

# Cards

{% api-method method="get" host="https://api.mtgbracket.com" path="/expansions" %}
{% api-method-summary %}
Expansions
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of expansions supported by _mtgbracket_.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully return a list of available expansions.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 1,
            "code": "LEA",
            "name": "Limited Edition Alpha",
            "release_date": 744508800,
            "parent": null,
            "featured_card": null
        },
        {
            "id": 2,
            "code": "LEB",
            "name": "Limited Edition Beta",
            "release_date": 749433600,
            "parent": null,
            "featured_card": null
        },
        {
            "id": 3,
            "code": "2ED",
            "name": "Unlimited Edition",
            "release_date": 754704000,
            "parent": null,
            "featured_card": null
        },
        {
            "id": 19,
            "code": "ARN",
            "name": "Arabian Nights",
            "release_date": 754704000,
            "parent": null,
            "featured_card": null
        },
        {
            "id": 20,
            "code": "ATQ",
            "name": "Antiquities",
            "release_date": 762480000,
            "parent": null,
            "featured_card": null
        },
        {
            "id": 4,
            "code": "3ED",
            "name": "Revised Edition",
            "release_date": 765158400,
            "parent": null,
            "featured_card": null
        }
        ...
    ],
    "paging": {
        "prev": null,
        "next": "https://api.mtgbracket.com/expansions/?page=2&limit=50"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com/expansions" path="/:expansion\_code/cards" %}
{% api-method-summary %}
Expansion Cards
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of cards in an expansion.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="expansion\_code" type="string" required=true %}
Three-character expansion code.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully returned a list of cards for a given expansion.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 602,
            "multiverse_id": 232,
            "name": "Animate Wall",
            "text": "Enchant Wall\nEnchanted Wall can attack as though it didn't have defender.",
            "power": null,
            "toughness": null,
            "mana_cost": "{W}",
            "converted_mana_cost": 1,
            "color_identity": "w",
            "flavor": null,
            "number": 1,
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
                "id": 10,
                "user_id": null,
                "credit": "Dan Frazier",
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
        {
            "id": 604,
            "multiverse_id": 233,
            "name": "Armageddon",
            "text": "Destroy all lands.",
            "power": null,
            "toughness": null,
            "mana_cost": "{3}{W}",
            "converted_mana_cost": 4,
            "color_identity": "w",
            "flavor": null,
            "number": 2,
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
                "id": 12,
                "user_id": null,
                "credit": "Jesper Myrfors",
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
        {
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
        ...
    ],
    "paging": {
        "prev": null,
        "next": "https://api.mtgbracket.com/expansions/lea/cards?page=2&limit=50"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgrabcket.com" path="/expansions/:expansion\_code/cards/:card\_id/decks" %}
{% api-method-summary %}
Decks Using a Card
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of decks using a particular card.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully returned a list of decks.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 2,
            "user_id": 9,
            "name": "My Super Secret Tech",
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

{% api-method method="get" host="https://api.mtgbracket.com" path="/cards/search?q=:query" %}
{% api-method-summary %}
Search for a Card
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of cards matching criteria provided by a search query.  Searching in mtgbracket follows a specific format:  
  
`key`:`criteria`   
  
Example: /cards/search?q=c:redt:creature  
  
Would look for `red` `creature` cards.  More information can be found under the Searching for Cards guide.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="query" type="string" required=false %}
Search string
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully returned a list of cards matching the search query.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 13180,
            "multiverse_id": 79110,
            "name": "Honden of Infinite Rage",
            "text": "At the beginning of your upkeep, Honden of Infinite Rage deals damage to any target equal to the number of Shrines you control.",
            "power": null,
            "toughness": null,
            "mana_cost": "{2}{R}",
            "converted_mana_cost": 3,
            "color_identity": "r",
            "flavor": "To the sorrow of all, its rage became focused on those who once stoked it.",
            "number": 172,
            "loyalty": null,
            "expansion": {
                "id": 52,
                "code": "CHK",
                "name": "Champions of Kamigawa",
                "release_date": 1096588800,
                "parent": null,
                "featured_card": null
            },
            "rarity": {
                "id": 2,
                "name": "uncommon"
            },
            "artist": {
                "id": 2283,
                "user_id": null,
                "credit": "John Avon",
                "first_name": null,
                "last_name": null,
                "homepage_url": null,
                "date_created": 1584387881,
                "date_updated": 1584387881,
                "status": {
                    "id": 1,
                    "name": "active"
                }
            }
        },
        ...
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

