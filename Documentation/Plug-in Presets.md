Creating Presets for Notion
==========================
A preset is a file that maps Notion's written articulations and expressions to 3rd party VST instruments (or plug-ins). For a couple of examples, look in the [Demos folder](/Demos).

A preset is a folder with these items:

* A file named `Preset.xml`
* A folder named `Instruments`
* Within the Instruments folder, you can optionally have one level of sub-folders for an instrument family (e.g. Brass / Wind / Strings)
* In the Instruments folder (or optional sub-folder), a Notion file for each instrument - each Notion file contains an attached ruleset.

![Preset folder](/Documentation/Screenshots/preset_folder_setup.png?raw=true "Presets Folder")


Preset.xml
----------
This is a minimal definition for a presets XML file. You can structure the identifier as you like, or for example use your own reverse domain name to make sure it is unique. 

    <preset>
        <identifier>com.mydomain.pluginmaker.plugin.v1</identifier>
        <name>Preset Name Here</name>
    </preset>


An instruments file
-------------------
Each Notion file in the Instruments folder defines one instrument, which will then come up as an instrument in your preset.

Each file should have:

* Exactly one part with a plug-in instrument
* Exactly one rules definition in `Tools>Use Rules...`

You can put music and tests of various expressions in this file. This is useful and recommended.

![Notion file with Rule](/Documentation/Screenshots/rules_editor.png?raw=true "Notion file with Rule" )
*This image shows the Notion Rules Editor containing the VSL Cello rule, the VSL plug-in interface and a Notion score containing some test notes and articulations with the VSL Cello Rule attached to the staff*

The part will be used as a template when adding this instrument to the score. When you add this instrument into your score, Staff name and abbreviation, clef, transposition and staff type will be copied from the template into the added part of your score.

By default, the order of these instruments when shown in Score Setup, will be alphabetical. But you can customise the order, by adding a number to the front of the Notion file. e.g. "01 Violin.notion", "02 Viola.notion" etc. The number itself will not be shown in Score Setup.


Preset Expressions
------------------------
Many sound libraries have sounds that don't have a standard technique name in notation. You can have your preset access these with a preset expression, or user technique.

In the preset definition, keep the number unique. This number will be used to match an expression you've entered in the score and the rule you make for it.

    <preset>
        <identifier>com.mydomain.pluginmaker.plugin.v1</identifier>
        <name>Preset Name Here</name>
        <user-techniques>
            <technique number="1">Octaves</technique>
            <technique number="2">Rips</technique>
        </user-techniques>
    </preset>

Once you've created the expression in the XML and the corresponding rule in the Notion file, you can use it. Click the Techniques box in the Palette, then the arrow. This will show 'User' in the cursor. Place it where you wish in the score - Notion will then give you the list of expressions that you created.

![Preset Expressions](/Documentation/Screenshots/preset_expression.png?raw=true "Preset Expressions")


Using the Rules Editor
----------------------
The Rules Editor is built into Notion and can be used to edit the rules that define the mapping between articulations and techniques in the score and the control events sent to the player of the sample library. It can be opened when creating a new or editing an existing rule set in `Tools>Use Rules...`

All rules where all rule conditions are fulfilled are executed and the defined acions of these rules are performed. A rule will only be executed if all its conditions are true but for one note multiple rules can be executed if their conditions are fulfilled.

For a detailed description on how to use the Rules Editor see the [Notion User Guide](/Documentation/Notion%206.3%20User%20Guide.pdf) page 9.13 and for a list of all available techniques and expressions in the Rules Editor, see the Appendix on page 16.5.


Making the preset available on GitHub
-------------------------------------
For information on how to make self created presets available, see the [GitHub readme](/Documentation/Using%20GitHub.md).
