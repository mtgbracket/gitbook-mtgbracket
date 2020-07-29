---
description: >-
  Rulesets are templates for event configuration.  We provide default Rulesets
  to function as templates, which can be extended, modified, or shared by other
  users.
---

# Rulesets

{% api-method method="get" host="https://api.mtgbracket.com" path="/rulesets" %}
{% api-method-summary %}
Get Rulesets
{% endapi-method-summary %}

{% api-method-description %}
Returns a list of the default rulesets.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved a list of rulesets.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 1,
            "user_id": null,
            "name": "standard",
            "data": {
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
            }
        },
        {
            "id": 2,
            "user_id": null,
            "name": "modern",
            "data": {
                "name": "Modern",
                "tags": [
                    "constructed",
                    "modern"
                ],
                "cards": {
                    "banned": [
                        {
                            "id": "s:LEA"
                        },
                        {
                            "id": "s:LEB"
                        },
                        {
                            "id": "s:2ED"
                        },
                        {
                            "id": "s:3ED"
                        },
                        {
                            "id": "s:4ED"
                        },
                        {
                            "id": "s:5ED"
                        },
                        {
                            "id": "s:6ED"
                        },
                        {
                            "id": "s:7ED"
                        },
                        {
                            "id": "s:ARN"
                        },
                        {
                            "id": "s:ATQ"
                        },
                        {
                            "id": "s:LEG"
                        },
                        {
                            "id": "s:DRK"
                        },
                        {
                            "id": "s:FEM"
                        },
                        {
                            "id": "s:HML"
                        },
                        {
                            "id": "s:ICE"
                        },
                        {
                            "id": "s:ALL"
                        },
                        {
                            "id": "s:MIR"
                        },
                        {
                            "id": "s:VIS"
                        },
                        {
                            "id": "s:WTH"
                        },
                        {
                            "id": "s:TMP"
                        },
                        {
                            "id": "s:STH"
                        },
                        {
                            "id": "s:EXO"
                        },
                        {
                            "id": "s:USG"
                        },
                        {
                            "id": "s:ULG"
                        },
                        {
                            "id": "s:UDS"
                        },
                        {
                            "id": "s:MMQ"
                        },
                        {
                            "id": "s:NEM"
                        },
                        {
                            "id": "s:PCY"
                        },
                        {
                            "id": "s:INV"
                        },
                        {
                            "id": "s:PLS"
                        },
                        {
                            "id": "s:APC"
                        },
                        {
                            "id": "s:ODY"
                        },
                        {
                            "id": "s:TOR"
                        },
                        {
                            "id": "s:JUD"
                        },
                        {
                            "id": "s:ONS"
                        },
                        {
                            "id": "s:LEG"
                        },
                        {
                            "id": "s:SCG"
                        },
                        {
                            "id": "n:Ancient Den"
                        },
                        {
                            "id": "n:Birthing Pod"
                        },
                        {
                            "id": "n:Blazing Shoal"
                        },
                        {
                            "id": "n:Chrome Mox"
                        },
                        {
                            "id": "n:Cloudpost"
                        },
                        {
                            "id": "n:Dark Depths"
                        },
                        {
                            "id": "n:Deathrite Shaman"
                        },
                        {
                            "id": "n:Dig Through Time"
                        },
                        {
                            "id": "n:Dread Return"
                        },
                        {
                            "id": "n:Eye of Ugin"
                        },
                        {
                            "id": "n:Gitaxian Probe"
                        },
                        {
                            "id": "n:Glimpse of Nature"
                        },
                        {
                            "id": "n:Golgari Grave-Troll"
                        },
                        {
                            "id": "n:Great Furnace"
                        },
                        {
                            "id": "n:Green Sun's Zenith"
                        },
                        {
                            "id": "n:Hypergenesis"
                        },
                        {
                            "id": "n:Mental Misstep"
                        },
                        {
                            "id": "n:Ponder"
                        },
                        {
                            "id": "n:Preordain"
                        },
                        {
                            "id": "n:Punishing Fire"
                        },
                        {
                            "id": "n:Rite of Flame"
                        },
                        {
                            "id": "n:Seat of the Synod"
                        },
                        {
                            "id": "n:Second Sunrise"
                        },
                        {
                            "id": "n:Seething Song"
                        },
                        {
                            "id": "n:Sensei's Divining Top"
                        },
                        {
                            "id": "n:Skullclamp"
                        },
                        {
                            "id": "n:Splinter Twin"
                        },
                        {
                            "id": "n:Stoneforge Mystic"
                        },
                        {
                            "id": "n:Summer Bloom"
                        },
                        {
                            "id": "n:Treasure Cruise"
                        },
                        {
                            "id": "n:Tree of Tales"
                        },
                        {
                            "id": "n:Umezawa's Jitte"
                        },
                        {
                            "id": "n:Vault of Whispers"
                        }
                    ],
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
            }
        },
        {
            "id": 3,
            "user_id": null,
            "name": "legacy",
            "data": {
                "name": "Legacy",
                "tags": [
                    "constructed",
                    "legacy"
                ],
                "cards": {
                    "banned": [
                        {
                            "id": "n:Adriana's Valor"
                        },
                        {
                            "id": "n:Advantageous Proclamation"
                        },
                        {
                            "id": "n:Assemble the Rank and Vile"
                        },
                        {
                            "id": "n:Backup Plan"
                        },
                        {
                            "id": "n:Brago's Favor"
                        },
                        {
                            "id": "n:Double Stroke"
                        },
                        {
                            "id": "n:Echoing Boon"
                        },
                        {
                            "id": "n:Emissary's Ploy"
                        },
                        {
                            "id": "n:Hired Heist"
                        },
                        {
                            "id": "n:Hold the Perimeter"
                        },
                        {
                            "id": "n:Hymn of the Wilds"
                        },
                        {
                            "id": "n:Immediate Action"
                        },
                        {
                            "id": "n:Incendiary Dissent"
                        },
                        {
                            "id": "n:Iterative Analysis"
                        },
                        {
                            "id": "n:Muzzlo's Preparations"
                        },
                        {
                            "id": "n:Natural Unity"
                        },
                        {
                            "id": "n:Power Play"
                        },
                        {
                            "id": "n:Secret Summoning"
                        },
                        {
                            "id": "n:Secret's of Paradise"
                        },
                        {
                            "id": "n:Sentinel Dispatch"
                        },
                        {
                            "id": "n:Sovereign's Realm"
                        },
                        {
                            "id": "n:Summoner's Bond"
                        },
                        {
                            "id": "n:Unexpected Potential"
                        },
                        {
                            "id": "n:Weight Advantage"
                        },
                        {
                            "id": "n:Amulet of Quoz"
                        },
                        {
                            "id": "n:Bronze Tablet"
                        },
                        {
                            "id": "n:Contract from Below"
                        },
                        {
                            "id": "n:Darkpact"
                        },
                        {
                            "id": "n:Demonic Attourney"
                        },
                        {
                            "id": "n:Jeweled Bird"
                        },
                        {
                            "id": "n:Rebirth"
                        },
                        {
                            "id": "n:Tempest Efreet"
                        },
                        {
                            "id": "n:Timmerian Fiends"
                        },
                        {
                            "id": "n:Ancestral Recall"
                        },
                        {
                            "id": "n:Balance"
                        },
                        {
                            "id": "n:Bazaar of Baghdad"
                        },
                        {
                            "id": "n:Black Lotus"
                        },
                        {
                            "id": "n:Channel"
                        },
                        {
                            "id": "n:Chaos Orb"
                        },
                        {
                            "id": "n:Demonic Consultation"
                        },
                        {
                            "id": "n:Demonic Tutor"
                        },
                        {
                            "id": "n:Dig Through Time"
                        },
                        {
                            "id": "n:Earthcraft"
                        },
                        {
                            "id": "n:Falling Star"
                        },
                        {
                            "id": "n:Fastbond"
                        },
                        {
                            "id": "n:Flash"
                        },
                        {
                            "id": "n:Frantic Search"
                        },
                        {
                            "id": "n:Goblin Recruiter"
                        },
                        {
                            "id": "n:Gush"
                        },
                        {
                            "id": "n:Hermit Druid"
                        },
                        {
                            "id": "n:Imperial Seal"
                        },
                        {
                            "id": "n:Library of Alexandria"
                        },
                        {
                            "id": "n:Mana Crypt"
                        },
                        {
                            "id": "n:Mana Drain"
                        },
                        {
                            "id": "n:Mana Vault"
                        },
                        {
                            "id": "n:Memory Jar"
                        },
                        {
                            "id": "n:Mental Misstep"
                        },
                        {
                            "id": "n:Mind Twist"
                        },
                        {
                            "id": "n:Mind's Desire"
                        },
                        {
                            "id": "n:Mishra's Workshop"
                        },
                        {
                            "id": "n:Mox Emerald"
                        },
                        {
                            "id": "n:Mox Jet"
                        },
                        {
                            "id": "n:Mox Pearl"
                        },
                        {
                            "id": "n:Mox Ruby"
                        },
                        {
                            "id": "n:Mox Sapphire"
                        },
                        {
                            "id": "n:Mystical Tutor"
                        },
                        {
                            "id": "n:Necropotence"
                        },
                        {
                            "id": "n:Oath of Druids"
                        },
                        {
                            "id": "n:Shahrazad"
                        },
                        {
                            "id": "n:Skullclamp"
                        },
                        {
                            "id": "n:Sol Ring"
                        },
                        {
                            "id": "n:Strip Mine"
                        },
                        {
                            "id": "n:Survival of the Fittest"
                        },
                        {
                            "id": "n:Time Vault"
                        },
                        {
                            "id": "n:Time Walk"
                        },
                        {
                            "id": "n:Timetwister"
                        },
                        {
                            "id": "n:Tinker"
                        },
                        {
                            "id": "n:Tolarian Academy"
                        },
                        {
                            "id": "n:Treasure Cruise"
                        },
                        {
                            "id": "n:Vampiric Tutor"
                        },
                        {
                            "id": "n:Wheel of Fortune"
                        },
                        {
                            "id": "n:Windfall"
                        },
                        {
                            "id": "n:Yawgmoth's Bargain"
                        },
                        {
                            "id": "n:Yawgmoth's Will"
                        }
                    ],
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
            }
        },
        {
            "id": 4,
            "user_id": null,
            "name": "vintage",
            "data": {
                "name": "Vintage",
                "tags": [
                    "constructed",
                    "vintage"
                ],
                "cards": {
                    "banned": [
                        {
                            "id": "n:Chaos Orb"
                        },
                        {
                            "id": "n:Falling Star"
                        },
                        {
                            "id": "n:Shahrazad"
                        },
                        {
                            "id": "n:Adriana's Valor"
                        },
                        {
                            "id": "n:Advantageous Proclamation"
                        },
                        {
                            "id": "n:Assemble the Rank and Vile"
                        },
                        {
                            "id": "n:Backup Plan"
                        },
                        {
                            "id": "n:Brago's Favor"
                        },
                        {
                            "id": "n:Double Stroke"
                        },
                        {
                            "id": "n:Echoing Boon"
                        },
                        {
                            "id": "n:Emissary's Ploy"
                        },
                        {
                            "id": "n:Hired Heist"
                        },
                        {
                            "id": "n:Hold the Perimeter"
                        },
                        {
                            "id": "n:Hymn of the Wilds"
                        },
                        {
                            "id": "n:Immediate Action"
                        },
                        {
                            "id": "n:Incendiary Dissent"
                        },
                        {
                            "id": "n:Iterative Analysis"
                        },
                        {
                            "id": "n:Muzzlo's Preparations"
                        },
                        {
                            "id": "n:Natural Unity"
                        },
                        {
                            "id": "n:Power Play"
                        },
                        {
                            "id": "n:Secret Summoning"
                        },
                        {
                            "id": "n:Secret's of Paradise"
                        },
                        {
                            "id": "n:Sentinel Dispatch"
                        },
                        {
                            "id": "n:Sovereign's Realm"
                        },
                        {
                            "id": "n:Summoner's Bond"
                        },
                        {
                            "id": "n:Unexpected Potential"
                        },
                        {
                            "id": "n:Weight Advantage"
                        },
                        {
                            "id": "n:Amulet of Quoz"
                        },
                        {
                            "id": "n:Bronze Tablet"
                        },
                        {
                            "id": "n:Contract from Below"
                        },
                        {
                            "id": "n:Darkpact"
                        },
                        {
                            "id": "n:Demonic Attourney"
                        },
                        {
                            "id": "n:Jeweled Bird"
                        },
                        {
                            "id": "n:Rebirth"
                        },
                        {
                            "id": "n:Tempest Efreet"
                        },
                        {
                            "id": "n:Timmerian Fiends"
                        }
                    ],
                    "restricted": [
                        {
                            "id": "n:Ancestral Recall"
                        },
                        {
                            "id": "n:Balance"
                        },
                        {
                            "id": "n:Black Lotus"
                        },
                        {
                            "id": "n:Brainstorm"
                        },
                        {
                            "id": "n:Chalice of the Void"
                        },
                        {
                            "id": "n:Chanel"
                        },
                        {
                            "id": "n:Demonic Consultation"
                        },
                        {
                            "id": "n:Demonic Tutor"
                        },
                        {
                            "id": "n:Dig Through Time"
                        },
                        {
                            "id": "n:Fastbond"
                        },
                        {
                            "id": "n:Flash"
                        },
                        {
                            "id": "n:Gitaxian Probe"
                        },
                        {
                            "id": "n:Gush"
                        },
                        {
                            "id": "n:Imperial Seal"
                        },
                        {
                            "id": "n:Library of Alexandria"
                        },
                        {
                            "id": "n:Lion's Eye Diamond"
                        },
                        {
                            "id": "n:Lodestone Golem"
                        },
                        {
                            "id": "n:Lotus Petal"
                        },
                        {
                            "id": "n:Mana Crypt"
                        },
                        {
                            "id": "n:Mana Vault"
                        },
                        {
                            "id": "n:Memory Jar"
                        },
                        {
                            "id": "n:Merchant Scroll"
                        },
                        {
                            "id": "n:Mind's Desire"
                        },
                        {
                            "id": "n:Monastary Mentor"
                        },
                        {
                            "id": "n:Mox Emerald"
                        },
                        {
                            "id": "n:Mox Jet"
                        },
                        {
                            "id": "n:Mox Pearl"
                        },
                        {
                            "id": "n:Mox Ruby"
                        },
                        {
                            "id": "n:Mox Sapphire"
                        },
                        {
                            "id": "n:Mystical Tutor"
                        },
                        {
                            "id": "n:Necropotence"
                        },
                        {
                            "id": "n:Ponder"
                        },
                        {
                            "id": "n:Sol Ring"
                        },
                        {
                            "id": "n:Strip Mine"
                        },
                        {
                            "id": "n:Thorn of Amethyst"
                        },
                        {
                            "id": "n:Time Vault"
                        },
                        {
                            "id": "n:Time Walk"
                        },
                        {
                            "id": "n:Timetwister"
                        },
                        {
                            "id": "n:Tinker"
                        },
                        {
                            "id": "n:Tolarian Academy"
                        },
                        {
                            "id": "n:Treasure Cruise"
                        },
                        {
                            "id": "n:Trinisphere"
                        },
                        {
                            "id": "n:Vampiric Tutor"
                        },
                        {
                            "id": "n:Wheel of Fortune"
                        },
                        {
                            "id": "n:Windfall"
                        },
                        {
                            "id": "n:Yawgmoth's Will"
                        }
                    ],
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
            }
        },
        {
            "id": 5,
            "user_id": null,
            "name": "pauper",
            "data": {
                "name": "Pauper",
                "tags": [
                    "constructed",
                    "pauper"
                ],
                "cards": {
                    "banned": [
                        {
                            "id": "r:mythic"
                        },
                        {
                            "id": "r: rare"
                        },
                        {
                            "id": "r:uncommon"
                        },
                        {
                            "id": "n:Cloud of Faeries"
                        },
                        {
                            "id": "n:Cloudpost"
                        },
                        {
                            "id": "n:Cranial Plating"
                        },
                        {
                            "id": "n:Daze"
                        },
                        {
                            "id": "n:Empty the Warrens"
                        },
                        {
                            "id": "n:Frantic Search"
                        },
                        {
                            "id": "n:Gitaxian Probe"
                        },
                        {
                            "id": "n:Grapeshot"
                        },
                        {
                            "id": "n:Gush"
                        },
                        {
                            "id": "n:Invigorate"
                        },
                        {
                            "id": "n:Peregrine Drake"
                        },
                        {
                            "id": "n:Temporal Fissure"
                        },
                        {
                            "id": "n:Treasure Cruise"
                        }
                    ],
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

{% api-method method="get" host="https://api.mtgbracket.com" path="/users/:user\_id/rulesets" %}
{% api-method-summary %}
Get a User's Rulesets
{% endapi-method-summary %}

{% api-method-description %}
Return a list of rulesets belonging to a user.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved a list of user's rulesets.
{% endapi-method-response-example-description %}

```javascript
{
    "items": [
        {
            "id": 6,
            "user_id": 1,
            "name": "Custom Rules",
            "data": {
                "name": "Custom Rules",
                "tags": [
                    "custom",
                    "for-fun"
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

{% api-method method="post" host="https://api.mtgbracket.com" path="/users/:user\_id/rulesets" %}
{% api-method-summary %}
Create Ruleset
{% endapi-method-summary %}

{% api-method-description %}
Create a new ruleset.
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
{% api-method-response-example httpCode=201 %}
{% api-method-response-example-description %}
Successfully created a custom ruleset.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 7,
    "user_id": 1,
    "name": "Three-Headed Giant",
    "data": {
        "name": "Three-Headed Giant",
        "tags": [
            "custom",
            "for-fun"
        ],
        "cards": {
            "banned": [],
            "restricted": [],
            "whitelisted": [],
            "has_commander": true,
            "allow_sideboards": false,
            "max_library_size": 100,
            "min_library_size": 100,
            "number_of_copies": 4,
            "total_power_level": null,
            "enforce_color_identity": true
        },
        "points": {
            "win": 3,
            "draw": 2,
            "loss": 1
        },
        "rounds": {
            "best_of": 1,
            "duration": 3300,
            "matchmaking_style": "swiss"
        },
        "players": {
            "team_size": 3,
            "default_number_per_round": 6
        },
        "starting_life_total": 40
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="https://api.mtgbracket.com" path="/users/:user\_id/rulesets/:ruleset\_id" %}
{% api-method-summary %}
Update Ruleset
{% endapi-method-summary %}

{% api-method-description %}
Update a ruleset.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="ruleset\_id" type="integer" required=true %}
Ruleset's unique ID.
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
Successfully updated a custom ruleset.
{% endapi-method-response-example-description %}

```javascript
{
    "id": 7,
    "user_id": 1,
    "name": "Three-Headed Giant",
    "data": {
        "name": "Three-Headed Giant",
        "tags": [
            "custom",
            "for-fun"
        ],
        "cards": {
            "banned": [
                {
                    "id": "n:Sen Triplets"
                }
            ],
            "restricted": [],
            "whitelisted": [],
            "has_commander": true,
            "allow_sideboards": false,
            "max_library_size": 100,
            "min_library_size": 100,
            "number_of_copies": 4,
            "total_power_level": null,
            "enforce_color_identity": true
        },
        "points": {
            "win": 3,
            "draw": 2,
            "loss": 1
        },
        "rounds": {
            "best_of": 1,
            "duration": 3300,
            "matchmaking_style": "swiss"
        },
        "players": {
            "team_size": 3,
            "default_number_per_round": 6
        },
        "starting_life_total": 40
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="delete" host="" path="/users/:user\_id/rulesets/:ruleset\_id" %}
{% api-method-summary %}
Delete Ruleset
{% endapi-method-summary %}

{% api-method-description %}
Delete a ruleset.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="user\_id" type="integer" required=true %}
User's unique ID.
{% endapi-method-parameter %}

{% api-method-parameter name="ruleset\_id" type="integer" required=true %}
Ruleset's unique ID.
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

