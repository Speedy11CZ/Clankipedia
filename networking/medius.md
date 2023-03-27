---
title: Medius (SCE-RT)
description: Medius (SCE-RT) was a networking engine solution that most top-title games would have implemented for their multiplayer games as the underlying protocol.
published: true
date: 2023-03-27T23:37:48.933Z
tags: api, authentication, modding, network, online
editor: markdown
dateCreated: 2023-03-27T22:34:20.364Z
---

# Medius (SCE-RT)
Medius (SCE-RT) was a networking engine solution that most top-title games would have implemented for their multiplayer games as the underlying protocol. 

There is very little documentation regarding it therefore it's not fully understood and the only parts that we know of have to be reverse-engineered.

## Documentation
[Medius Components API](/medius/medius_components-api.pdf)
[Medius API Overview](/medius/sce-rt_sdk_medius_api_overview.pdf)
[Medius API Reference](/medius/sce-rt_sdk_medius_api_reference.pdf)
[DME API Overview](/medius/sce-rt_sdk_dme_api_overview.pdf)
[DME API Reference](/medius/sce-rt_sdk_dme_api_reference.pdf)
[MGCL API Overview](/medius/sce-rt_sdk_mgcl_api_overview.pdf)
[MGCL API Reference](/medius/sce-rt_sdk_mgcl_api_reference.pdf)
[SOCOM GDC 2003 Presentation](/medius/socom_gdc_2003_presentation.pdf)

## Components
Medius servers are split into 6 major components:

### Medius Universe Information Server (MUIS)
- Server for providing the client with multiple other Medius stacks (MAS/MLS/MPS/DME).
- This server generally runs on port `10071`.

### Medius Universe Manager (MUM)
- Keeps track of lobby rooms, game information, and players. 
- This server generally runs on port `10076`.

### Medius Authentication Server (MAS)
- Allows users to login, authenticate and obtain a session token to login to the Medius Lobby Server.
- This server generally runs on port `10075`.

### Medius Lobby Server (MLS)
- Handles license agreement, announcements, global chat room, clans, create games, and join games.
- This server generally runs on port `10077` or sometimes `10078`.

### Medius Proxy Server (MPS)
- Global chat room, clans, create games, and join games.
- This server generally runs on port `10078`.

### Distributed Memory Engine - Game Server (DME)
- The DME Game Server is a "Reliable UDP" server that handles connections between clients on a game's current status.

### Medius Network Address Translation (NAT)
- A UDP server used to give the client their IP Address.

## Protocol
All encrypted Medius packets are structured as follows:

(This is an example MAS login packet from a PlayStation 2 client)

```
00000000  92 40 00 f4 f8 7a f7 34  25 c8 9a 6d a9 dd eb ab   .@...z.4 %..m....
00000010  a8 3c a6 e6 b4 72 6d ef  51 23 00 de ea 43 d5 8f   .<...rm. Q#...C..
00000020  22 50 3f af 9c 52 96 10  7c a4 be a9 57 8a ae 49   "P?..R.. |...W..I
00000030  68 06 20 73 c6 24 a8 07  ad 44 d2 54 29 8d 58 b6   h. s.$.. .D.T).X.
00000040  3c da 3b e4 33 8c 57                               <.;.3.W
```

---

|Packet ID (1)|Length (2)|Checksum (4)|Data (64)|
|-------------|----------|------------|---------|
|92|40 00|f8 7a f7 34|25 c8 9a 6d a9 dd eb ab a8 3c a6 e6 b4 72 6d ef 51 23 00 de ea 43 d5 8f 22 50 3f af 9c 52 96 10 7c a4 be a9 57 8a ae 49 68 06 20 73 c6 24 a8 07 ad 44 d2 54 29 8d 58 b6 3c da 3b e4 33 8c 57|

---


