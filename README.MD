
# Welcome to the Raise the Empires Preservation Project

![Empires & Allies Logo](empiresservercontainer/rte_staging_assets/templates/layouts/logo.png "Empires & Allies Logo")

[![Gitpod Ready-to-Code](https://img.shields.io/badge/Gitpod-Ready--to--Code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native)

> Empires and Allies (Facebook) officially closed on June 17th, 2013.

:world_map: [Main Repository](https://github.com/AcidCaos/raisetheempires#readme)

The Raise the Empires team presents the Old Empires & Allies Preservation Project, dedicated to safeguarding and rejuvenating this Flash game to ensure it endures the test of time.

## Current Status
| Attribute              | Value                              |
| -----------------------| ---------------------------------- |
| Current Developed Build| ![version](https://img.shields.io/badge/build-480-blue) |
| Current Releases       | ![version](https://img.shields.io/badge/build-470-blue) |
| Current Main Repo Size | [![size](https://img.shields.io/badge/size-585%20MB-brightgreen)](#) |
| Current Source Size    | [![size](https://img.shields.io/badge/size-30%20MB-brightgreen)](#) |

<!--
## Releases

| Build  | Update                                         | Release date  | Release details |
| -------| ---------------------------------------------- | -------------- | --------------- |
| 467~470| Platform Trial, ssh keyfixes, Content update merge with version 0.06a | July, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_46x)
| 450    | Added support for new termux dependencies       | June, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_450) |
| 416~418| ServerID implementation, Virtualenv dependencies, etc.. | May, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_416) |
| 319~325| Invading feature, Major bug fixes, Stability improvement, etc.. | April, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_319) |
| 260    | Invade neighbors initial for Build 319         | April, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_260) |
| 239~257| Base32 and base64 Encoder, Liveupdate           | April, 2020 | [Release cancelled] |
| 210    | Added Local mode feature & Stability improvements | April, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_210) |
| 201    | New Welcome screen & Simpler installation with 'curl' | April, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_201) |
| 193    | Custom ssh config & Merge with new main repo    | April, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_193) |
| 185    | UI Overhaul & Additional bonus decorations      | March, 2020 | :tickets: [Single Script Archive](https://github.com/Questandachievement7Developer/RaiseTheEmpiresPort_Native/releases/tag/Build_185) |
| 171    | Initial for UI Overhaul                         | March, 2020 | [Release cancelled] |
| 129    | Multiplayer Update Merge with version 0.05a     | February, 2020 | :tickets: [Single Script Archive](http://tiny.cc/RaiseTheEmpires_129) |
| 119    | Automatic Host forwarding                       | January, 2020 | :tickets: [Single Script Archive](http://tiny.cc/EALSERVE119) |
| 99     | Initial Host forwarding                         | January, 2020 | [Release cancelled] |
| 57~58  | First initial Release on android x86 and GNU systems natively | January, 2020 | :tickets: [Single Script Archive](http://tiny.cc/RaiseTheEmpires2020_01_24) |
| 20     | Released noArch version                         | January, 2020 | :tickets: [Single Script Archive](http://tiny.cc/RaiseTheEmpires29TNoArch) |
-->

## How to Install?
### Installing on Android using Termux
1. Install Puffin Browser from the Play Store.
2. Download the latest version of Termux from [here](https://github.com/termux/termux-app/releases).
3. Copy and paste the following command into Termux (You only need to do this once):
   ```bash
   pkg install git wget python -y
   pkg update
   pkg install libxml2 libxslt -y
   pkg install dropbear -y
   pkg install openssh -y
   git clone https://github.com/AcidCaos/raisetheempires
   pip install "git+https://github.com/hex-in/libscrc.git"
   pip install tendo py3amf "flask<2.1.0" flask_session flask_sqlalchemy flask_compress flask_socketio daiquiri python-editor xmldiff jsonpatch tqdm
   ```
4. Press Enter to run the command.
5. If there's a confirmation [Y/n], type Y.
6. If there are several confirmations [Y/I/N/O/D/Z], type Y.
7. Wait until the installation is completed (and ensure your internet connection is stable).

Then use this command every time you want to play:
   ```bash
   cd raisetheempires
   python empires-server.py --no-popup --no-crash-log --port 5005
   ```
   Press Enter to run the command.

After that, swipe left on Termux and tap the 'New Session' option. Copy this command to start hosting on a public link:
   ```bash
   ssh -R 80:localhost:5005 nokey@localhost.run
   ```
   Press Enter to run the command. If there's a confirmation [yes/no], type yes. Copy the generated link into Puffin Browser.

*Done*

### Installing on GNU/Linux/Ubuntu
1. Assuming you have the terminal opened.
2. Copy and paste this command into the terminal (You only need to do this once):
   ```bash
   sudo apt update
   sudo apt install python3 python3-pip
   git clone https://github.com/AcidCaos/raisetheempires
   cd raisetheempires
   pip3 install -r requirements.txt
   ```

Then use this command every time you want to play:
   ```bash
   python3 empires-server.py --no-popup --no-crash-log --port 5005
   ```
   You need to use a Flash-enabled browser, then go to this URL: http://127.0.0.1:5005

*Optional*: If you want to host online on a public link, open a new terminal window and use this command:
   ```bash
   ssh -R 80:localhost:5005 nokey@localhost.run
   ```
   If there's confirmation [yes/no], type yes.

*Done*

### Installing on macOS
1. Download Python 3.8 from [here](https://www.python.org/ftp/python/3.8.6/python-3.8.6-macosx10.9.pkg).
2. Install it.
3. Then open Terminal, copy and paste this command (You only need to do this once):
   ```bash
   git clone https://github.com/AcidCaos/raisetheempires
   cd raisetheempires
   pip3 install -r requirements.txt
   ```
   If there's a notice that you haven't installed Xcode, install it first.

Then use this command every time you want to play:
   ```bash
   python3 empires-server.py --no-popup --no-crash-log --port 5005
   ```
   You need to use a Flash-enabled browser, then go to this URL: http://127.0.0.1:5005

*Done*

## Need Assistance or Have Questions?
Feel free to reach out to us:

:email: questandachievement@gmail.com

Personal Discord: Yuuta kun#5097

Join our community Discord [Discord group](https://discord.gg/xrNE6Hg)

> Don't hesitate to ask; we are here to help, and we won't judge if you have many questions! 😄

## Reporting Bugs and Contacting
:speech_balloon: Check our Community [Discord group](https://discord.gg/xrNE6Hg)  [![Discord Channel](https://img.shields.io/discord/536575691563466772?label=)](https://discord.gg/xrNE6Hg)

## Tools
:world_map: [Empires & Allies Empire Map Editor](https://github.com/AcidCaos/ea-empire-editor)

:classical_building: [Emipres & Allies Revision History](https://github.com/AcidCaos/empires-revision-history#readme)

:minidisc: [Empires & Allies Servers Support](https://github.com/AcidCaos/raisetheempires/blob/master/SERVERS.md)

## External Links
:beginner: [Empires & Allies Wiki (FANDOM)](https://empiresandallies.fandom.com/wiki/Empires_%26_Allies_Wiki/Main_2)

:clapper: [Empires & Allies Trailer](https://www.youtube.com/watch?v=pAdlyz9miqo)

:smiley_cat: [Empires & Allies subreddit](https://reddit.com/r/EmpiresAndAllies)

## On Archives and Accessibility to Digital Heritage
- [Exemption to PCCPSACT](https://www.federalregister.gov/documents/2018/10/26/2018-23241/exemption-to-prohibition-on-circumvention-of-copyright-protection-systems-for-access-control), exemptions to the provision of the Digital Millennium Copyright Act (“DMCA”).
- [EFGAMP](https://efgamp.eu/), the European Federation of Video Game Archives, Museums, and Preservation projects.
- [UNESCO PERSIST Programme](https://unescopersist.org/), helps ensure that digital information can continue to be accessed in the future.
- [The Internet Archive](https://archive.org/), a digital library of Internet sites and other cultural artifacts in digital form.
- [BlueMaxima's Flashpoint](https://bluemaxima.org/flashpoint/), the web game preservation project.

[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue)](http://www.gnu.org/licenses/gpl-3.0)

```
Old Empires and Allies preservation project Copyright (C) 2019-2023 by the Raise the Empires team.

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
```