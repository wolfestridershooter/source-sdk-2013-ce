# Forked from Source SDK 2013 Community Edition
(https://github.com/Nbc66/source-sdk-2013-ce)

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


# New commands
-nodefaultcubemap: Don't generate a default cubemap. <-----(This fixes not being able to build cubemaps on some PCs)

-allowdynamicpropsasstatic: Allow all models with the 'static' flag in the model viewer to be used on prop_static, even when their propdata doesn't contain 'allowstatic'

-noblocks       : Do not chop the level into blocks.

-nohiddenmaps   : Exclude manifest maps if they are currently hidden.

-defaultproppermodelsstatic: All propper_models will be inserted into the BSP
as static props by default, unless InsertAsStaticProp equals 1.

-strippropperentities: Removes all entities with propper_ in their classname.
This is to avoid a bunch of Propper entities attempting to spawn in-game despite them being internal entities.

# Requirements
To be able to use Source 2013 CE you will need to download **Visual Studio 2022** and install:
* MSVC v143 - VS 2022 C++ x64/x86 build tools
* C++ MFC Library for latest v143 build tools (x86 and x64)
* Windows 11 SDK (10.0.22000.0)

As of July 2023, CE has been tested on Visual Studio 2022 with the latest versions of the requirements listed above. So if desired you can use that instead.

# Contributing
I'd appreciate any form of help so ideally if you want to help this project out the best way would be to make a pull request.

# Credits in order of their implimentation
<p>The insperation for this fork: https://github.com/wouterpleizier/source-sdk-2013<br>
A small fix for detail props (Look at the bottom of the commit, THE-HAVOK's comment): https://github.com/ValveSoftware/source-sdk-2013/commit/fd3c17eff24be4c5d66d9fd4fe2e1fb90101f77a</p>

<p>Disable skyboxed cubemap, staticprops for on any model, support for func_detail_blocker, and increased compile general limits: https://github.com/wouterpleizier/source-sdk-2013<br>
https://github.com/Nbc66/source-sdk-2013-ce/commit/e70875d0d85e91cff7965416e64d65cbb8dce9f8</p>

<p>False debug counter fix: ValveSoftware/source-sdk-2013#436<br>
Commit: https://github.com/Nbc66/source-sdk-2013-ce/commit/1c3f381ed304637d9377931d19e665305ce17201</p>

<p>VDC increase thread pool for compilers https://developer.valvesoftware.com/wiki/Increased_Thread_Limit_for_Compile_Tools<br>
Commit: https://github.com/Nbc66/source-sdk-2013-ce/commit/dc01ad40f94e961497493594634a1cf9419508fb</p>

<p>Custom shader vbsp fix: ValveSoftware/source-sdk-2013#200<br>
Commit: https://github.com/Nbc66/source-sdk-2013-ce/commit/474eda071dbdc6ffe0ffb48b17bca9a944e4eda4</p>

<p>func_detail smoothing group fix: ValveSoftware/source-sdk-2013#391<br>
Commit: https://github.com/Nbc66/source-sdk-2013-ce/commit/70941050b51341110650e2f9c46683af6ff604f8</p>

<p>VBSP features for Propper: mapbase-source/source-sdk-2013#143<br>
Commit: https://github.com/Nbc66/source-sdk-2013-ce/commit/ba1c1d585391045f64ed1b77818b7ffec110c5f3</p>

<p>A bunch of miscellaneous vbsp fixes: https://github.com/DeathByNukes/source-sdk-2013<br>
Commit: https://github.com/Nbc66/source-sdk-2013-ce/commit/b5863641c093368c6d1c91b12f314936af6eebae</p>