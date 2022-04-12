---
title: Wrench Editor
description: Wrench is a level editor and viewer for the PS2 Ratchet & Clank games working from Ratchet & Clank 1 to Ratchet & Clank: Deadlocked.
published: true
date: 2022-04-12T09:40:59.636Z
tags: level editor, modding
editor: markdown
dateCreated: 2022-03-05T15:43:32.492Z
---

# [Wrench Editor](https://github.com/chaoticgd/wrench/)
Wrench is a set of modding tools for the Ratchet & Clank PS2 games, created by **chaoticgd**.

![Wrench Editor](https://github.com/chaoticgd/wrench/raw/master/docs/screenshots/editor.png)

Features currently include:
- WAD Utility
  - Pack/unpack levels.
  - Export moby meshes as COLLADA files.
  - Import/export instances/entities as JSON.
  - Import/export textures as PNG files.
  - Import/export collision meshes as COLLADA files.
  - Import/export everything else as binary files.
- Level Editor
  - View unpacked levels.
  - Move objects and modify their properties.
- ISO Utility
  - Extract files from R&C1, R&C2, R&C3 and Deadlocked.
  - Build modded ISO files for R&C2, R&C3 and Deadlocked.

# Installation
Installing wrench is sometime a bit difficult, including all Visual Studio versions and complementary plugin software, people who don't already use Visual Studio are of course a bit lost.

**N.B: This software is only buildable on Windows yet.**

## First step
Install [Visual Studio](https://visualstudio.microsoft.com/downloads/) 2017, 2019 or 2022 _**Community Edition**_.

[![Visual Studio](https://cdn.discordapp.com/attachments/452456855743102976/963135980192292894/visual_studio.png)](https://visualstudio.microsoft.com/downloads/)

## Second step
Install [CMake](https://cmake.org/download/) in any recent version you want, installer or zip archive. To unzip archives you will need [7-Zip](https://www.7-zip.org/download.html "https://www.7-zip.org/download.html") (any version) 

[![cmake.png](/cmake.png "Download the version you need or you want. Format too.")](https://cmake.org/download/)

## Third step
### Less recommended
On the main screen of the Visual Studio installer, install a new Visual Studio version (2017 or later), and then check the "**C++ Desktop Dev**" check box. This is a kit for Desktop Apps development in **C++**. You should also **click on ".NET Desktop Dev"** if you downloaded the classic version with the button "**Visual Studio 2022**", it's a devkit for **C#** and **F#** apps, even if **wrench** is a **C++** program, the other modding tools are globally made in **C#** too.
When the download is done, launch the version and check if CMake is installed into the Visual Studio console. If not, try to reinstall CMake.
## Fourth step
Clone or download [Wrench Editor](https://github.com/chaoticgd/wrench/) on GitHub. Put it in a folder where you'll easily find it again.

[![github_clone.png](/github_clone.png "Go on the Chaoticgd's repo")](https://github.com/chaoticgd/wrench/)

- You can take one of these solution:
  1) This is to clone the repo and stay updated (you will have to rebuild each new version). It works with **[GitHub Desktop](https://desktop.github.com/ "https://desktop.github.com/")**
  2) This is to clone the repo and stay update BUT will open directly **Visual Studio** instead of **GitHub Desktop**.
  3) This will just give you a copy of the current version of the repo. **We will take this button for example here**. Of course, it's a zip, so you'll unzip it with **[7-Zip](https://www.7-zip.org/download.html "https://www.7-zip.org/download.html")**.

### HEAVILY RECOMMENDED
Go into a folder, **right click**>**open terminal here** and execute `git clone https://github.com/chaoticgd/wrench.git --recursive`.
If it don't works, verify that **[Git](https://git-scm.com/ "https://git-scm.com/")** is installed on your computer. If not, download and install it.
`--recursive` command clone also the dependencies, and in this it's essential if you don't get them by using the "**Download ZIP**" button.
The cloning can take a while.
While cloning, it should look like this. If it's not so long or it don't load, retry or/and verify the case and if you put `--recursive` at the end.

![git_cloning.png](/git_cloning.png)

## Fifth step
When it's cloned or copied, open **Visual Studio** and click **Open a local folder**, then navigate to the **wrench-master** folder you just unzipped and when you're in, just click **Open**.
Now open a terminal by clicking on the top-corner third button **Display**>**Terminal**
A inbox window should appear below the text editor.

## Sixth step
Building: Into the newly created terminal, execute the command `cmake .`, it will generate all the **CMake** files project.
Now, a `wrench.sln` **Visual Studio solution** should appear. just click it, it will re-open the current **Visual Studio window**.

### Building using command lines
Into the folder, execute the command **`cmake --build . --config BUILD_TYPE`**; **Important**, replace `BUILD_TYPE` with one of the following options:
- `Debug` : very slow - not recommended
- `Release` : no symbols - not recommended
- ⭐ `RelWithDebInfo` : release but has symbols - recommended
- `MinSizeRel` : release but minimal size (?) - not recommended (?)

### Building using Visual Studio generator
On the **Visual Studio** page - If you didn't opened the `wrench.sln` file, then do it - **right click** on **wrench** into the **Solution Explorer** and click **Set as Startup Project**.
> You should now be able to build and debug wrench using the toolbar controls and all Visual Studio features.
\- chaoticgd
>
Then, click the **Generate button**. Of course, as said higher, you can select multiple build versions. **chaoticgd** recommend using the `RelWithDebInfo` build method, so you should do so.

For more informations, go to the **[original GitHub Project page](https://github.com/chaoticgd/wrench/)**, and if you have questions or want to report errors, go to the **[issues page](https://github.com/chaoticgd/wrench/issues)**.