Plug-in Presets for Notion
==========================

A plug-in preset is a folder with these items:

* A file named `Preset.xml`
* A folder named `Instruments`
* In the Instruments folder, a Notion file for each instrument


Preset.xml
----------

This is a minimal definition for a presets XML file. Use your own reverse domain name to keep your preset identifier unique, but you can structure the identifier as you like. 

    <preset>
        <identifier>com.mydomain.pluginmaker.plugin.v1</identifier>
        <name>Preset Name Here</name>
    </preset>


An instruments file
-------------------

Each Notion file in the Instruments folder defines one instrument, which will then come up as an instrument in your preset.

Each file should have:

* One part with a plug-in instrument
* One rules definition in `Use Rules`

The part will be used as a template when adding this instrument to the score, so things like the staff name, abbreviation, and staff type will be copied when you add this instrument into your score.

You can put music and tests of various expressions in this file. This is useful and recommended. 


User-defined expressions
------------------------

Many sound libraries have sounds that don't have a standard technique name in notation. Use can have your preset access these with a preset expression, or user technique.

In the preset definition, keep the number unique. This number will be used to match an expression you've entered in the score and the rule you make for it.

    <preset>
        <identifier>com.mydomain.pluginmaker.plugin.v1</identifier>
        <name>Preset Name Here</name>
        <user-techniques>
            <technique number=1>Octaves</technique>
            <technique number=2>Rips</technique>
        </user-techniques>
    </preset>



Preset locations
----------------

On macOS, Notion will look for presets here:

* `/Users/<user>/Documents/Notion 6/Presets`
* `/Library/Application Support/Notion Music/Notion 6/Presets`

On Windows, Notion looks here:

* `C:\Users\<users>\Documents\Notion 6\Presets`
* `C:\Program Files\Notion 6\Presets` (or where you have installed Notion)

The location will change with the app's major version, so Notion 7 will have presets in its own folder.





