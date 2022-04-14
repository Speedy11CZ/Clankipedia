---
title: Patches
description: All you need to know about modding using patch system of Ratchet & Clank (FFA to ItN)
published: true
date: 2022-04-14T12:55:47.281Z
tags: information, installing, modding, online, patches
editor: markdown
dateCreated: 2022-04-12T10:04:47.681Z
---

# How work patches ?
Patches are basically working like for **every games** on computer that aren't made with **new generation engines** or which are **not hosted on specific update systems**.
So, how exactly does it work ?
Into the **game root folder** you should see something like `USRDIR`. This folder contains everything like game *engine files for some games*, and globally **textures**, **models**, **maps**, **scripts**, etc...

## Where can I find it ?
For **Ratchet & Clank** games, the patches are only available **natively** on **Ratchet & Clank: Full Frontal Assault**, **Ratchet & Clank: All 4 One** and **Ratchet & Clank: Into the Nexus**.
The **patches** are available in the **data** subfolder (`NPUA00001\USRDIR\data`{.orange-code}) for **Ratchet & Clank** games, the patches are globally `patch_XX.psarc`{.orange-code} (`XX` are numbers from `00` to `99`).
**For more informations on the [PSArc files](./filesformat#psarc), go on its page.**
The `.psarc`{.orange-code} archives contain only files which have to change. It means that the `patch_XX.psarc`{.orange-code} archive make every files that are into it overwrite `global_uncached.psarc`{.orange-code} archive files.

## How's the patch architecture ?
First, you have to understand that the patch come from the **USRDIR** directly. You'll have to think relative.
For example, if I want to modify the **jungle_ruin** level in **FFA**, I'll have to put my modifications like this:
`patch_06\built\levels\jungle_ruin\`{.orange-code} <= *my modified files in here.* - It's the same thing into **USRDIR**:
`USRDIR\built\levels\jungle_ruin\`{.orange-code} <= *here, there's `level_uncached.psarc`{.orange-code} for example*

## What can I change into ?
Technically, almost everything. Adding a map is simple and hard, duplicate a map (<kbd>CTRL</kbd> + <kbd>C</kbd>) into your patch folder (<kbd>CTRL</kbd> + <kbd>V</kbd>), for example like this: `patch_06\built\levels\my_new_level`{.orange-code}. Do not forget that you won't be able to load that level without coding. Anyway, you can now modify the level with the **[LombaxToes Editor](../tools/lteditor)**.
You can also change code, by replacing old `.lc` files with new `.lc` files. The code have to respect the functions used in other `lua` files.
To change script files, you can add your new compiled `lua` files into `patch_06\built\levels\my_new_level\scripts\main.lc`{.orange-code}.
The patch size is of course not limited, however if you modify already existing `lua` files, do not forget to backup them before, and that the code into them **does not concatenate** to the original file, it **overwrite totally the file**. So each time you modify a lua file, remember you have to **compile it** into `luac` format (`.lc`{.orange-code} format)
So globally, this technic work for these modifications[:](https://www.youtube.com/watch?v=dQw4w9WgXcQ)
* `Data` (`.dat`{.orange-code}) files - Contain generally textures, models, map regions, etc...
* `Script` (`.lc`{.orange-code}) files - Compiled lua script files. Globally they are used for every event stuff in the game, and weapons events.
* `Tables` (`.csv`{.orange-code}) files - Tables that contains statistics of weapons. Changing them change also the weapon's stats.
* `Packages` (`.pkg`{.orange-code}) files - These are archives too, they can contain **voicelines**, **environnement sounds**, **weapons sounds**, **game musics**...

## How can I install a patch ?
To install a patch, you need first a **Custom FirmWare** or a **Hybrid FirmWare**. The most famous are **[Cobra CFW](https://www.psx-place.com/threads/ps3xploit-flash-writer-aka-cfw-installer-supports-all-ps3-fat-models-most-slim-models.16876/)** ([here](https://www.youtube.com/watch?v=QldjWRGH0wA&ab_channel=MrMario2011) is a tutorial), and **[HEN HFW](http://ps3xploit.com/)** ([here](https://www.youtube.com/watch?v=xGS_Ryx_7r8&ab_channel=MrMario2011) is a tutorial)

When you have finally your **CFW** (for **FAT**) or **HFW** (for **SLIM** and **SUPERSLIM**) on your PS3, you need to put your patch on an **USB key FORMATTED in FAT32** and also the `.pkg`{.orange-code} of **[multiMAN](https://store.brewology.com/ahomebrew.php?brewid=24)** (latest version for **Cobra CFW** and unoffical one for **HEN**, then plug the **USB key** into your console.
Now, go to `⭐ Package Manager > 📁 Install Package File > 📁 Package Directory` and install your **multiMAN** package file.
Launch **multiMAN** and go to the file explorer.
go to `/dev_usb000/`{.orange-code}, search your `patch_XX.psarc`{.orange-code} file, copy it, and then go to `/dev_hdd000/game/`{.orange-code} and now, search for the code of the game your modding, for example, the **European Disc** of **Ratchet & Clank: Full Frontal Assault** *(Q-Force)* code is `BCES001954`, so the dir is `/dev_hdd000/game/BCES001954/`{.orange-code}, etc...
Into the game folder, find `USRDIR/data`{.orange-code} folder, and drop the file in.
For example, for our patch it should look like this: `/dev_hdd000/game/BCES001954/USRDIR/data/patch_06.psarc`{.orange-code}

## ⚠️ - Warning!
Before launching your game, disable the game update checking into your **CFW** (not sure for HFW, please check), or your update will be deleted and overwrote by an older one. If the game you mod is online, **be extremely careful** and disable the **Sony PSN Logging** on your **CFW**, they are sent to Sony and sometime it happens that players get banned... It's rare but be careful.

## Patches limitations
With patches, you can modify a lot of files, however there are rules:
- The patch **have to respect** the game folders architecure
- You cannot put `.psarc`{.orange-code} files into a patch, first it's useless, and the PlayStation will not be able to read it. (It can read only specific folders with specific files)
	- Tolerated / readable formats:
    `.pkg`{.orange-code} packages - sounds archive for example
		`.lc`{.orange-code} compiled scripts - lua compiled code
		`.dat`{.orange-code} textures, models & instructions - archives ?
   	`.BIN`{.orange-code} the only known file with this extension is `EBOOT.BIN`
* You cannot just put the new code like this, convert it to `.lc`{.orange-code} file and drop it into your file. You have to continue the already existing code and then put it in the patch.

## Games using patch system
All the games using a patch system, however only the ones that download them using the Playstation Network.
- Ratchet & Clank: All 4 One; `NPEA00356`, `BCES01141`, `NPUA80695`, `BCUS98175`
- Ratchet & Clank: Full Frontal Assault / Q-Force; `NPEA00378`, `BCES01594`, `NPUA80642`, `BCUS98380`
- Ratchet & Clank: Into the Nexus / NEXUS; `NPEA00457`, `BCES01908`, `BCES01949`, `NPUA80908`, `BCUS99245`
- Ratchet & Clank: A Crack in Time; `BCES00511`, `BCES00726`, `BCUS98124` - ⚠️ This game don't use the same patch system, and the patches are only for disc versions of the game.