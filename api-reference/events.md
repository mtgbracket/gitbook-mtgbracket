# Events

{% api-method method="get" host="https://api.mtgbracket.com" path="/events" %}
{% api-method-summary %}
Get Events
{% endapi-method-summary %}

{% api-method-description %}
Return a list of events.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved a list of events.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 11,
            "organization_id": 12,
            "name": "FNM",
            "rules": {
                "name": "Modern (house)",
                "tags": [
                    "constructed",
                    "fnm",
                    "modern"
                ],
                "cards": {
                    "banned": [],
                    "restricted": [],
                    "whitelisted": [],
                    "has_commander": false,
                    "allow_sideboards": true,
                    "max_library_size": null,
                    "min_library_size": 60,
                    "number_of_copies": 4,
                    "total_power_level": null,
                    "enforce_color_identity": false
                },
                "points": {
                    "win": 3,
                    "draw": 2,
                    "loss": 1
                },
                "rounds": {
                    "best_of": 3,
                    "duration": 3300,
                    "matchmaking_style": "swiss"
                },
                "players": {
                    "team_size": 1,
                    "default_number_per_round": 2
                },
                "starting_life_total": 20
            },
            "date_started": 1561040672,
            "date_ended": 1561040672,
            "date_created": 1561055147,
            "date_updated": 1586050754,
            "status": {
                "id": 2,
                "name": "inactive"
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

{% api-method method="get" host="https://api.mtgbracket.com" path="/events/:event\_id" %}
{% api-method-summary %}
Get Event Details
{% endapi-method-summary %}

{% api-method-description %}
Return the details of a single event.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved an event's details.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 11,
    "organization_id": 12,
    "name": "FNM",
    "rules": {
        "name": "Modern (house)",
        "tags": [
            "constructed",
            "fnm",
            "modern"
        ],
        "cards": {
            "banned": [],
            "restricted": [],
            "whitelisted": [],
            "has_commander": false,
            "allow_sideboards": true,
            "max_library_size": null,
            "min_library_size": 60,
            "number_of_copies": 4,
            "total_power_level": null,
            "enforce_color_identity": false
        },
        "points": {
            "win": 3,
            "draw": 2,
            "loss": 1
        },
        "rounds": {
            "best_of": 3,
            "duration": 3300,
            "matchmaking_style": "swiss"
        },
        "players": {
            "team_size": 1,
            "default_number_per_round": 2
        },
        "starting_life_total": 20
    },
    "date_started": 1561040672,
    "date_ended": 1561040672,
    "date_created": 1561055147,
    "date_updated": 1586050754,
    "status": {
        "id": 2,
        "name": "inactive"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/events/:event\_id/players" %}
{% api-method-summary %}
Get Event Players
{% endapi-method-summary %}

{% api-method-description %}
Return list of players registered for an event.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
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
Successfully retrieved list of players for this event.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 1,
            "date_created": 1595203200,
            "date_updated": 1595203200,
            "status": {
                "id": 1,
                "name": "active"
            },
            "deck": {
                "id": 1,
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
                    }
                ]
            },
            "player": {
                "id": 1,
                "number": "999999010",
                "username": "polkadothippo",
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

{% api-method method="post" host="https://api.mtgbracket.com" path="/events/:event\_id/players" %}
{% api-method-summary %}
Register a Player
{% endapi-method-summary %}

{% api-method-description %}
Registers a player to an event.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully registered a player to an event.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 1,
    "date_created": 1595203200,
    "date_updated": 1595203200,
    "status": {
        "id": 1,
        "name": "active"
    },
    "deck": {
        "id": 1,
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
            }
        ]
    },
    "player": {
        "id": 1,
        "number": "999999010",
        "username": "polkadothippo",
        "status": {
            "id": 1,
            "name": "active"
        }
    }
},
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.mtgbracket.com" path="/events/:event\_id/players/:player\_id" %}
{% api-method-summary %}
Remove a Player
{% endapi-method-summary %}

{% api-method-description %}
Removes a player from an event.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="player\_id" type="integer" required=true %}
Player's unique ID.
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

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/events/:event\_id/rounds/:round\_number" %}
{% api-method-summary %}
Get Round
{% endapi-method-summary %}

{% api-method-description %}
Return details of a particular round.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="round\_number" type="integer" required=true %}
Round number.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
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

{% api-method method="post" host="https://api.mtgbracket.com" path="/events/:event\_id/rounds" %}
{% api-method-summary %}
Start Round
{% endapi-method-summary %}

{% api-method-description %}
Start a new round and generate pairings from the registered players.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
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
Successfully retrieved round details.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 55,
    "number": 1,
    "pairing_size": 2,
    "date_started": null,
    "date_ended": null,
    "matchmaking_type": {
        "id": 1,
        "name": "swiss"
    },
    "date_created": 1586098416,
    "date_updated": 1586098416,
    "status": {
        "id": 1,
        "name": "active"
    },
    "pairings": []
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/events" %}
{% api-method-summary %}
Get Organization Events
{% endapi-method-summary %}

