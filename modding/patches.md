---
title: Patches
description: Here's a "tutorial" about how works patches and how to use them  when it is possible.
published: true
date: 2022-04-12T14:03:07.791Z
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
The **patches** are available in the **data** subfolder (`NPUA00001\USRDIR\data`) for **Ratchet & Clank** games, the patches are globally `patch_XX.psarc`{.orange-code} (`XX` are numbers from `00` to `99`).
**For more informations on the [PSArc files](./modding/filesformat#psarc), go on its page.**
The `.psarc` archives contain only files which have to change. It means that the `patch_XX.psarc` archive make every files that are into it overwrite `global_uncached.psarc` archive files.

## How's the patch architecture ?
First, you have to understand that the patch come from the **USRDIR** directly. You'll have to think relative.
For example, if I want to modify the **jungle_ruin** level in **FFA**, I'll have to put my modifications like this:
`patch_06\built\levels\jungle_ruin\` <= *my modified files in here.* - It's the same thing into **USRDIR**:
`USRDIR\built\levels\jungle_ruin\` <= *here, there's `level_uncached.psarc` for example*

