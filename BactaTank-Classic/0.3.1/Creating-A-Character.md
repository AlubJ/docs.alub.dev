# Creating a Custom Character
After [installing BactaTank Classic](README?id=installation), the obvious next step is to create a character.

?> Character editing and creation varies in difficulty, depending on your goal. This tutorial will cover the most basic of character creation, more complex characters may require looking into some of the other docs, unless already given a tutorial.

?> Sometimes, when stating directories, the tutorial uses `~`. This represents your game's folder.

## Compatible Games

This table outlines which games are compatible with BactaTank Classic. It includes "classic" era LEGO games developed by TtGames/Traveller's Tales, as well as some of their other games based on similar revisions of the engine.

| Game                                        | Can be loaded | Can be edited |
| ------------------------------------------- | ------------- | ------------- |
| LEGO Star Wars: The Videogame               |      ❌       |      ❌       |
| LEGO Star Wars II: The Original Trilogy     |      ❌       |      ❌       | 
| Bionicle Heroes                             |      ❌       |      ❌       | 
| LEGO Star Wars: The Complete Saga           |      ✅       |      ✅       |               
| LEGO Batman: The Videogame                  |      ✅       |      ✅       | 
| LEGO Indiana Jones: The Original Adventures |      ✅       |      ✅       | 
| Transformers: The Videogame                 |      ⚠️       |      ❌       | 
| The Chronicles of Narnia: Prince Caspian    |      ⚠️       |      ❌       |

!> Transformers and Narnia models can be loaded for viewing, however this functionality is extremely experimental and can result in crashing. These are only supported for viewing. (Transformers model versions need to be enabled for loading in the preferences).

## Setting Up The Character Folder

?> This step can be skipped if you want your character to be in another character's folder (mainly used for characters sharing animations).

To start creating a character, you need to create your character's folder. The character's folder holds most of the character's files and data. To start, locate the `CHARS` folder in your game's root directory (the directory that shows up when clicking the game folder).

![image](https://github.com/user-attachments/assets/40abdce6-8fe0-4446-a6a5-a1fd638c57ef)

Then create a folder, naming it whatever you'd like (Preferrably the character's name in all caps, but you can also just make it something you can remember). This is where all the character's files will be.

