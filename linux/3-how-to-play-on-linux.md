# Contents
-	[Using Steam](#using-steam)
	-	[Steam's wineprefix directory](#steams-wineprefix-directory)
	-	[Goldberg achievement emulator](#goldberg-achievement-emulator)
-	[Using Lutris](#using-lutris)
	-	[Lutris' wineprefix directory](#lutris-wineprefix-directory)
	-	[Using custom DXVK in Lutris](#using-custom-dxvk-in-lutris)
	-	[Installing repacks return error](#installing-repacks-return-error)

# How To Play On Linux

Here is a [introductory article](https://www.pcmag.com/how-to/how-to-play-pc-games-on-linux) about using Steam with Proton and Lutris to play games on Linux.

## Using Steam

You can also add a non-Steam game to Steam and then play it on Linux using Proton. Follow these steps to do so. *This also applies to the Steam Deck!*

1. Open Steam and make sure that *Steam Play* is activated. 
2. Click on "*Steam*" in the top left, click on "*Preferences*" and "*Steam Play*" at the bottom.
3. There tick both the box "*Enable Steam Play for supported titles*" and "*Enable Steam Play for all other titles*".
4. Choose the latest Proton version for "*Run other titles with:*".
5. Close the windows and return to Steam.
6. In the bottom left click on "*+ Add a game*" and then on "*Add a Non-Steam Game...*".
7. In the new window click on "*Browse...*".
8. On the bottom select "*File type: All Files*".
9. Browse to the directory in which your game is saved.
10. Select the game's executable e. g. *game-launcher.exe*".
11. Click "*Open*" and then "*Add selected programs*".
12. The game is now in your Steam library.
13. Right-click the game and select "*Properties...*".
14. Check that "*Target*" contains the path **and** the game's executable. This might not be visible on Steam Deck, in that case copy the path from a file browser (like Dolphin) and paste it into the field. Make sure to include quotation marks, e. g. `/home/arjab/games/Elden Ring/eldenring.exe`.
15. Check that "*Start in*" contains **only** the path from the previous section, but **not** the executable, e. g. `/home/arjab/games/Elden Ring/`.
16. Check that "*Launch options*" is empty if not specified otherwise.
17. Close the window, it saves automatically.
18. Hit the "*Play*"-button. Enjoy!

That's it.

19. If the game doesn't run, open "*Properties...*" again.
20. On the left, switch to the section "*Compatibility*".
21. Tick the box "*Force the use of a specific Steam Play compatibility tool*".
21. Choose a different Proton version or a custom version like [Proton by Glorious Eggroll](https://github.com/GloriousEggroll/proton-ge-custom#installation).
22. Close the window and start the game.

### Steam's wineprefix directory

Steam saves a [wineprefix](https://wiki.archlinux.org/title/Wine#WINEPREFIX) for every game in the following directory:
`/home/$user/.steam/steam/steamapps/compatdata/$appid/pfx/`

Replace $user with your username and $appid with Steam's application ID for the game. You can find the app ID by right-clicking on the game and selecting "*Properties...*". Than switch to the tab "*Updates*" on the left and you will see for example "*App ID: 1234567*" at the bottom.

The above path is a link to the actual path, which can be found in `/home/$user/.local/share/Steam/...`.

### Goldberg achievement emulator

[Here](https://www.reddit.com/r/LinuxCrackSupport/comments/wl55ps/guide_for_using_the_new_achievement_capabilities/) is a guide for using the achievement capabilities of Goldberg Steam emu.

## Using Lutris

Follow these steps to play a cracked game using Lutris:

*It's not necessary to install a game using Lutris as described here. But for some (cracked) games it works better or as described below is necessary insofar as you need a different runner for e. g. the [installation of FitGirl repacks](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_playing_fitgirl_repacks_using_lutris_and_proton). So if you have an already installed game, skip steps 6 to 12.*

1. Obtain your desired game from a respected source.
2. Install Lutris and open it.
3. Click on to top left "+"-button to add a game.
4. Enter the name of the game and select the Runner "Wine".
5. Change to the tab "Game options".
6. *Click on the top right button "Browse.." to select the game's executable.*
7. *Browse to the directory of your downloaded game and select the installer's *.exe.*
8. *Click "Save", you'll see your game's installation has been added to Lutris.*
9. *Double-click on it or use the bottom-left button "Play".*
10. *The installation should start, follow the on-screen instructions.*
11. *After the installation is done, right-click the game in Lutris and click "Configure".*
12. *Go to "Game options" and click the top right button "Browse..".*
13. Browse to the directory in which you've installed the game.
14. Select the game's executable and click the bottom right "Save".
15. Double-click the game in Lutris to start it or use the bottom left button "Play".

*Optional: If a game doesn't work or has poor performance, click "Configure" on the game and tick the bottom left box "Show advanced options". Now you can edit the game's options, [change the runner](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_use_proton_with_lutris), etc.*

Here's also a [guide](https://www.reddit.com/r/LinuxCrackSupport/comments/wik3qi/foolproof_lutris_wine_guide_on_steam_deck/) on how to use Lutris and Wine on the Deck.

### Lutris' wineprefix directory

Lutris uses the default [wineprefix](https://wiki.archlinux.org/title/Wine#WINEPREFIX) for all games which is located in "*/home/$user/.wine*". Sometimes it's necessary to create a new wineprefix and point to it in the game's Lutris configuration.

### Using custom DXVK in Lutris

Lutris uses it's own [fork](https://github.com/lutris/dxvk) of [DXVK](https://github.com/doitsujin/dxvk), but you can also use a custom version of DXVK with Lutris.

Simply install DXVK for example downloading the latest [release](https://github.com/doitsujin/dxvk/releases/) or by installing the [AUR package](https://aur.archlinux.org/packages/dxvk-bin) and copy or [symlink](https://kb.iu.edu/d/abbe) it to the following directory:

`~/.local/share/lutris/runtime/dxvk/custom`

You can name the `custom`directory anything you want, but it must contain the "*x64*" and "*x86*" folders. Now open any game's configuration in Lutris, chek the "*Show advanced options*" box and type the folders name into the "*DXVK version*" field.

Here's the official [tutorial](https://github.com/lutris/docs/blob/master/HowToDXVK.md#d9vk-and-custom-dxvk) by Lutris including a [video](https://www.youtube.com/watch?v=X6Vk_J3p2KA).

The same can be done for [VKD3D](https://wiki.winehq.org/Vkd3d), but Lutris already uses a [fork](https://github.com/lutris/vkd3d) of [VKD3D-Proton](https://github.com/HansKristian-Work/vkd3d-proton).

### Installing repacks return error

Thanks to u/hackedyak there is an [easy fix](https://www.reddit.com/r/LinuxCrackSupport/comments/tirarp/psa_when_installing_repacks_with_custom_wine/) for failing repack installations related to `isdone.dll` or `unarc.dll`..

1. When you run the installation using Lutris, right-click on the game in Lutris and select "*Configure*".
2. Select the right-most tab called "System options".
3. Scroll down to "*Environment variables*".
4. Click the "*Add*"-button on the bottom right.
5. Click into the field labeled "*Key*" and enter the following:

`WINE_LARGE_ADDRESS_AWARE` - if you're using a Wine/Lutris runner.

`PROTON_LARGE_ADDRESS_AWARE` - if you're using a Proton runner.

More on the installation of FitGirl repacks can be found [here](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_6.4_playing_fitgirl_repacks_using_lutris_and_proton).

6. Now click into the field labeled "*Value*" and enter `0`.
7. Click on "*Save*" in the bottom right and start the installation.

You should **change this back** to `1` after the installation though!
