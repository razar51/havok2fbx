Havok 2 FBX Converter 0.1b
=============================

Utility to convert Havok 2014-1-0 x32 files to FBX 2014.2.1

Updated to not assume one-to-one 'animation track'-to-bone mapping. Certain havok files will have animations where the number of bones in the 
skeleton does not equal the number of bones in the animation (for example, FFXIV animations extracted with ffxiv_explorer). 
There is a mapping/binding in the file that specifies which bone each track is affecting.

This tool has been updated to honor that binding and now should properly match each animation track with the proper bone in the skeleton.

Support
---------------------
- x32 .hkt / .hkx / .xml animation/skeleton

Setup
---------------------
Required Libraries/Applications:
- Havok SDK 2014-1-0
- FBX SDK 2014.2.1
- Visual Studio 2012 for Platform Toolset V110

Required Environment Variables for installed libraries:
- HAVOK_SDK_ROOT
- FBX_SDK_ROOT

Compiling
---------------------
- 1.) Open solution file and make sure all libaries are installed
- 2.) Compile as Debug or Release
- 3.) Copy release/debug libfbxsdk.dll from FBX SDK to application directory

Usage
---------------------
- Files to be converted must be on Version 2014-1-0 x32!
- Verfiy using Havok Content Tools before trying to convert

- Run havok2fbx.exe -hk_skeleton PATH -hk_anim PATH -fbx PATH
	- hk_skeleton 	= The skeleton base to use
	- hk_anim		= Animation to load with the skeleton ( optional )
	- fbx			= path and filename for exported fbx, uses input filename if not specified ( optional )

Credits
---------------------
- Autodesk, Inc. ( FBX SDK )
- Havok.com Inc. ( HAVOK Public SDK x32 )
- Ken Shoemake ( Euler/Quat Code Snippet )
- Figment ( Animation loading code idea/snippet from hkxcmd )
- Highflex ( Creator of havok2fbx tool )

Licensing
---------------------
- Check LICENSE.txt