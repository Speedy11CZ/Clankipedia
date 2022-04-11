---
title: Wrench Editor
description: 
published: true
date: 2022-04-11T18:40:26.182Z
tags: 
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
On the main screen of the Visual Studio installer, install a new Visual Studio version (2017 or later), and then check the "**.NET DEKSTOP Dev**" check box. This is a kit for Desktop Apps development in **C#** (CSharp) and **F#** (FSharp) *(and also Visual Basic/VB)*.
When the download is done, launch the version and check if CMake is installed into the Visual Studio console. If not, try to reinstall CMake.
## Fourth step
Clone or download [Wrench Editor](https://github.com/chaoticgd/wrench/) on GitHub. Put it in a folder where you'll easily find it again.
When download is done, open the visual studio solution. A Visual Studio page should appear.