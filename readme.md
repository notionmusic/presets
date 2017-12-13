# Welcome to Notion's Community Presets

This space allows you to download, edit, upload and share presets for Notion. A preset is something that maps Notion's written articulations and expressions, to 3rd party VST instruments (or plug-ins).

Getting started
=================
To get started, download the repository as described in the [GitHub readme](Documentation/Using%20GitHub.md).

After you have downloaded the repository, copy the preset folders you want to use from `presets/Libraries/<Vendor name>` to one of the following locations:

Preset locations
----------------
You can save the folder in one of two possible locations (depending on how you wish to organise yourself):

On macOS, Notion will look for presets here:

* `/Users/<user>/Documents/Notion/Presets` (you will need to create this folder if it does not already exist)
* `/Library/Application Support/Notion Music/Notion 6/Presets`

On Windows, Notion looks here:

* `C:\Users\<users>\Documents\Notion\Presets`(you will need to create this folder if it does not already exist)
* `C:\Program Files\Notion 6\Presets` (or where you have installed Notion)

The location of the second of each locations above will change with the app's major version, so Notion 7 will have presets in its own folder.


Using the presets
-----------------
On launching, Notion will check the two preset locations above, and add any Presets it finds to Score Setup. 
Look under VST Presets>Your Preset Name in Score Setup.

Select the instrument, and Notion will add it to the score.
![Score Setup](/Documentation/Screenshots/vst_preset_scoresetup.png?raw=true "Score Setup")


Creating and uploading presets
------------------------------
If there is no preset for the sample library you want to use, be invited to create your own and make it available online so that others can use and improve it.

Documentation on how to create presets can be found in the [Preset readme](Documentation/Plug-in%20Presets.md).
If you have created your own preset folder and don't know how to make it available on GitHub, see the [GitHub readme](Documentation/Using%20GitHub.md).

Further reading
---------------
For help creating rulesets, and for anything else, see the main [Notion User Guide](Documentation/Notion%206.3%20User%20Guide.pdf) (or from within Notion itself, from Help>User Guide)
   - For Presets see page 9.10
   - For Preset Expressions, see page 9.11
   - For Creating Rules see page 9.13
   - For list of all available techniques and expressions in the Rules Editor, see the Appendix on page 16.5
