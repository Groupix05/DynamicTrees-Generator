# DynamicTrees-Generator
An app to help creates dynamicTrees addons

## Source-Code
For now there is no source code because the code is a nightmare

## Current issues
I didnt have time to fix some issues:
- saving settings in the project editor is broken

## How to use
When launching the generator you have this:
![MainPage](https://github.com/Groupix05/DynamicTrees-Generator/blob/main/images/MainPage.png)

You can open a project with "Browse" or create a new one with all of the parameters below.
So first, choose a name for your project, if you dont want "DynamicTrees-" in front of your project's name, tick "Custom name"
Then choose a Minecraft version (1.12.2 and 1.21.1 fabric is not yet supported)
You can tick connector if you want to create an addon for a fabric mod.
You can select a custom directory where you want it to be saved, by default it will create your project in "Documents/DynamicTreesGenerator"
You need to edit things in more settings before creating your project :

![settings](https://github.com/Groupix05/DynamicTrees-Generator/blob/main/images/Settings.png)

Modid and group are required before creating a project, every other settings are optional.
If you dont know modding, the modid is the project identity, it needs to be different for every minecraft mods. And the group is often who made the mod, I dont really know myself...
Forge Version, DT Version and DT+ Version should be set up automaticly when you choose a mc version. If the mod you use requires a higher version of those mods, you can edit here.

Once created, you have a new page :
![Editor](https://github.com/Groupix05/DynamicTrees-Generator/blob/main/images/Editor.png)

In this view, there is a lot of unfinished buttons, only the buttons on the top works for now.
- "runClient" : runs the game in a dev environment
- "runData" : Generates the required data for your addon (like loot table, tags, and blockstates)(add "--existing-mod", "[modid]" before doing runData, the modid here is the mod you want to create an addon for, you can add multiple of these lines if you want to create an addon for multiple mods. DONT FORGET THE COMMA IF YOU ADD THOSE LINES)
- "build" : builds your project, the .jar can be found in build/libs/
- Settings : if you want to edit some parameters of your project, but saving is broken for now.


Once created, you can open build.gradle.kts and add your mods :
replace //implementation(fg.deobf("curse.maven:template-projectid:fileid")) with your mods :
check those on curseforge : 
- template=name of the mod (can be anything)
- projectid= the id of the project
- fileid= the id of the file
check here for more help : https://www.cursemaven.com
Dont forget the libs of your mods !!!

Dont forget to add your mods in the mods.toml inside the resource folder (src/main/resources/META-INF) 


