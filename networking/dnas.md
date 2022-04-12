---
title: DNAS
description: 
published: true
date: 2022-04-12T09:45:34.171Z
tags: authentication, network, errors
editor: markdown
dateCreated: 2022-03-05T00:48:38.418Z
---

# Dynamic Network Authentication System (DNAS)

Dynamic Network Authentication System is a proprietary authentication system created by Sony Computer Entertainment Inc.

> DNAS retrieves information about a user’s hardware and software for authentication,  
> copy protection, account blocking, system, rules, or game management and other purposes.  
> The information collected does not identify the user personally. A publisher can combine  
> this information with personally identifying information from the publisher’s records if  
> the user provides the personally identifying information. Before providing any personal  
> information to a publisher please be sure to review the publisher’s privacy policy and  
> terms and conditions of use. Do not provide personally identifying information to a  
> publisher unless you accept the conditions of use and terms of their privacy policy.  
> SCEI, Sony Computer Entertainment America ("SCEA") and their affiliates cannot guarantee  
> the continuous operation of the "DNAS" servers. SCEA shall not be liable for any delay or  
> failure of the "DNAS" servers to perform.
{.is-info}

## Discontinuation

On April 4, 2016; SCEI discontinued the official DNAS servers, thus forcefully taking down hundreds of multiplayer game titles with it.

## Official DNAS domains

