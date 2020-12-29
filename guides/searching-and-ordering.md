---
description: >-
  List APIs can be filtered or ordered using preset lists of key:value pairs
  that identify which records you are interested in.
---

# Searching, Paging, and Ordering

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

Cards are unique in _mtgbracket_, in that they can be filtered using the native internal format, or using a popular external service called [_Scryfall_](https://www.scryfall.com).

Additional information about card searching can be found in a dedicated section here: 

{% page-ref page="exploring-cards/searching-for-cards.md" %}

### Expansions

Users can also search for individual Magic: the Gathering expansions rather than cards themselves.  They can be filtered by name, set code, parent block name, parent block code, release date, release year, or by the name of a card contained by that expansion.

* name \[n\]
* code \[o\]
* parent block name \[p\]
* parent block code \[po\]
* release date \[d\]
* release year \[y\]
* card name \[c\]

### Decks

Users can search for decks by the user ID of its creator, by name, by created date, or by the name of a card contained by that deck.

* user ID \[u\]
* name \[n\]
* created date \[d\]
* card name \[c\]

### Events

Events can be found by name, the organization running them, start date, format, or by location.

* name \[n\]
* organization ID \[o\]
* start date \[d\]
* format \[f\]
* latitude \[lt\]
* longitude \[ln\]

## Paging and Ordering Results

Whenever an mtgbracket API returns more than a single resource, the result set will be contained inside an `"items"` array within the JSON response body.  Additionally, that response will also include a `"paging"` object which will contain shortcut URLs to the previous and next pages of results, if applicable.

By default, most results are limited to **50** results per response, but this number can be increased or decreased as needed.

Limits can be set by providing a `limit` parameter in your API request, which contains an integer meant to represent the maximum number of results you would like to retrieve.

Moving up and down the "pages" of results is as easy as adding a `page` parameter along with your limit.  Each new page will return a different subset of your total results.

Finally, results can be sorted using an `order` parameter.  The `order` parameter uses the same key:value format as the search query, but with the exception being that the _value_ portion can only be one of two possible strings: `asc` or `desc`.

In almost all cases, you will be able to order any result set by any **root key** of the primary object returned in the response.

The following example will illustrate the expected result when we put everything together.

{% tabs %}
{% tab title="HTTP" %}
```http
GET /organizations?q=n:shop&order=date_created:desc&limit=5 HTTP/1.1
Host: accounts.mtgbracket.com
Authorization: Bearer a3793ef87a1f47a5421f666f0dab6d48a0d95ac9e9eafddac798c2db35fb8d6681f6c49c84bbb06f
Content-Type: application/json
```
{% endtab %}

{% tab title="cURL" %}
```
curl --location --request GET 'http://accounts.mtgbracket.com/organizations?q=n:shop&order=date_created:desc&limit=5' \
--header 'Authorization: Bearer a3793ef87a1f47a5421f666f0dab6d48a0d95ac9e9eafddac798c2db35fb8d6681f6c49c84bbb06f' \
--header 'Content-Type: application/json'
```
{% endtab %}
{% endtabs %}

```javascript
{
    "items": [
        {
            "id": 2493,
            "name": "Elizabeth's Magic Shop",
            "date_created": 1600435892,
            "date_updated": 1600435892,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 2483,
            "name": "Amelia's Fantasy Shoppe",
            "date_created": 1600435891,
            "date_updated": 1600435891,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 2478,
            "name": "Antoine's Geek Shoppe",
            "date_created": 1600435890,
            "date_updated": 1600435890,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 2481,
            "name": "Sarah's Game Shop",
            "date_created": 1600435890,
            "date_updated": 1600435890,
            "status": {
                "id": 1,
                "name": "active"
            }
        },
        {
            "id": 2464,
            "name": "Samuel's Fantasy Shop",
            "date_created": 1600435889,
            "date_updated": 1600435889,
            "status": {
                "id": 1,
                "name": "active"
            }
        }
    ],
    "paging": {
        "prev": null,
        "next": "http://accounts.mtgbracket.com/organizations/?order=date_created%3Adesc&q=n%3Ashop&page=2&limit=5"
    }
}
```

