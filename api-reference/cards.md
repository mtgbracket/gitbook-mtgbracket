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

{% endapi-method-response-example-description %}

```

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

{% endapi-method-response-example-description %}

```

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

{% endapi-method-response-example-description %}

```

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

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

