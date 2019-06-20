# MirrorModRemoteConfiguredMods
This is the public mirror of a configuration file in the Mirror Mod, read from to load part's mirrored rotation configurations for foreign mods. If you want your mod to be automatically compatible with the mirror mod, first create a mirror configuration [as shown in this video](https://youtu.be/5VuLQEuy1BI?t=504). Then create files from the logged configurations, place them somewhere in your mod's folder and note the paths of those files inside your new json, which should be added here in config.json.

## Creating an entry in config.json to add your mod

--> youtube link to be added

## Example

For each of your mods you want to add compatibility for, add a new JSON object containing the keys "localId", "partDefinitionPaths" and "mirrorDefinitionPaths" like so:

```js
        {
            // <YOUR MOD NAME HERE>
            // <YOUR MOD'S WORKSHOP LINK>
            "localId": "11111111-1111-1111-1111-111111111111",  // Your mod's localId, found in the description.json of your mod
            "partDefinitionPaths": [  // An array containing all the paths to the part definition files.
                "Objects/Database/ShapeSets/parts.json",
                "Objects/Database/ShapeSets/otherparts.json",
                "Objects/Database/ShapeSets/parts.json"
            ],
            "mirrorDefinitionPaths": [ // An array containing the paths to the json files defining the mirror rotations for your parts
                "Objects/Database/ShapeSets/mirrored/mirror.json"
            ]
        }
```

#### Be sure to include your mod's name, workshop page and correctly add commas.
#### Pull requests creating invalid JSON or not being up to spec will not be accepted until fixed.

## Q & A:

### Why do you need the paths to the json files defining my parts?
In order to prevent mod A from overwriting the mirrored rotations for a part from mod B, the mirror mod will need access to the part UUIDs of mod A. Thus, if mod A defines mirrored rotations for part UUIDs which it itself does not define, this is considered an illegal configuration.

### Why would I create multiple paths for the mirror definitions? The Mirror Mod only spits out one json when configuring mirror rotations.
Just like the game allows multiple part definition files, the Mirror Mod does too. This allows organizing parts into seperate files.
