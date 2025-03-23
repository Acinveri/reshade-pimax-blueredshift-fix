
This repository contains a chromatic aberration shader that helps fix the "RedBlue shift" experienced
on Varjo HMDs (Aero, XR-3, VR-3) and Pimax Crystal. Not compatible with Quad Views.

To get ReShade visit https://reshade.me

Installation using the ReShade Setup Tool (easy)
------------------------------------------------
If you have Reshade already installed for the game, just copy PimaxBlueShiftFix.fx to the Shaders folder. Alternatively:

1. Select the game or application you want to use ReShade on
2. select the appropriate rendering API (DX9,DX10/11/12,OpenGL,Vulkan) if ReShade asks for it. You can look at the 
[PcGamingWiki](https://www.pcgamingwiki.com/) in the section "API" if you're unsure which rendering API to choose
3. add this link `https://github.com/Acinveri/reshade-pimax-blueredshift-fix/archive/main.zip` in the installer when it asks you which effect packages to install
4. select the newly added repository
5. start your game and enable the technique in ReShade. See section "Usage" or "Quickstart" for further details

Installation (manual)
---------------------

1. [Download](https://github.com/Acinveri/reshade-pimax-blueredshift-fix/archive/main.zip) this repository
2. Extract the downloaded archive file somewhere
3. Start your game, open the ReShade in-game menu and switch to the "Settings" tab
4. Add the path to the extracted [Shaders](/Shaders) folder to "Effect Search Paths"
6. Switch back to the "Home" tab and click on "Reload" to load the shaders

Usage
-----

1. enable the `ZZZ_PimaxBlueShiftFix` technique in ReShade 
2. make sure the `ZZZ_PimaxBlueShiftFix` technique is **last** in the list
3. main parameters to adjust are `Red Offset` and `Blue Offset`. `Correction Origin X` and `Correction Origin Y` should be constants for a given headset, but since I don't know their exact values you can play with them too.  


Credits
-------
Largly based on https://github.com/bernhardberger/reshade-varjo-redshift-fix shader for Varjo Aero by Bernhard Berger
Special thanks to Matthieu Bucchianeri ([mbucchia](https://github.com/mbucchia)) for writing the initial HLSL pixel shader for his awesome [OpenXR-Toolkit](https://mbucchia.github.io/OpenXR-Toolkit/) project!
