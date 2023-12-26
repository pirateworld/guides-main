# Contents
-   [Tips and tricks](#tips-and-tricks)
    -   [Native Linux repacks/releases](#native-linux-repacksreleases)
        -   [Johncena141](#johncena141)
        -   [Linux RuleZ](#linux-rulez)
        -   [Vortex Mod Manager](#vortex-mod-manager)
        -   [Use Proton with Lutris](#use-proton-with-lutris)
        -   [Playing FitGirl repacks](#playing-fitgirl-repacks)
        -   [Steamworks and online fix using Steam Tinker Launch](#steamworks-and-online-fix-using-steam-tinker-launcher)
        -   [Blocking Internet for games](#blocking-internet-for-games)
        -   [Tools, tweaks and miscellaneous](#tools-tweaks-and-miscellaneous)

# Tips and tricks

## Native Linux repacks/releases

There's a [dedicated post](https://www.reddit.com/r/LinuxCrackSupport/comments/wyy7f7/release_watch_native_linux_games/) for new native Linux releases.

### Johncena141

The group [johncena141](https://github.com/jc141x/jc141-bash/tree/master/setup) offers games including a specific version of Wine and other tweaks to run on Linux out-of-the-box. You can find them on 1337x. (Be aware that the website is changing quite frequently, you'll find the correct website in the latest releases on 1337x.)

Here's a quick [guide](https://www.reddit.com/r/LinuxCrackSupport/comments/vf37oe/guide_to_install_and_play_all_of_johncena141/) on how to install and play johncens141's releases.

There's also [a GUI](https://www.reddit.com/r/LinuxCrackSupport/comments/vid4fz/gui_for_johncena141_repacks/) to download, manage and play Johncena141's repacks.

There are also some Linux builds for games on RuTracker (thanks u/iamnotstanley).

### Linux RuleZ

There are native repacks/releases by Linux RuleZ to be found on Zamuda and Torrminatorr ([related post](https://www.reddit.com/r/LinuxCrackSupport/comments/vthdb6/linux_repacker_linux_rules/)).

## Vortex Mod Manager

It is possible to use the Vortex Mod Manager on Linux through a [Lutris install script](https://lutris.net/games/vortex-mod-manager/) as explained in [this video](https://www.youtube.com/watch?v=MDr7L-XRd54).
Another possible solution is to use a virtual machine according to [this post](https://www.reddit.com/r/LinuxCrackSupport/comments/tjz4b7/you_can_use_virtualbox_share_your_game_folder/).

It's also possible to install it using [Steam Tinker Launch](https://github.com/frostworx/steamtinkerlaunch#steam-tinker-launch).

## Use Proton with Lutris

Some games will only run using Proton, which is obviously not possible when you try to play a cracked game via Lutris. Luckily, it's fairly easy to use Proton with Lutris, by either using Steam or getting it from Github directly.

1. Get Proton, either using [Steam](https://segmentnext.com/2018/12/06/steam-proton-guide/) or by downloading it from [Github](https://github.com/ValveSoftware/Proton). Some distros offer Proton in their repositories, for example it's available on Arch Linux in the [AUR](https://aur.archlinux.org/packages/proton/).
2. Locate the installation directory of Proton. If you installed it through Steam it's one of the following. `~/.steam/steam/steamapps/common/Proton
~/.local/share/Steam/steamapps/common/Proton`
If you have downloaded Proton manually, navigate to the directory where you have saved it or where you installed it without Steam.
3. Inside the directory you'll find a folder called `dist` (or `files`) it should contain the subfolders `bin`, `lib`, `lib32`, `share`, which contains the files we need for Lutris. Check the following directory, where the runners of Lutris are located: `~/.local/share/lutris/runners/wine/`
4. Create a folder in that directory with the name of the respective Proton version, e. g. *Proton-5.13* or *Proton-Experimental*. If you have simply downloaded Proton, simply copy the respective files into that directory and skip the next step.
5. Now we create a softlink from the folder we just created, that's pointing to the `dist` (or `files`) folder.
`ln -s ~/.steam/steam/steamapps/common/Proton/dist/* ~/.local/share/lutris/runners/wine/Proton/`
or
`ln -s ~/.steam/steam/steamapps/common/Proton/files/* ~/.local/share/lutris/runners/wine/Proton/`
6. Now there should be the content of the `dist` folder inside the `Proton` folder, you've just created. Start Lutris (or restart it, if it's open) and select a game, go to *Configure -> Runner options -> Wine version* and select *Proton*.
7. Save everything and start the game!

*The popular [Proton build by Glorious Eggroll](https://github.com/GloriousEggroll/proton-ge-custom#1-running-non-steam-games-with-proton-outside-of-steam-is-not-supported-do-not-ask-for-help-with-this) does [not support to be used with Lutris](https://github.com/GloriousEggroll/proton-ge-custom#1-running-non-steam-games-with-proton-outside-of-steam-is-not-supported-do-not-ask-for-help-with-this) and could potentially break your things.*
*If you want to use Proton outside of Steam, Glorious Eggroll provides a [Wine build for the use with Lutris](https://github.com/gloriouseggroll/wine-ge-custom) etc.*

## Playing FitGirl repacks

When you have an error during installation, take a look at [this section](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_3.2.2_installing_repacks_return_error).

* u/TermoZour [mentioned](https://www.reddit.com/r/LinuxCrackSupport/comments/mfdjrk/welcome_to_linux_crack_support/gsnjbai) to add tips on how to play FitGirl repacks on Linux and for now it seems like this is simply possible by running them [using Proton](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_playing_fitgirl_repacks_using_lutris_and_proton).
* Another solution would be to use this [script](https://github.com/Francesco149/protonfit), which I haven't tested for now and which isn't maintained anymore.
* [Here's another short tutorial](https://www.reddit.com/r/LinuxCrackSupport/comments/pwevxf/installing_fitgirl_repacks_on_linux_through/).
* [And yet another tutorial](https://www.reddit.com/r/LinuxCrackSupport/comments/ru6vem/yet_another_guide_on_how_to_install_fitgirl/)
* [Here's a guide for installing FitGirl repacks on the Steam Deck](https://www.reddit.com/r/LinuxCrackSupport/comments/wkdblj/how_to_install_fitgirl_repacks_on_steamdeck/)

### Steamworks and online fix using Steam Tinker Launch

Here's [a quick guide](https://www.reddit.com/r/LinuxCrackSupport/comments/tqjp3z/guide_running_steamworks_fixonline_fix_with_linux/) on how to run a Steamworks and online fix using [Steam Tinker Launch](https://github.com/frostworx/steamtinkerlaunch#steam-tinker-launch) and Proton.

## Blocking internet for games

[Here](https://www.reddit.com/r/LinuxCrackSupport/comments/wk6s4q/strategies_for_blocking_internet_on_cracked_games/) is a guide for blocking internet on cracked games.

## Tools, tweaks and miscellaneous

* [Proton GE](https://github.com/GloriousEggroll/proton-ge-custom) \- special build of Proton with various patches and fixes included. (Here's a [great article](https://linuxgamingcentral.com/posts/proton_ge_tutorial/) about it.)
* [ProtonUp](https://github.com/AUNaseef/protonup) and [ProtonUp-Qt](https://github.com/DavidoTek/ProtonUp-Qt) for easy installation of Proton GE.
* [Protonutils](https://github.com/nning/protonutils) a CLI-tool for managing you Proton versions.
* [VKD3D-Proton](https://github.com/HansKristian-Work/vkd3d-proton) \- VKD3D-Proton is a fork of VKD3D, which aims to implement the full Direct3D 12 API on top of Vulkan.
* [Winetricks](https://wiki.winehq.org/Winetricks)
* [Wine GE](https://github.com/GloriousEggroll/wine-ge-custom) \- a special build for use with Lutris.
* [wine-tkg](https://github.com/Tk-Glitch/wine-tkg), [proton-tkg](https://github.com/Frogging-Family/wine-tkg-git/tree/master/proton-tkg) and [wine-proton-tkg](https://github.com/Tk-Glitch/wine-proton-tkg) \- Wine-tkg is a build-system aiming at easier custom wine builds creation.
* [Tk-Glitch](https://github.com/Tk-Glitch) and [Frogging Family's](https://github.com/Frogging-Family) work in general.

* [Steam Tinker Launch](https://github.com/frostworx/steamtinkerlaunch#steam-tinker-launch) is a "tool for use with the Steam client which allows customizing and start tools and options for games quickly".
* [LibreGaming](https://github.com/Ahmed-Al-Balochi/LibreGaming#libregaming) for downloading distro-specific dependencies for gaming.
* [Chad Launcher](https://gitlab.com/Gnurur/chad_launcher#chad-launcher) for launching pirated games (discontinued).
* [Rum](https://johncena141.eu.org:8141/johncena141/rum/src/branch/master/README.md) is the successor of Chad launcher.

* [DXVK](https://github.com/doitsujin/dxvk) \- DirectX 9, 10 and 11 implementation using [Vulkan](https://en.wikipedia.org/wiki/Vulkan_(API).
* [dxvk-tools](https://github.com/Frogging-Family/dxvk-tools) \- DXVK & vkd3d-proton script to build/patch/install/update, Lutris and Proton-tkg compatible.
* [DXUP](https://github.com/Joshua-Ashton/dxup) \- A D3D9 and D3D10 -> D3D11 translation layer (archived!).
* [VKD3D](https://github.com/d3d12/vkd3d) \- The VKD3D 3D Graphics Library using a similar API to Direct3D 12.
* ...
