# Source SDK 2013 Extended Compilers
Forked from Source SDK 2013 Community Edition: https://github.com/Nbc66/source-sdk-2013-ce

# Info
This is a fork of Source 2013 CE with the goal of fixing up Source 2013's compile tools with miscellaneous fixes and performance improvments to make map makers' lives easier.

# Beware!
These compilers are still in devlopment, if you push the limits of even these compilers you'll probably run into crashes and other bugs I'm not aware of.
Although so far for the most part they seem pretty stable so far to me.

# Disclaimer
These are the singleplayer version of the compilers, you should still be able to compile mutiplayer maps although I did just want to let you know.
With that out of the way lets get onto the features!

# Features
Far increased compile limits. (sometimes doubled or quadrupled!)
New commands. (See the new commands section)
Some optimizations that can in some cases more than half your compile times.
Propper prop_static intergration.
Support for func_detail_blocker.
Vanilla lighting unlike Slammin's VRAD which is slightly different with the same settings and can mess up lighting on func_brushs.
Large address aware, allowing for more memory usage on 64-bit systems.

# New limits
Vanilla VBSP: https://github.com/wolfestridershooter/source-sdk-2013-ce/blob/master/vanilla_vbsp_limits.txt
Extended VBSP: https://github.com/wolfestridershooter/source-sdk-2013-ce/blob/master/extended_vbsp_limits.txt

# New commands
-nodefaultcubemap: Don't generate a default cubemap. <-(This fixes not being able to build cubemaps on some PCs)

-allowdynamicpropsasstatic: Allow all models with the 'static' flag in the model viewer to be used on prop_static, even when their propdata doesn't contain 'allowstatic'

-noblocks       : Do not chop the level into blocks.

-nohiddenmaps   : Exclude manifest maps if they are currently hidden.

-defaultproppermodelsstatic: All propper_models will be inserted into the BSP
as static props by default, unless InsertAsStaticProp equals 1.

-strippropperentities: Removes all entities with propper_ in their classname.
This is to avoid a bunch of Propper entities attempting to spawn in-game despite them being internal entities.

# Requirements
Since this is a fork of Source 2013 CE you'll need the same tools and **Visual Studio 2022** to compile:
* MSVC v143 - VS 2022 C++ x64/x86 build tools
* C++ MFC Library for latest v143 build tools (x86 and x64)
* Windows 11 SDK (10.0.22000.0)

As of July 2023, CE has been tested on Visual Studio 2022 with the latest versions of the requirements listed above. So if desired you can use that instead.

# Contributing
I'd appreciate any form of help so ideally if you want to help this project out the best way would be to make a pull request.