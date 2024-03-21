
Small datapack to add a advancement for taming all dog variants

--- 

# How to add your own wolf variant to advancement list.

add another entry in `criteria`

```json
"<namespace>:<variant_name>": {
            "trigger": "minecraft:tame_animal",
            "conditions": {
                "entity": [
                    {
                        "condition": "minecraft:entity_properties",
                        "entity": "this",
                        "predicate": {
                            "type_specific": {
                                "type": "minecraft:wolf",
                                "variant": "<namespace>:<variant_name>"
                            }
                        }
                    }
                ]
            }
        }
```

then add 
```json
[
    "minecraft:snowy"
]
```
in `requirements` list in the bottom

You can repeat this for any amount of wolf variants