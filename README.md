# SKamera
A highly customizable Camera Path System written in Skript.
Can be used to create camera paths for cutscenes cinematic showcases and much more


## Using the System

### Requirenments
The Plugin [Skript](https://github.com/SkriptLang/Skript) itself

This System requires the following Skript Addons to run properly
 - [skript-yaml](https://github.com/Sashie/skript-yaml)
 - SkBee
 - [PoaSK](https://github.com/Ekpoa/PoaSkRewritev2)
 - [skript-particles](https://github.com/sovdeeth/skript-particle) Can be optinally used to render particle lines async

It also requires the Modules ClientDisplays and Debugging (specifically positondebug.sk) from my [skript Libraries](https://github.com/Dragoncraft000/skript-libraries) Collection

## Installation
1. Download all required Addons
2. Download the skript-libraries Modules and place them inside you scripts folder
3. Download the latest release or clone the repository
4. Copy the SKamera folder into your Server scripts folder
5. Restart your server or run `/sk relaod SKamera/`

## Configuration
Before you start to use the system I recommend changing some variables to fit your server

By Default Skamera tries to read a prefix from a global Prefix variable called {prefix}, this allows the system to easily use the same prefix as other skript-based systems while only having to set one value.
If you don't have a default prefix or your variable has a different name you can uncomment Line 8 in `Player/camerapaths.sk` and change the string to your desired prefix

Line 6 and 7 in `Player/camerapaths.sk` contain the strings used to display the Intro Fade and Cinemascope Bars. You will need to change these values to your own unicode Characters from you resource pack if you want to use the features.

The default path all camera path files will be stored in is `/plugins/SKamera/camera_paths`.
You can change that value in `Player/dataloader.sk`.

## First Camera Path

Create a New Cutscene by running
```
/camerapath create <id>
```
This will automatically select the path in editor Mode.
Fly to the first location you want to set and run
```
/point add
```
to add a new point to the path at your current location. Each path requires at least to points but you can create as many as you like.

To view your newly created camera path right click with the red play button in you hotbar

To exit the editor mode run
```
/camerapath cancel
```
all changes are automatically saved


## Todo

- [ ] Add Translations for all messages
- [ ] Finish Documentation
- [ ] Set up Permissions for all actions
- [ ] Expose the generated spline to allow usage within other systems

## Reporting Bugs or Requesting Features
To report a bug or request a specific feature either create an issue or contact me on the SkUnity Discord Server

## License
Licensed under the MIT License. See LICENSE.txt for more information.