-   [gate1.us.dnas.playstation.org](http://gate1.us.dnas.playstation.org) - USA
-   [gate1.jp.dnas.playstation.org](http://gate1.jp.dnas.playstation.org) - Japan
-   [gate1.eu.dnas.playstation.org](http://gate1.eu.dnas.playstation.org) - Europe

## Status Codes

-   \-101 to -108: **Authentication**
-   \-201 to -204: **Downloading**
-   \-401 to -404: **Hardware**
-   \-601 to -625: **Network**
-   \-701 to -703: **Unique ID**
-   \-800 to -1099: **Unexpected**

| Code | Name | Description |
| --- | --- | --- |
| \-101 | sceDNAS2\_SS\_SERVER\_BUSY | DNAS server is busy. "DNAS Error (-101) The network authentication server is busy. Please try again later." |
| \-102 | sceDNAS2\_SS\_BEFORE\_SERVICE | DNAS authentication service period has not started for this title. "DNAS Error (-102) This software title is not in service." |
| \-103 | sceDNAS2\_SS\_OUT\_OF\_SERVICE | DNAS authentication service period has ended for this title. "DNAS Error (-103) This software title is not in service." |
| \-104 | sceDNAS2\_SS\_END\_OF\_SERVICE | All DNAS services have stopped. "DNAS Error (-104) The network authentication server is not in service." |
| \-105 | sceDNAS2\_SS\_SESSION\_TIME\_OUT | Session timeout. "DNAS Error (-105) Connection to the network authentication server has timed out. Please try again later." |
| \-106 | sceDNAS2\_SS\_INVALID\_SERVER | DNAS library (PS2) received an invalid server response. "DNAS Error (-106) A network authentication system error has occurred." |
| \-107 | sceDNAS2\_SS\_INTERNAL\_ERROR | DNAS library (PS2) internal error while authentication DNAS server. "DNAS Error (-107) A network authentication system error has occurred." |
| \-108 | sceDNAS2\_SS\_EXTERNAL\_ERROR | DNAS server received corrupted data. "DNAS Error (-108) A network authentication system error has occurred." |
| \-201 | sceDNAS2\_SS\_DL\_NODATA | This title does not have a data download service. "DNAS Error (-201) A download error has occurred." |
| \-202 | sceDNAS2\_SS\_DL\_BEFORE\_SERVICE | Data download service has not started for this title. "DNAS Error (-202) A download error has occurred." |
| \-203 | sceDNAS2\_SS\_DL\_OUT\_OF\_SERVICE | Data download service has ended for this title. "DNAS Error (-203) A download error has occurred." |
| \-204 | sceDNAS2\_SS\_DL\_NOT\_UPDATED | No new download data. "DNAS Error (-204) A download error has occurred." |
| \-401 | sceDNAS2\_SS\_INVALID\_PS2 | Invalid PS2 hardware. "DNAS Error (-401) A PS2 hardware information error has occurred." |
| \-402 | sceDNAS2\_SS\_INVALID\_MEDIA | Invalid disc. "DNAS Error (-402) A PS2 disc information error has occurred." |
| \-403 | sceDNAS2\_SS\_INVALID\_AUTHDATA | Invalid or corrupted disc authentication data. "DNAS Error (-403) A PS2 disc information error has occurred." |
| \-404 | sceDNAS2\_SS\_INVALID\_HDD\_BINDING | Current PS2 and HDD combination is different than registered combination. "DNAS Error (-404) A PS2 hardware information error has occurred." |
| \-501 | sceDNAS2\_SS\_MISMATCH\_AUTHDATA | Failed in registering auth data to the database on the server side. |
| \-601 | GLUE\_ABORT | An network connection was aborted. "DNAS Error (-601) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-602 | NET\_PROXY | Proxy server error. "DNAS Error (-602) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-603 | NET\_TIMEOUT | Connection timed out. "DNAS Error (-603) Connection timed out." Please try connection again at a later time. |
| \-610 | NET\_SSL | An SSL session error occured. "DNAS Error (-610) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-611 | NET\_DNS\_HOST\_NOT\_FOUND | The DNS resolver did not recognize the DNAS server host name. "DNAS Error (-611) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-612 | NET\_DNS\_TRY\_AGAIN | The DNS resolver cannot be found. "DNAS Error (-612) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-613 | NET\_DNS\_NO\_RECOVERY | The DNS resolver response is invalid. "DNAS Error (-613) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-614 | NET\_DNS\_NO\_DATA | The DNS resolver found no IP address for the DNAS server host name. "DNAS Error (-614) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-615 | NET\_DNS\_OTHERS | Other DNS resolver-related errors. "DNAS Error (-615) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-616 | NET\_EISCONN | A server connection already exists from this client IP address. "DNAS Error (-616) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-617 | NET\_ETIMEOUT | A network timeout occurred. "DNAS Error (-617) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-618 | NET\_ECONNREFUSED | The connection was refused (the server is not running). "DNAS Error (-618) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-619 | NET\_ENETUNREACH | The network destination is unreachable. "DNAS Error (-619) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-620 | NET\_ENOTCONN | The network connection is down. "DNAS Error (-620) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-621 | NET\_ENOBUFS | An out-of-memory error occured. "DNAS Error (-621) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-622 | NET\_EMFILE | Unable to create any more network connections. "DNAS Error (-622) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-623 | NET\_EBADF | The title requested a network connection using an invalid value. "DNAS Error (-623) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-624 | NET\_EINVAL | The title requested a network function using invalid options. "DNAS Error (-624) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-625 | NET\_OTHERS | Other network-related errors. "DNAS Error (-625) A network error has occurred." Please double-check your network connection and/or network configuration. |
| \-626 |     | "Connection to the DNAS server failed." The server and port the client attempted connecting to is closed. |
| \-701 | sceDNAS2\_SS\_ID\_NOUSE | The title does not use the unique *category* ID feature. "DNAS Error (-701) A software category error has occurred." |
| \-702 | sceDNAS2\_SS\_ID\_CAT\_NOT\_EXIST | The specified unique *category* ID category does not exist. "DNAS Error (-702) A software category error has occurred." |
| \-703 | sceDNAS2\_SS\_ID\_NOT\_JOIN\_TO\_CAT | The title does not belong to the specified unique *category* ID category. "DNAS Error (-703) A software category error has occurred." |
| \-832 |     | Unregistered title ID. Incorrect title ID in SYSTEM.CNF. Using the wrong regional DNAS library, thus talking to the wrong DNAS server. Using the production server (debug=0) without DNS redirection. |
| \-848 |     | Unregistered title ID. Incorrect title ID in SYSTEM.CNF. Using the wrong regional DNAS library, thus talking to the wrong DNAS server. Using the production server (debug=0) without DNS redirection. |
| \-848 |     | Wrong authentication data or passphrase. |
| \-833 |     | Region Error. |
| \-840 |     | Server is down, try again later. |
| \-864 |     | Invalid media, Invalid DNAS Disc ID, Media Error e.g. using CD-R and DVD-R discs against the production server, or using manufactured discs against the development server. |
| \-880 |     | PS2 hardware incompatibility. |
| \-881 |     | PS2 hardware incompatibility. |

## Solution

The shutdown of DNAS has caused hundreds of multiplayer titles go offline with it. The community has went above and beyond to try to revive many game servers.

Since SCEI discontinued DNAS, there have been a few replacement services out there, such as:

| Name | Primary DNS | Secondary DNS | Websíte |
| --- | --- | --- | --- |
| Cristian | 45.7.228.197 | 0.0.0.0 | [https://ps2online.com](https://ps2online.com) |
| Bobz | 66.66.23.98 | 0.0.0.0 | [http://bobzent.info](http://bobzent.info) |
| Outbreak | 173.198.207.99 | 0.0.0.0 | [http://obsrv.org](http://obsrv.org) |
| MGO | 192.3.217.61 | 192.3.217.162 | [https://snake.savemgo.com](https://snake.savemgo.com) |
| TM:BO | 173.198.252.240 | 0.0.0.0 | [http://173.198.252.240](http://173.198.252.240) |
| SWBFSpy | 66.85.14.80 | 0.0.0.0 | [http://www.swbfgamers.com](http://www.swbfgamers.com) |
| PS Rewired | 135.148.144.253 | 0.0.0.0 | [https://socomcommunity.com](https://socomcommunity.com) |
## How replacement services works

DNAS protection works on the http protocol. However, all communication is encrypted and private keys are not available. Replacement servers always return the success result that was captured from the packet when the official DNAS protection was operational. Each game has a different response. If DNAS responses were not captured for a game, a patch needs to be applied.