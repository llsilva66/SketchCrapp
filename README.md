
![banner](https://i.imgur.com/cl2HGy0.gif)

## SketchCrapp
![latest supported](https://img.shields.io/badge/latest%20supported-71.2-brightgreen?style=for-the-badge)
![GitHub Repo stars](https://img.shields.io/github/stars/duraki/SketchCrapp?color=brightgreen&style=for-the-badge)
![GitHub watchers](https://img.shields.io/github/watchers/duraki/SketchCrapp?color=brightgreen&style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/duraki/SketchCrapp?color=brightgreen&style=for-the-badge)

Sketch.App Patch Tool, brought to you by [@duraki](https://github.com/duraki) & [@elijahtsai](https://github.com/elijahtsai). This script provides you a quick and dirty way to patch Sketch.app for Unlimited Trial. You can always patch manually using Ghidra by following [this tutorial](https://duraki.github.io/posts/o/20200214-sketch.app-patch-in-ghidra.html). Offsets available [here](https://github.com/duraki/SketchCrapp/blob/master/README.md#offset-table).

**Download Sketch.App version of your choice here:** https://www.sketch.com/updates/

## Usage

* Open your MacOS Terminal (`Cmd+Space`, type **Terminal**)
* Type the commands below
* Download or clone this repository
  * `cd $HOME && git clone https://github.com/duraki/SketchCrapp`
* Make script executable
  * `cd $HOME/SketchCrapp && chmod +x sketchcrapp.sh`
* Run the script to patch Sketch.app
  * `cd $HOME/SketchCrapp && ./sketchcrapp.sh`

## Magic Trick ✨
For the people who would like to try the new version, we got you covered. You can pass `-m` argument for the ultimate life-saving trick, which will automagically download latest Sketch app from the official website and patch the bundle, ready to be launched from the Applications folder.

One-liner script to install latest Sketch version and automatically patch it:<br />`bash -c "$(curl -s https://raw.githubusercontent.com/duraki/SketchCrapp/master/sketchcrapp.sh -o -)" -O -m`
<br /><br />
![magictrickimage](https://i.imgur.com/gGr8bHi.png)

<p align="center">Successful screenshot of using magic trick</p>

## Notice
 - The application should automatically detect your Sketch.App version. If not, you can pass `-a` argument for your Sketch.app Application Bundle or use `-m` argument to automatically install and crack the latest version.

```
crackb0x:SketchCrapp duraki$ ./sketchcrapp.sh -h
           __       __      __
      ___ / /_____ / /_____/ /  ___________ ____  ___
    ( _-</  '_/ -_) __/ __/ _ \/ __/ __/ _ `/ _ \/ _ \
    /___/_/\_\\__/\__/\__/_//_/\__/_/  \_,_/ .__/ .__/
                                          /_/  /_/
         Sketch.App Patch Tool (https://github.com/duraki/SketchCrapp)
         by @duraki & @elijahtsai

Usage:
./sketchcrapp [-h] [-a] <applicationPath> [-m] [-g] <version>
Supported versions: v58, v63.1, v64.0, v65.1, v66.1, v67, v67.1, v67.2,
v68, v68.1, v68.2, v69, v69.1, v69.2, v70.2, v70.3, v70.4, v70.5, v70.6
v71.1, v71.2
[+] SketchCrapp last published date: 2021-04-12 serial 023
```

```
crackb0x:SketchCrapp duraki$ ./sketchcrapp.sh -m
           __       __      __
      ___ / /_____ / /_____/ /  ___________ ____  ___
    ( _-</  '_/ -_) __/ __/ _ \/ __/ __/ _ `/ _ \/ _ \
    /___/_/\_\\__/\__/\__/_//_/\__/_/  \_,_/ .__/ .__/
                                          /_/  /_/
         Sketch.App Patch Tool (https://github.com/duraki/SketchCrapp)
         by @duraki & @elijahtsai

[+] Hello, The magic show is about to start! Are you ready?
[+] Checking if version 71.2 is supported ...Yes
[+] Fetching https://download.sketchapp.com/sketch-versions.xml ...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
100 85817  100 85817    0     0  53435      0  0:00:01  0:00:01 --:--:--  355k
[+] Generating swift script ...
[+] Zip file download path: https://download.sketch.com/sketch-71.2-115329.zip
[+] Checking directory tmp existence ... OK
[+] Fetching https://download.sketch.com/sketch-71.2-115329.zip ...   
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100 58.5M  100 58.5M    0     0  1805k      0  0:00:33  0:00:33 --:--:-- 2328k
[+] Checking if Sketch.app exist in /tmp ... Not exist. Continuous.
[+] Checking if Sketch.app exist in /Applications ... Exist. Removing.
[+] Moving Sketch.app to /Applications directory ... Successfully.
[+] Analysing application bundle ... Starting
[+] Finding executable file ... OK
[+] Finding Info.plist ... OK
[+] Checking Info.plist for CFBundleShortVersionString ... OK
[+] Validating executable file ... OK
[+] Selected Sketch.app version is 71.2 ... SketchCrapp starting ... OK
[+] Patching offsets for 71.2 ... Starting modern arch patch via bash&seek ...
[+] Patching address at offset: 0x5dccbf with value: \00
1+0 records in
1+0 records out
1 bytes transferred in 0.000147 secs (6809 bytes/sec)
[+] Patching address at offset: 0x5dccc2 with value: \00
1+0 records in
1+0 records out
1 bytes transferred in 0.000024 secs (41528 bytes/sec)
[+] Patching address at offset: 0x5db90e with value: \00\00
2+0 records in
2+0 records out
2 bytes transferred in 0.000021 secs (95325 bytes/sec)
[+] Patching address at offset: 0x5dba3e with value: \165
1+0 records in
1+0 records out
1 bytes transferred in 0.000019 secs (52429 bytes/sec)
[+] Patching address at offset: 0x6cef41 with value: \00\00\00\00\00\00\00\00\00\00\00\00\00\00\00
15+0 records in
15+0 records out
15 bytes transferred in 0.000062 secs (241052 bytes/sec)
[+] Patching address at offset: 0x6cef51 with value: \40\123\153\145\164\143\150\103\162\141\160\160\40
13+0 records in
13+0 records out
13 bytes transferred in 0.000056 secs (232025 bytes/sec)
[+] Patching address at offset: 0xe89f98 with value: \01
1+0 records in
1+0 records out
1 bytes transferred in 0.000017 secs (58254 bytes/sec)
[+] Patching address at offset: 0xe89f9c with value: \24
1+0 records in
1+0 records out
1 bytes transferred in 0.000020 secs (49932 bytes/sec)
[+] Patching address at offset: 0xe9859c with value: \165\00
2+0 records in
2+0 records out
2 bytes transferred in 0.000027 secs (74235 bytes/sec)
[+] Patching address at offset: 0xe986bf with value: \64
1+0 records in
1+0 records out
1 bytes transferred in 0.000025 secs (39946 bytes/sec)
[+] Patching address at offset: 0xfaa308 with value: \00\00\00\00\00\00\00\00\00\00\00\00\00\00\00
15+0 records in
15+0 records out
15 bytes transferred in 0.000085 secs (176231 bytes/sec)
[+] Patching address at offset: 0xfaa318 with value: \40\123\153\145\164\143\150\103\162\141\160\160\40
13+0 records in
13+0 records out
13 bytes transferred in 0.000056 secs (232025 bytes/sec)
[+] Checking user default keychain ... Exist
[+] Checking SketchCrapp identity ... Exist
[+] Skipping certificate creation ... OK
[+] Signing the patched *.app bundle. This may require root privilege.
[+] If asked, enter your login password. Choose "Always Allow" to not be asked again.
/Applications/Sketch.app: replacing existing signature
/Applications/Sketch.app: signed app bundle with Mach-O universal (x86_64 arm64) [com.bohemiancoding.sketch3]
[+] Cleaning up file(s) ... Cleaned
[+] SketchCrapp process completed. Sketch.app has been patched :)
[+] -- Notice:
[+] If a dialogue shows up with message: “Sketch 3.app” can’t be opened
[+] please right-click the application and select open,
[+] or go to Settings -› Security and allow opening Sketch.app application.
[+]
[+] If you are using an old version and a dialogue shows up asking for password
[+] about "com.bohemiancoding.sketch3.HockeySDK"
[+] please enter your login password. Choose "Always Allow" to not be asked again.

[+] SketchCrapp (A Sketch.app cracking tool)
[+] https://github.com/duraki/SketchCrapp [by @duraki & @elijahtsai]
[+] SketchCrapp last published date: 2021-04-12 serial 023
```

## Issues

If you have troubles using the script, please contact the team via GitHub Issues.

---
## Version Request

#### Higher Version

If the version you are trying to patch is higher than supported, please notify the team via GitHub Issues.

#### Lower Version

If you really need specific version you can contact the team via GitHub Issues, but we can only do our best to help you.

**Build with ❤️ by [@duraki](https://twitter.com/0xduraki) & [@elijahtsai](https://twitter.com/elijahtsai_)**

**Special Fans: [@JosephShenton](https://github.com/JosephShenton) & [@Aurther-Nadeem](https://github.com/Aurther-Nadeem)**

> [Original idea and thread](https://gist.github.com/Bhavdip/76c581d7ac03bdce6d226a2e8c522df4)

### Offset Table
|58|63.1|64|65.1|66.1|67 & 67.1|
|----|----|----|----|----|----|
|0x1003912c0|0x1004a2a50|0x1004cde70|0x1004db500|0x1004f3750|0x10050a6d0|
|0x10038ff14|0x1004a1724|0x1004ccb44|0x1004da1d4|0x1004f2424|0x100509394|
|0x10038ff2c|0x1004a1738|0x1004ccb58|0x1004da1e8|0x1004f2438|0x1005093a8|
|0x10038ff32|0x1004a173e|0x1004ccb5e|0x1004da1ee|0x1004f243e|0x1005093ae|
|0x10039007d|0x1004a1879|0x1004ccc99|0x1004da329|0x1004f2579|0x1005094e9|
|0x10039009a|0x1004a1896|0x1004cccb6|0x1004da346|0x1004f2596|0x100509506|

|67.2|68|68.1 & 68.2|69|69.1 & 69.2|
|----|----|----|----|----|
|0x10050a790|0x10054d2b0|0x10054d350|0x1005cf770|0x1005d09e0|
|0x100509454|0x10054bf74|0x10054c014|0x1005ce434|0x1005cf564|
|0x100509468|0x10054bf88|0x10054c028|0x1005ce448|0x1005cf57c|
|0x10050946e|0x10054bf8e|0x10054c02e|0x1005ce44e|0x1005cf582|
|0x1005095a9|0x10054c0c9|0x10054c169|0x1005ce589|0x1005cf6ae|
|0x1005095c6|0x10054c0e6|0x10054c186|0x1005ce5a6|0x1005cf6d2|

### Stars Record
|⭐️|Date|
|:----:|:----:|
|100|2020-11-20|
|150|2021-01-15|
|200|2021-03-04|
|250|soon 🙉|

### Stargazers over time
[![Stargazers over time](https://starchart.cc/duraki/SketchCrapp.svg)](https://starchart.cc/duraki/SketchCrapp)