{% api-method-description %}
Get events from an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved a list of events for an organization.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 11,
            "organization_id": 12,
            "name": "FNM",
            "rules": {
                "name": "Modern (house)",
                "tags": [
                    "constructed",
                    "fnm",
                    "modern"
                ],
                "cards": {
                    "banned": [],
                    "restricted": [],
                    "whitelisted": [],
                    "has_commander": false,
                    "allow_sideboards": true,
                    "max_library_size": null,
                    "min_library_size": 60,
                    "number_of_copies": 4,
                    "total_power_level": null,
                    "enforce_color_identity": false
                },
                "points": {
                    "win": 3,
                    "draw": 2,
                    "loss": 1
                },
                "rounds": {
                    "best_of": 3,
                    "duration": 3300,
                    "matchmaking_style": "swiss"
                },
                "players": {
                    "team_size": 1,
                    "default_number_per_round": 2
                },
                "starting_life_total": 20
            },
            "date_started": 1561040672,
            "date_ended": 1561040672,
            "date_created": 1561055147,
            "date_updated": 1586050754,
            "status": {
                "id": 2,
                "name": "inactive"
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

{% api-method method="post" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/events" %}
{% api-method-summary %}
Create Event
{% endapi-method-summary %}

{% api-method-description %}
Create a new event under an organization.
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
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully created a new event for an organization.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 12,
    "organization_id": 12,
    "name": "FNM",
    "rules": {
        "name": "Standard",
        "tags": [
            "constructed",
            "fnm",
            "standard"
        ],
        "cards": {
            "banned": [
                {
                    "id": "n:Rampaging Ferocidon"
                }
            ],
            "restricted": [],
            "whitelisted": [
                {
                    "id": "s:WAR"
                },
                {
                    "id": "s:RNA"
                },
                {
                    "id": "s:GRN"
                },
                {
                    "id": "s:M19"
                },
                {
                    "id": "s:DOM"
                },
                {
                    "id": "s:RIX"
                },
                {
                    "id": "s:XLN"
                }
            ],
            "has_commander": false,
            "allow_sideboards": true,
            "max_library_size": null,
            "min_library_size": 60,
            "number_of_copies": 4,
            "total_power_level": null,
            "enforce_color_identity": false
        },
        "points": {
            "win": 3,
            "draw": 2,
            "loss": 1
        },
        "rounds": {
            "best_of": 3,
            "duration": 3300,
            "matchmaking_style": "swiss"
        },
        "players": {
            "team_size": 1,
            "default_number_per_round": 2
        },
        "starting_life_total": 20
    },
    "date_started": 1585187379,
    "date_ended": null,
    "date_created": 1595968093,
    "date_updated": 1595968093,
    "status": {
        "id": 2,
        "name": "inactive"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/events/:event\_id" %}
{% api-method-summary %}
Update Event
{% endapi-method-summary %}

{% api-method-description %}
Update an event under an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=true %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
Event's name.
{% endapi-method-parameter %}

{% api-method-parameter name="date\_started" type="integer" required=false %}
Event's start date.
{% endapi-method-parameter %}

{% api-method-parameter name="date\_ended" type="integer" required=false %}
Event's end date.
{% endapi-method-parameter %}

{% api-method-parameter name="rules" type="object" required=false %}
Event's rule data.
{% endapi-method-parameter %}

{% api-method-parameter name="status\_id" type="integer" required=false %}
Event's status ID.
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully updated an event.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 12,
    "organization_id": 12,
    "name": "FNM 2",
    "rules": {
        "name": "Standard",
        "tags": [
            "constructed",
            "fnm",
            "standard"
        ],
        "cards": {
            "banned": [
                {
                    "id": "n:Rampaging Ferocidon"
                }
            ],
            "restricted": [],
            "whitelisted": [
                {
                    "id": "s:WAR"
                },
                {
                    "id": "s:RNA"
                },
                {
                    "id": "s:GRN"
                },
                {
                    "id": "s:M19"
                },
                {
                    "id": "s:DOM"
                },
                {
                    "id": "s:RIX"
                },
                {
                    "id": "s:XLN"
                }
            ],
            "has_commander": false,
            "allow_sideboards": true,
            "max_library_size": null,
            "min_library_size": 60,
            "number_of_copies": 4,
            "total_power_level": null,
            "enforce_color_identity": false
        },
        "points": {
            "win": 3,
            "draw": 2,
            "loss": 1
        },
        "rounds": {
            "best_of": 3,
            "duration": 3300,
            "matchmaking_style": "swiss"
        },
        "players": {
            "team_size": 1,
            "default_number_per_round": 2
        },
        "starting_life_total": 20
    },
    "date_started": 1585187379,
    "date_ended": 1585187379,
    "date_created": 1595968093,
    "date_updated": 1595968221,
    "status": {
        "id": 2,
        "name": "inactive"
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="https://api.mtgbracket.com" path="/organizations/:organization\_id/events/:event\_id" %}
{% api-method-summary %}
Delete Event
{% endapi-method-summary %}

{% api-method-description %}
Delete an event under an organization.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="organization\_id" type="integer" required=true %}
Organization's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="event\_id" type="integer" required=true %}
Event's unique ID.
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
Successfully deleted an event.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

