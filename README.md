# MirrorModRemoteConfiguredMods
mirror rotation configurations for other mods

## How to create a new mirror rotation configuration for the parts of your mod? 

--> youtube link to be added
### Steps:

--> TODO

## How to make sure the mirror mod supports your mod?

just edit the config.json to include your mod.
example:
```json
{
    "mods":[
        {
            //already existing mod in the config
            //https://steamcommunity.com/sharedfiles/filedetails/?id=someID
            "localId":"11111111-1111-1111-1111-111111111111",
            "partDefinitionPaths":[
                "Objects/Database/ShapeSets/parts.json"
            ],
            "mirrorDefinitionPaths":[
                "Objects/Database/ShapeSets/mirrored/mirror.json"
            ]
        }
		,
        {
            //YOUR MOD NAME HERE
            //https://steamcommunity.com/sharedfiles/filedetails/?id=workshoplink
            "localId":"11111111-1111-1111-1111-111111111111",  // your mod localId, you can find this in the description.json of your mod
            "partDefinitionPaths":[  // this is an array containing all the paths to the json files defining your parts
                "Objects/Database/ShapeSets/parts.json",
                "Objects/Database/ShapeSets/otherparts.json",
                "Objects/Database/ShapeSets/parts.json"
            ],
            "mirrorDefinitionPaths":[ // this is an array containing the paths to the json files containing the mirror rotation definitions for your parts.
                "Objects/Database/ShapeSets/mirrored/mirror.json"
            ]
        }
		
    ]
}
```

## Q&A:

### Why can you not generate an algorithm?

### Why do you need the paths to the json files defining my parts?

### Why would i create multiple paths for the mirror definitions? The Mirror Mod only spits out one json when configuring mirror rotations.