![image](https://github.com/user-attachments/assets/fe7e2a4e-1b66-44b7-ad2e-a0a642d7287c)

## Finding a Base

Once the character's folder is setup, you'll need to find a character to copy as a starting point, or a base. Questions to consider when finding a base for a character are:
- Are there enough texture/mesh slots?
- Do they work with the animations I want?
- Do they have a face structure similar to that of the character I want?
- Do they have similar abilities to the character I want? (doesn't matter, makes txt setup easier though)

?> You may not always be able to find a good base easily, and that's okay. Some of the questions to consider can be a bit confusing for beginners. You can always ask the [TtGames Modding Discord Server](https://discord.gg/ttgames-lego-modding-539431629718945793).

Once you find a good character as a base, copy their `*_PC.GHG` and `*.TXT` files over (optionally copy `*_LR_PC.GHG` if you want to make a lo-res model). You can find character's files in their character folder. In this tutorial, I will be using "Riddler Goon" from LEGO Batman: The Videogame as a base, to make a new goon variant, Generic Goon (How creative).

![image](https://github.com/user-attachments/assets/4892cd91-b917-4104-a8d7-9cafcfc90590)

Next, paste their files in your character's folder and rename them to your character's name.

![image](https://github.com/user-attachments/assets/c7707e98-9053-4068-9069-d630edb467e2)

?> When renaming the `*_PC.GHG` or `*_LR_PC.GHG` file, keep the `_PC` or `_LR_PC` accordingly.

Once renamed, open the character's `*_PC.GHG` file in BactaTank Classic by using `CTRL+O` in BactaTank Classic, dragging and dropping onto the window, or using `Open With...` when right-clicking the file. Continue to the next section.

## Editing Textures
Once the character is open in BactaTank Classic, it should looks something like this (what you see will vary depending on the model used).

![image](https://github.com/user-attachments/assets/b213e9b5-9b60-4564-bf67-db0c615b0bd8)

On the left side of the window, there are multiple dropdown buttons labeled `Textures`, `Materials`, etc. Click `Textures`. It should look something like this (amount of textures vary from character to character).

![image](https://github.com/user-attachments/assets/aa3d2088-3a1b-4243-ae95-802953a3603e)

Click on one of the textures and find the one you want to edit. Clicking on a texture shows a preview on the right-hand side.

![image](https://github.com/user-attachments/assets/ff037065-1431-4522-976e-79df9816b893)

Export the texture using `CTRL+E` or by clicking ![Triple Dot Button](assets/tripleDotButton.png) in the upper-right hand corner and clicking `Export Texture`. Save the texture in any place you'll remember later. Refer to [Editing Textures](Textures) for opening and exporting textures.

![image](https://github.com/user-attachments/assets/dc3fcf59-b58d-422c-857f-a19acf50c41e)

### Exporting UVs
By clicking the tab at the top that says "UV Viewer," you can view how your character's texture(s) is projected across a surface. You can save the current UV map as an image for reference by clicking ![Save Button](assets/saveButton.png) and saving the file where you can remember.

![image](https://github.com/user-attachments/assets/6ebb0d16-b059-44f6-9e3f-ef3451f2dac1)

Once the texture file is saved, you can reimport it using `CTRL+R` or by clicking ![Triple Dot Button](assets/tripleDotButton.png) in the upper-right hand corner and clicking `Replace Texture`. Then select the new texture file. You should see the new texture in place of the old one.

?> Some UVs may be shown below the actual texture. This is due to a way TCS UV maps were programmed. You can fix this by changing the `1.000`, or the Y offset, to `0` at the top of the UV viewer.

Save the model using `CTRL+S` or clicking `File >> Save Model`. You should save it over the model in your character's folder. If you make drastic changes, be sure to keep a backup incase anything goes wrong.

## Editing Meshes
On the left side of the window, there are multiple dropdown buttons labeled `Textures`, `Materials`, etc. Click `Meshes`. It should look something like this (amount of meshes vary from character to character).

![image](https://github.com/user-attachments/assets/b2551a40-b73a-497b-b83b-f0077d2f15b6)

Click on one of the meshes and find the one you want to edit. Clicking on a mesh shows a preview on the right hand side.

![image](https://github.com/user-attachments/assets/0d1c332b-cb83-44c1-8247-e43a0776c26f)

Export the mesh using `CTRL+E` or by clicking ![Triple Dot Button](assets/tripleDotButton.png) in the upper-right hand corner and clicking `Export Mesh`. Save the mesh in any place you'll remember later. 
Refer to [Editing Meshes](Meshes) for opening and exporting meshes.

Once the mesh file is saved, you can reimport it using `CTRL+R` or by clicking ![Triple Dot Button](assets/tripleDotButton.png) in the upper-right hand corner and clicking `Replace Mesh`. Then select the new mesh file. You should see the new mesh in place of the old one.

![image](https://github.com/user-attachments/assets/daa84770-08c8-4189-8fa2-c19050050997)

Save the model using `CTRL+S` or clicking `File >> Save Model`. You should save it over the model in your character's folder. If you make drastic changes, be sure to keep a backup incase anything goes wrong.

## Editing the Text File
Now it's time to edit the character's text file. The text file contains specific traits of the character, like what abilities it has, animations it uses, character display name, icon, weapons, and more.

?> Certain keywords/tags typed into the character text file may not function between games. For example, lightsabers will NOT work in LB1.

Open your character's `*.TXT` file in any text editing app (I'll be using notepad++ for this).

![image](https://github.com/user-attachments/assets/b32463a1-d658-44df-8b9a-fe123568cca7)

### Tag Overview
This will go over a few important tags in the character's text file.
- `icon="icon_*"` - Used to decide what icon the character will have in the roster. Icon files can be found in `~/STUFF/ICONS`.
- `name_id=*` - Used to determine what name is displayed for the character in-game. Name IDs can be found in `~/STUFF/TEXT/<LANG>.txt`, with `<LANG>` being the language name you want to edit.
- `layers_*=*` - Used to determine what layers of the character are shown at certain distances/criteria. Layer numbers can be found by viewing the character with BactaTank Classic.
  - `layers_special` - Always drawn.
  - `layers_high` - Drawn when the camera is close to the character.
  - `layers_medium` - Drawn when the camera is a medium distance from the character.
  - `layers_low` - Drawn when the camera is far from the player.
  - `layers_dead` - Drawn when the character "explodes" or dies.

?> Most generic tags can be found and explained in the [Lego Star Wars: The Complete Saga Modding Resource](https://docs.google.com/document/d/1HyLlJhCfjT6hUY-UU9ACqak4tDqorkk464dm7nuvH74/edit?tab=t.0).

## Adding the Character In Game
Now it's time to make the character show up in game.

### Giving Them a Unique Name
Open `~/STUFF/TEXT/<LANG>.TXT`. This file contains most of the text handled in the game, including character names, prologue text, level titles, etc.

![image](https://github.com/user-attachments/assets/de09a48b-46d3-4317-b1fb-33c836053caf)

When you open it, it should look something like this, varying depending on the game. Each row has a number next to the text. This is the text ID, which is how the game is able to find text entries. Find a number (below 1000) that isn't used. Type the number and then your characters name, like this:

![image](https://github.com/user-attachments/assets/90890b25-a15c-4070-b901-0e5f015dbc2c)

Make sure to include quotes or the character name will not work.

Open your characters `*.TXT` file. Change the number next to `name_id=` to your new entry's id.

![image](https://github.com/user-attachments/assets/aeff8abd-b76f-4ed3-a7e4-7df25f37fd2d)

### Adding Them to the Roster
Open `~/CHARS/CHARS.TXT`. This file handles what characters are loaded into the game.

![image](https://github.com/user-attachments/assets/2fa9044b-d11d-4f91-8d79-af3de494f5d3)

Scroll to the bottom of the file and add your character to the file like this:

![image](https://github.com/user-attachments/assets/c7fc5af7-b10f-4e92-9c54-49ee31756d7e)

Now your character will be loaded in game, but still needs to be added to the character roster.

Open `~/CHARS/COLLECTION.TXT`. This file handles what characters are added to the in game roster.

![image](https://github.com/user-attachments/assets/448cbf47-9a80-4cbc-91bf-06d7ec2c57ca)

Scroll to the bottom and add your character to the file like this:

![image](https://github.com/user-attachments/assets/5819e7ac-2f9a-40ce-b91d-6a0fb5965218)

?> The order of `COLLECTION.TXT` determines the order of the character roster. You can move your character's collection entry to change its position in the roster.

Your character should now show up in game and be playable! Nice!

![20250426125755_1](https://github.com/user-attachments/assets/1360c34c-7626-4266-a3bc-dc42d6804cd6)

?> If your character shows up as a blank slot with a "?" as the name, you may have a file called `CHARSTXT.FPK` that you need to delete. You can find and delete it in `~/CHARS`.

## Conclusion
In this tutorial, you learned the basics of how to create and add a character to a classic LEGO game with BactaTank Classic. You learned how to find bases, edit textures, models, text files, and more. With this knowledge, you can create almost any character you can imagine.
