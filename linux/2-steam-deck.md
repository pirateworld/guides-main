# Contents
-	[Steam Deck](#steam-deck)
  - [Overview and Principles](#overview-and-principles)
  - [Getting Started With Non-Steam Games - Game Launchers](#getting-started-with-non-steam-games-game-launchers)
    - [Game Launchers](#game-launchers)
      - [What is a Game Launcher?](#-what-is-a-game-launcher)
      - [Which Game Launcher Should I Use?](#-which-game-launcher-should-i-use)
        - [TL;DR](#-tldr)
        - [Pros and Cons of Different Launchers / Most Used Launchers](#-pros-and-cons-of-different-launchers-most-used-launchers)
          - [Steam](#steam)
          - [Lutris](#lutris)
          - [Bottles](#bottles)
        - [Other Launchers](#-other-launchers)
          - [Heroic Launcher](#heroic-launcher)
    - [Proton and Wine](#proton-and-wine)
      - [TL;DR](#-tldr-1)
      - [What are Wine and Proton 'Runners'?](#-what-are-wine-and-proton-runners)
        - [What are Proton-GE, Wine-GE, Lutris-GE, and Caffe?](#-what-are-proton-ge-wine-ge-lutris-ge-and-caffe)
      - [Should I be using Proton, Proton Experimental, or Proton-GE for my Steam game?](#-should-i-be-using-protonproton-ge-or-wine-ge-for-my-games)
    - [Getting Started with Non-Steam Games - Installing Non-Steam Games](#getting-started-with-non-steam-games-installing-non-steam-games)
      - [Step 1: Updating Proton / Wine](#a-step-1-updating-proton-wine)
        - [TL;DR](#-tldr-2)
        - [Installing Different Proton / Wine Versions Using ProtonUp-Qt](#-installing-different-proton-wine-versions-using-protonup-qt)
      - [Step 2: Installing Non-Steam Games](#b-step-2-installing-non-steam-games)
        - [Installing Non-Steam Games Through Steam](#-installing-non-steam-games-through-steam)
          - [TL;DR](#-tldr-3)
            - [Installing using an Installer (Including Repacks)](#-installing-using-an-installer-including-repacks)
            - [Installing A "Portable"/"Preinstalled"/"Clean Steam Files" Game](#-installing-a-portablepreinstalledclean-steam-files-game)
          - [Installing using an Installer (Including Repacks)](#-installing-using-an-installer-including-repacks-1)
          - [Installing A "Portable"/"Preinstalled"/"Clean Steam Files" Game](#-installing-a-portablepreinstalledclean-steam-files-game-1)
        - [Installing Non-Steam Games Through Lutris](#-installing-non-steam-games-through-lutris)
          - [TL;DR](#-tldr-4)
            - [Installing a Game on Lutris from an Installer File](#installing-a-game-on-lutris-from-an-installer-file)
  - [Getting Started with Steam Games - Dependencies](#getting-started-with-steam-games-dependencies)
    - [A) About Dependencies](#a-about-dependencies)
      - [What are Dependencies?](#-what-are-dependencies)
      - [What Dependencies Does My Game Need?](#-what-dependencies-does-my-game-need)
        - [Common Dependencies](#-common-dependencies)
          - [Windows Dependencies](#-windows-dependencies)
          - [Linux Dependencies](#-linux-dependencies)
        - [Using Steamdb.info to Determine Dependencies](#-using-steamdbinfo-to-determine-dependencies)
    - [B) Installing Dependencies](#b-installing-dependencies)
      - [Installing Dependencies Using Winetricks / Protontricks](#-installing-dependencies-using-winetricks-protontricks)
        - [What are Winetricks / Protontricks?](#-what-are-winetricks-protontricks)
      - [Manually Installing Dependencies](#-manually-installing-dependencies)
        - [Manually Installing Via Steam](#-manually-installing-via-steam)
        - [Manually Installing Via Lutris](#-manually-installing-via-lutris)
        - [Manually Installing Via Bottles](#-manually-installing-via-bottles)
  - [Getting Started with Non-Steam Games - Assigning Box Art in Steam](#getting-started-with-non-steam-games-assigning-box-art-in-steam)
  - [Common Errors and How to Solve Them](#6-common-errors-and-how-to-solve-them)
    - ["Failed to open game.uproject"](#-failed-to-open-gameuproject)
    - ["Steam Controller Isn't Picking Up Inputs for My Game](#-steam-controller-isnt-picking-up-inputs-for-my-game)
    - [DX12 is not Supported on Your System](#-dx12-is-not-supported-on-your-system)
  - [F.A.Q.](#7-faq)
    - [Controller Profiles for Non-Steam Games](#-controller-profiles-for-non-steam-games)
    - [Cloudsync Non-Steam Games](#-cloudsync-non-steam-games)
  - [Glossary](#glossary)

## Steam Deck

### Overview and Principles

The Steam Deck is running a usual Linux distribution called [Arch Linux](https://wiki.archlinux.org/title/Gaming). That means, everything in this wiki should equally apply to playing cracked games on the Steam Deck. Take your time and read at least through the following section and the linked article, as it explains all the basics about gaming on Linux. If you're interested in an overview of the hardware of the Deck, here is a very thorough [guide for the Steam Deck](https://github.com/mikeroyal/Steam-Deck-Guide).

 In the interest of keeping things as simple as possible - that is, using the least software necessary to get a game running - Steam is the preferred method for installation for Non-Steam games in the majority of situations. This Wiki page follows that principle of using Steam as a first option for game installation, and other launchers according to preference.

<hr>

### Getting Started With Non-Steam Games - Game Launchers
___________________

#### Game Launchers

##### **• What is a Game Launcher?**

A game launcher allows you to gather and manage (install, configure and launch) all your games acquired from any source, in a single interface. The default launcher for the Steam Deck is Steam - the Steam launcher is the interface you see when you boot the Steam Deck. 

The game launcher is the central hub from which you will run all games, and is integral to running games on the Steam Deck.

##### **• Which Game Launcher Should I Use?**

Essentially, there is no "right or wrong" launcher to use. Many times, it comes down to preference. However, as stated in the Overview and Principles section of this Wiki, we tend to recommend using Steam's launcher (the one that is built into the Deck and helps launch games from the main screen) - whenever possible - in the interest of installing the least amount of software. 

When asking yourself “What should I use to install my games - Steam, Lutris, Bottles…?” start off by looking at this flow chart to make your launcher decision:

If, after looking at this chart and following this guide, you don’t find a solution. Please feel free to ask a question in the sub.    

<hr>

### **• TL;DR**

Try and install your game through Steam, if that doesn't work (or if you prefer something else), try Lutris or Bottles. If you're wanting to install a legitimate Epic Games game, try installing through Heroic Launcher. 

<hr>

##### **• Pros and Cons of Different Launchers / Most Used Launchers** 

###### **Steam**

|Pros|Cons|
|:--------:|:-------:|
|Streamlines all games to run through the main launcher of the Deck, Steam. |Accessing the wine prefix for each game can be difficult compared to other launchers.| 
| Uses Gamescope without any extra commands, allowing you to use frame limiting options and FSR natively with the Deck’s menu.| Enabling custom, per-game settings is less convenient than other launchers.|
| Requires no extra software to run most games.| SteamOS on the deck sometimes struggles with games that need multiple windows open at once (i.e. a multiplayer game that needs a separate game matching software running in the background).|    


###### **Lutris**

|Pros|Cons|
|:--------:|:-------:|
|Attractive UI| Requires extra software to be installed other than Steam|
|Creates easy to find wine prefix folders| Can be overwhelming for a beginner due to the amount per-game setting options|
|Allows for easy manipulation of per-game settings| Isn’t integrated into SteamOS|
|Allows for easy installation of game dependencies| Requires extra steps to get working with Steam’s built in Gamescope/FSR|
|Has its own version of Wine that can be useful in edge cases|
|Allows you to connect legitimate accounts (such as Epic Game Store, GoG, etc) to install those games directly|


###### **Bottles**

|Pros|Cons|
|:--------:|:-------:|
|Creates easy to find wine prefix folders| Plain UI|
|Allows for easy manipulation of per-game settings| Requires extra software to be installed other than Steam |
|Allows for easy installation of game dependencies| Can be overwhelming for a beginner due to the amount per-game setting options |
|Has its own version of Wine that can be useful in edge cases| Isn’t integrated into SteamOS|
|Specializes in running Windows programs other than games as well| Requires extra steps to get working with Steam’s built in Gamescope/FSR|

<hr>

##### **• Other Launchers**

###### **Heroic Launcher**

|Pros|Cons|
|:--------:|:-------:|
|Attractive UI| Does NOT allow for the installation of non-Steam games other than through legitimately connected accounts| 
|Creates easy to find wine prefix folders| Requirers extra steps to get working with Steam’s built in Gamescope/FSR|
|Allows for easy manipulation of per-game settings|
|Allows for easy installation of game dependencies|
|Runs legitimate Epic Game Store particularly well| 
|Allows you to connect legitimate accounts (such as Epic Game Store and GoG) to install those games directly| 

<hr>

### Proton and Wine

<hr>

#### **• TL;DR**

Proton and Wine help Windows games/programs to run on Linux. Use Proton when launching games through Steam and Wine with other launchers.  

<hr>

#### **• What are Wine and Proton 'Runners'?**

* **Runners** - Runners are the components that are needed to run a Windows game on Linux. Wine, Proton and all of their variants are considered runners.

* **Wine** - Wine is what is known as a compatibility layer which allows enables Windows programs to run on Linux, which the Steam Deck is built on. Wine can run Windows applications as well as video games. 

* **Proton** - Proton is the version of Wine that Valve (the company behind the Steam Deck) created in order to create a version that more specifically caters to running video games.     

##### **• What are Proton-GE, Wine-GE, Lutris-GE, and Caffe?**

* **Proton-GE** -  A custom version of Proton with gaming related patches created by developer GloriousEggroll. This is only intended to used with Steam as a launcher. 

* **Wine-GE** - A custom version of Wine that is also made by GloriousEggroll. It contains fixes like Proton-GE, but is intended to be used when **not** using Steam to launch games.

* **Lutris-GE** - Essentially the same as Wine-GE, but modified for Lutris.

* **Caffe** - The official Wine implementation for Bottles. 

#### **• Should I be using Proton/Proton-GE or Wine-GE for my games?**

[There is a longer explanations to be had about this](https://www.reddit.com/r/linux_gaming/comments/uzrz2k/a_thread_about_using_protonge_and_winege_builds/), but the simple answer is: Use Proton/Proton-GE on games running through Steam, and Wine-GE when using other launchers like Lutris, Bottles, or Heroic. 

##### **• Should I be using Proton, Proton Experimental, or Proton-GE for my Steam game?**

In general, using the most up-to-date Proton-GE is recommended as it includes the latest fixes for new games and is updated more often than Steam's Proton Experimental build (which, itself, is more up-to-date than the numbered versions of Proton - i.e. Proton 7, etc...). [See the LinuxCrackSupport's FAQ for more information about this specific build](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_1.1.3_what_is_proton-ge.3F).

Be aware that a specific build might be more appropriate for a specific game. Therefore the general procedure should be: 

  1. Try the newest Proton-GE build

  2. If Proton-GE doesn't work, look up on [protondb.com](https://www.protondb.com/) any user reports for the game you're trying and see if they mention a specific build of Proton to use. 

<hr>

# Getting Started With Non-Steam Games - Installing Non-Steam Games

<hr>

## A). Step 1: Updating Proton / Wine

The first step before you install games should be to update your Proton/Wine versions (that is, Proton-GE/Wine-GE). This is done to ensure that you have the latest version of Proton and Wine which often bring fixes for many games. 

*NOTE: Updating to the latest version of Proton (especially non-official builds like Proton-GE or Wine-GE), while nearly always recommended, can be a double-edged sword in the sense that these new builds may bring regressions. As noted in the previous section (Should I be using Proton, Proton Experimental, or Proton-GE for my Steam game?) you should still be using the latest Proton-GE with Steam, and if that doesn't work, look up your game on protondb.com to see which version of Proton best works with the game.* 

<hr>

###  **• TL;DR**

 Download ProtonUp-Qt from the Discover Store on the Steam Deck's desktop environment and install the latest version of Proton-GE / Wine-GE for your desired launcher. 
 
<hr>

### **• Installing Different Proton / Wine Versions Using ProtonUp-Qt**

1. [Put the Steam Deck into Desktop Mode](https://www.digitaltrends.com/computing/how-to-use-desktop-mode-on-the-steam-deck/#:~:text=Step%201%3A%20Turn%20your%20Steam,now%20technically%20in%20Desktop%20Mode.). 

2. Open the Discover App store, search for ProtonUp-Qt (Or [click this link](https://flathub.org/apps/details/net.davidotek.pupgui2) and hit install), and install it. 

3. Open the app and you'll be presented with with the interface that looks like [this](https://user-images.githubusercontent.com/54072917/142935052-5d627e22-dc1a-4d31-9189-288b41022534.png). 

  Here is where we can select which program we want to install a different Wine version to using the dropdown menu at the top. It defaults to Steam, but has options for Lutris and Heroic Launcher if you've got those installed.  

4. After selecting what program you want to install the custom Wine version to using the dropdown menu mentioned above, click the "Add Version" button in the bottom right. 

5. [This screen](https://raw.githubusercontent.com/DavidoTek/ProtonUp-Qt/main/.github/images/pupgui2-dark.png) will appear and you'll be presented with two options: 

    **Compatability Tools** - this allows you to select the custom Wine versions such as Proton-GE and more. 

    **Version** -  this allows you to select the version of the custom Wine build that you're about to install.

6. Select the "Compatibility Tools" option you want (this will default to Pronton-GE which is the most commonly installed) and the "Version" (it will default to the latest version for each Wine build) and click install. 

7. Now you can delete the previous build of your custom Wine build by selecting it and click "Remove Selected" if you no longer have any games using the previous version. 

 *Note: It will warn you if you do have games assigned to the selected version, though you can delete the previous build anyway, despite it being used. Any games that were using the previous version that you deleted will have to be manually changed to the new version in Steam under Compatibility Settings.*

<hr>

## B). Step 2: Installing Non-Steam Games

<hr>

#### **• Installing Non-Steam Games Through Steam**

This section shows you how to install games - including repacks - through Steam directly.   

<hr>

#####  **• TL;DR**

###### **• Installing using an Installer (Including Repacks)**

1. Add the game's installer as a non-Steam game
2. Add ``` STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1``` in the Launch Command section for the installer on Steam if your game will be installed on the SD card
3. Set the compatibility tool to use the latest Proton-GE for the game's installer
4. Install the game
5. After installation, add the main exe file of your game as a non-Steam game
6. Set the compatibility tool to use the latest Proton-GE for the game you installed 
7. If your game was installed to your SD card, add ```STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1``` to the Launch Options box in the General settings of the game. 

###### **• Installing A "Portable"/"Preinstalled"/"Clean Steam Files" Game**

1. Add the game's executable as a non-Steam game
2. Add ``` STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1``` in the Launch Command section for the installer on Steam if your game will be installed on the SD card
3. Set the compatibility tool to use the latest Proton-GE for the game's executable 
4. Play the game

<hr>

##### **• Installing using an Installer (Including Repacks)**
 
1. [Put the Steam Deck into Desktop Mode](https://www.digitaltrends.com/computing/how-to-use-desktop-mode-on-the-steam-deck/#:~:text=Step%201%3A%20Turn%20your%20Steam,now%20technically%20in%20Desktop%20Mode.) 

2. Open Steam

3. Under "Games", [click "Add a Non-Steam Game to my Library"](https://i.ytimg.com/vi/3IGWCgot5ko/maxresdefault.jpg)

4. [This screen](https://i.imgur.com/lRaTGW5.png) will appear -  click "Browse" and locate your game's installer

  *Note: ```/run/media/mmcblk0p1``` is the default location of the SD card on the Deck.*  

5.  Once your game installer's exe is selected, you'll see it will [show a check mark by the program](https://i.imgur.com/lRaTGW5.png). Click "Add Selected Programs" to add it to Steam.

6. [Find the installer that you've added in the list of games on Steam, right click it, and click "Properties"](https://i.imgur.com/skXzM1w.png)

7. [Within Properties, there will be a tab called "Compatibility". Click that tab and set the tool to force the use of the compatibility tool, selecting your latest Proton-GE build](https://i.imgur.com/xgh2Yzt.png)   

8. Run your installer and let it finish (remember, ```/run/media/mmcblk0p1``` is the default location of the SD card on the Deck. if you need to install your game to a folder there)

9. [Once the installer finishes - in your game list on Steam, right click the INSTALLER that you added first, navigate to "Manage", and click "Remove non-Steam game from your library" to remove the installer that you will no longer need.](https://i.imgur.com/S7UuBaH.jpg)

10. Now add the main executable file of your game (found somewhere in the folder that you installed your game to) as a non-Steam game by repeating steps 3-5 of this section of the guide 

11. Set the compatibility tool to use the latest Proton-GE for the game executable that you just added by repeating step 7 of this section of the guide

12. **If your game was installed to your SD card**: [Find the game's executable that you've just added in the list of games on Steam, right click it, and click "Properties", then navigate to the General tab's Launch options](https://i.imgur.com/07DLot7.png). Under the "Launch Options" box, add ```STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1```

13. Run the game  

<hr>

##### **• Installing A "Portable"/"Preinstalled"/"Clean Steam Files" Game**

This section of the guide is for games that come pre-installed in a folder - these games are usually "unpacked" into a folder and you're able to run the bare exe file of the game. 
 
1. [Put the Steam Deck into Desktop Mode](https://www.digitaltrends.com/computing/how-to-use-desktop-mode-on-the-steam-deck/#:~:text=Step%201%3A%20Turn%20your%20Steam,now%20technically%20in%20Desktop%20Mode.) 

2. Open Steam

3. Under "Games", [click "Add a Non-Steam Game to my Library"](https://i.ytimg.com/vi/3IGWCgot5ko/maxresdefault.jpg)

4. [This screen](https://i.imgur.com/lRaTGW5.png) will appear -  click "Browse" and locate your game's main executable file. This will differ from game to game. 

  *Note: ```/run/media/mmcblk0p1``` is the default location of the SD card on the Deck.*  

5.  Once your game's exe is selected, you'll see it will [show a check mark by the program](https://i.imgur.com/lRaTGW5.png). Click "Add Selected Programs" to add it to Steam.

6. [Find the executable that you've added in the list of games on Steam, right click it, and click "Properties"](https://i.imgur.com/skXzM1w.png)

7. [Within Properties, there will be a tab called "Compatibility". Click that tab and set the tool to force the use of the compatibility tool, selecting your latest Proton-GE build](https://i.imgur.com/xgh2Yzt.png)   

8. **If your game was installed to your SD card**: [Find the game's executable that you've just added in the list of games on Steam, right click it, and click "Properties", then navigate to the General tab](https://i.imgur.com/07DLot7.png). Under the "Launch Options" box, add ```STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1``` 

9. Run your game. 

<hr>

#### **• Installing Non-Steam Games Through Lutris**

This section shows you how to install games - including repacks - through Lutris. If you have any difficulties installing Lutris on the Steam Deck, please take a look at [this post on how to install Lutris](https://www.reddit.com/r/LinuxCrackSupport/comments/tnnq24/how_to_install_lutris_on_steam_deck/) and leave some feedback.
     
<hr>

#####  **• TL;DR**

###### Installing a Game on Lutris from an Installer File
1. In Lutris, click the "+" symbol in the top left to add a new game
2. [From the "Add games to Lutris" popup, choose "Install a Windows game from media"](https://i.imgur.com/kUsBmVJ.png) 
3. 
_____________________


<hr>

# Getting Started with Steam Games - Dependencies

<hr>

### A) About Dependencies

<hr>

#### **• What are Dependencies?**

* A software dependency is when when one piece of software depends on another to run correctly. Thus, the games are "dependent" on that separate software. 

* Dependencies are also known as Redistributables 

* For example, some games that run on Windows are dependent on Microsoft's Visual C++ Redistributable Packages, and because the games uses those packages to run, they must be installed before the games can run. 

* Sometimes dependencies are added to game installers in order to make sure your computer has the right software to run the game. 

* Some games are "self contained" in that all of the files needed to run the game are located within the game's folder once installed. Most games, however, rely on dependencies that are located outside of this folder.  

<hr>

#### **• What Dependencies Does My Game Need?**

##### **• Common Dependencies**

###### **• Windows Dependencies**

- **Microsoft Visual C++** - Visual C++ is a code compiler for the C programming language family. Many applications are written in C rely on this set of software libraries and can't run without it.

- **DirectX** - DirectX is a group of multimedia software that is required by many Windows games.

- **.NET** - .NET Framework is a software development framework for building and running applications on Windows. 

###### **• Linux Dependencies**

 - **DXVK** - a dependency that converts Microsoft Direct X 11 to Vulkan so that it is useable on Linux. This is included with most Proton/Wine releases so there's generally no need to install it separately. 

 - **VKD3D** - a dependency that converts Microsoft Direct X 12 to Vulkan so that it is useable on Linux. This is included with most Proton/Wine releases so there's generally no need to install it separately. 

_______________________

##### **• Using Steamdb.info to Determine Dependencies**

1. Navigate to [steamdb.info](https://steamdb.info/)
2. In the top right of the page, click the magnifying glass to search for your game 
3. [After you find your game, scroll down and click the "Depots" tab](https://i.imgur.com/3vwwqpE.png). 
4. Here we can see the that for this game - God of War - there are two depots associated with it: *"228988 - 27.86 MiB - Shared Install Depot from 228980"* and *"1593501 - 64.24 GiB"*, which will require us to dig a little deeper to find the dependencies. 

 **Note**: Some games, such as Cyberpunk 2077, [immediately show the dependencies as seen here](https://i.imgur.com/yZ8TIQl.png) ("VC 2019 Redist" aka Microsoft Visual C++ 2019). Each game displays the dependencies differently. 

5. In this case, click the "228988" depot - you typically the smaller one listed, as the other depot ("1593501") includes the main game files which are much larger. Remember, dependencies are adjunct software that is typically included with the game installer, so it will always be smaller than the game itself. 

6. [The page for the depot will display, so scroll down to the "Files" portion to see the the names of the dependencies you will need.](https://i.imgur.com/tDWlso7.png). In this case we have "VC_redist.x64.exe" and "VC_redist.x86.exe" which are two versions of the common dependency Microsoft Visual C++ 2019. 		


_________________

### B) Installing Dependencies

Many games will require dependencies be installed after the main game is installed. Here we've listed two ways of installing them: using Winetricks/Protontricks and manually. 

Because Winetricks/Protontricks does the easy work for you, we recommend trying it first. There will be cases, however, when those programs do not work and you will need to install them manually.     

#### **• Installing Dependencies Using Winetricks / Protontricks**

##### **• What are Winetricks / Protontricks?**

**• Winetricks** - Winetricks is program that runs scripts that can do many things, including install dependencies, change settings for the Wine folder, and more. It is used for game launchers *other* than Steam. 

**• Protontricks** - Protontricks is a version of Winetricks specifically used for Steam / Proton games. It is used for Steam's game launcher only.
 
#### **• Manually Installing Dependencies**

##### **• Manually Installing Via Steam**

1. Go to [this website](https://docs.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170) and download both the x86 and x64 version of the redistributable. 

2. Open the location of your compatdata folder which the default location is: /home/deck/.steam/steam/steamapps/compatdata

3. Sort this folder by last created. THIS IS VERY IMPORTANT TO KEEP TRACK OF THE LATEST FOLDERS FOR THE PURPOSES OF THIS GUIDE. 

4. Add both of the installers that you downloaded as non-Steam games on Steam and install them. 

5. Go back to that folder and sort again by last created and write down the path of the two folders that were just created for the installers. THIS IS SUPER IMPORTANT, KEEP TRACK OF THESE - YOU WILL USE THEM OVER AND OVER AGAIN FOR OTHER GAMES. 

6. Go to Steam and add the following launch commands to the game executable that was giving you the error (all in one line, all with one space between them): 

        STEAM_COMPAT_MOUNTS=/run/media/mmcblk0p1 STEAM_COMPAT_DATA_PATH=(path to your first folder) STEAM_COMPAT_DATA_PATH=(path to your second folder) %command%

7. Run the game, it should work now. 

  Note: you have to do these exact commands with many games that require these redistributables, except the DXVK command isn't necessary for other games, just makes Days Gone work better.

##### **• Manually Installing Via Lutris**

##### **• Manually Installing Via Bottles**

______________________________

# Getting Started With Non-Steam Games - Assigning Box Art in Steam

<hr>

# 6) Common Errors and How to Solve Them

## **• "Failed to open game.uproject"** 

This error is due to the fact that the game can't see the dependencies - namely Microsoft Visual C++ Redistributable. Install is using [this section](https://www.reddit.com/r/LinuxCrackSupport/wiki/edit/index/steamdeck#wiki_.2022_installing_dependencies_using_winetricks_.2F_protontricks) of the guide. 

## **• Steam Controller Isn't Picking Up Inputs for My Game**

## **• DX12 is not Supported on Your System**

<hr>

# 7) F.A.Q.

## **• Controller Profiles for Non-Steam Games**

Here's a [guide](https://www.reddit.com/r/LinuxCrackSupport/comments/vhm6qx/guide_downloading_community_controller_profiles/) on how to use community controller profiles on non-Steam games.

## **• Cloudsync Non-Steam Games**

Here's a short [video guide](https://www.reddit.com/r/LinuxCrackSupport/comments/wpq8p3/cloudsync_for_cracked_games_on_steam_deck/) on how to use cloudsync on your Steam Deck with cracked games.

<hr> 

# 8) Glossary

