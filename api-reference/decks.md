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
{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=false %}
OAuth 2.0 Bearer token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
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

{% api-method-headers %}
{% api-method-parameter name="Authorization" type="string" required=false %}
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
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

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

{% endapi-method-response-example-description %}

```

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
{% api-method-response-example httpCode=200 %}
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

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

