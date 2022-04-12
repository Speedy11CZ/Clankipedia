---
title: Patches
description: Here's a "tutorial" about how works patches and how to use them  when it is possible.
published: true
date: 2022-04-12T11:15:22.648Z
tags: information, modding, online, patches
editor: markdown
dateCreated: 2022-04-12T10:04:47.681Z
---

# How work patches ?
Patches are basically working like for **every games** on computer that aren't made with **new generation engines** or which are **not hosted on specific update systems**.
So, how exactly does it work ?
Into the **game root folder** you should see something like `USRDIR`. This folder contains everything like game *engine files for some games*, and globally **textures**, **models**, **maps**, **scripts**, etc...

## Where can I find it ?
For **Ratchet & Clank** games, the patches are only available **natively** on **Ratchet & Clank: Full Frontal Assault**, **Ratchet & Clank: All 4 One** and **Ratchet & Clank: Into the Nexus**.
The **patches** are available in the **data** subfolder (`NPUA00001\USRDIR\data`) for **Ratchet & Clank** games, the patches are globally `patch_XX.psarc` (`XX` are numbers from `00` to `99`).
**For more informations on the [PSArc files](./modding/filesformat#psarc), go on its page.**
The `.psarc` archives contain only files which have to change. It means that the `patch_XX.psarc` archive make every files that are into it overwrite `global_uncached.psarc` archive files.