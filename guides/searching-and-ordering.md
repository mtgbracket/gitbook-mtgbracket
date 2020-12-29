---
description: >-
  List APIs can be filtered or ordered using preset lists of key:value pairs
  that identify which records you are interested in.
---

# Searching & Ordering

## The Search Format

The root level `GET` API for any resource is considered the "list" API.  These "list" APIs will accept an optional `q` query-string parameter, which can be used to filter the list of returned results based on a suite of key:value pairs supported by that particular resource.

The following API would return a list of organizations that include the following string in their name:

{% tabs %}
{% tab title="HTTP" %}
```http
GET /organizations?q=n:misfit HTTP/1.1
Host: accounts.mtgbracket.com
Authorization: Bearer a3793ef87a1f47a5421f666f0dab6d48a0d95ac9e9eafddac798c2db35fb8d6681f6c49c84bbb06f
Content-Type: application/json
```
{% endtab %}

{% tab title="cUrl" %}
```
curl --location --request GET 'http://accounts.mtgbracket.com/organizations?q=n:misfit' \
--header 'Authorization: Bearer a3793ef87a1f47a5421f666f0dab6d48a0d95ac9e9eafddac798c2db35fb8d6681f6c49c84bbb06f' \
--header 'Content-Type: application/json'
```
{% endtab %}
{% endtabs %}

```javascript
{
    "items": [
        {
            "id": 1,
            "name": "misfitpixel 2",
            "date_created": 1585958400,
            "date_updated": 1606511147,
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

In the above example, we provided the key:value pair of `n:misfit` which instructs the _mtgbracket_ service that we are interested in organizations that include the string "misfit" somewhere in its **name**.

{% hint style="info" %}
All search parameters are considered AND conditions.  Returned results must satisfy all of the provided key:value pairs provided.
{% endhint %}

Different resources will support different keys that can be used to filter their results.  Those are listed below.

### Users

{% hint style="warning" %}
Search for users has not yet been implemented.
{% endhint %}

### Organizations

Users can search for organizations by name, or by a linked user's ID.

* name \[n\]
* user ID \[u\]

### Cards

Cards are unique in _mtgbracket_, in that they can be filtered using the native internal format, or using a popular external service called [Scryfall](https://www.scryfall.com).

Additional information about card searching can be found in a dedicated section here: 

{% page-ref page="exploring-cards/searching-for-cards.md" %}

### Decks

### Events

## Ordering Results

