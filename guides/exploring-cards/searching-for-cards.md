---
description: >-
  Our service allows for searching for card records using our native query
  format, or using the popular Scryfall format.
---

# Searching Cards

_Mtgbracket_ provides an interface for users to search for cards, whether it's just for browsing, or for building and tuning their decks.

We support searching using our own native search format, or by using [_Scryfall's_](https://scryfall.com) more advanced syntax.

## Native Search

By default, _mtgbracket_ provides this functionality through its native search implementation, which supports searching for cards using the following criteria:

* colour \[c\]
* colour identity \[ci\]
* type \[t\]
* rarity \[r\]
* set/expansion \[s\]
* name \[n\]
* converted mana cost \[cmc\]
* mana cost \[m\]
* power \[p\]
* toughness \[d\]
* loyalty \[l\]
* oracle text \[o\]

Search parameters are cumulative and are layered separated by spaces in the URL.  Each search token is denoted using a key:value block.

_Example_: 

`https://api.mtgbracket.com/cards/search?q=t:creature%20t:legendary%20ci:uw`

This search includes the **type** and **colour identity** criteria.

This would return a result set that includes `creatures` that are `legendary` with a `colour identity` of `blue` and `white`.

{% hint style="info" %}
Take a look at the [Cards API reference](../../api-reference/cards.md#search-for-a-card) to review the data schema.
{% endhint %}

Criteria in your search query are treated as **AND** conditions, and will only return results that match all entered criteria.

{% hint style="info" %}
Optionally, you can perform searches using [Scryfall](https://scryfall.com) instead, which supports more complex queries.  The default search engine can be set by users in their preferences.
{% endhint %}

## Scryfall Search

Mtgbracket also supports executing searches against the [_Scryfall_](https://scryfall.com) API instead.  This can be done ad-hoc by users in the search bar, or by setting the default search provider to [_Scryfall_](https://scryfall.com) in their preferences.

Details about the [_Scryfall_](https://www.scryfall.com) search syntax can be found here:

{% embed url="https://scryfall.com/docs/syntax" %}

