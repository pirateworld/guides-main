# Contents
-	[Introduction](#introduction)
	-	[The basics of gaming on Linux.](#the-basics-of-gaming-on-linux)
		-	[What is Wine?](#what-is-wine)
		-	[What is Proton?](#what-is-proton)
		-	[What is Proton-GE?](#what-is-proton-ge)

## Introduction

This post is supposed to provide resources regarding gaming on Linux and pirated/cracked games. Since there are subreddits for both of these topics, it will start as a collection of links to existing resources ([see 4.](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_4._useful_resources)). If you feel like anything is missing or wrong, feel free to create a new post discussing the issue.

Sometimes you will see links to [the Arch wiki](https://wiki.archlinux.org/), which is a great resource for Linux in general and not just for Arch Linux, so don't worry.

### The basics of gaming on Linux.

[Here](https://www.reddit.com/r/LinuxCrackSupport/comments/wl4o2q/eli5_terms_used_in_linux_gaming_explanation_for/) is an explanation of some of the main terms used in gaming on Linux, which are also partly explained in the following.

#### What is Wine?

[Wine](https://wiki.archlinux.org/title/Wine) is a compatibility layer that makes it possible to run Windows applications on Linux. It usually creates a so-called [wineprefix](https://wiki.archlinux.org/title/Wine#WINEPREFIX) in your home directory which mimics a Windows-like folder-structure, in which every application is installed. When using default Wine it's advised to install [winetricks](https://wiki.archlinux.org/title/Wine#Winetricks), [DXVK](https://wiki.archlinux.org/title/Wine#DXVK) and [other useful tools](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_6.5_tools.2C_tweaks_and_miscellaneous).

*For Wine-GE take a look at the section about [Proton-GE](https://www.reddit.com/r/LinuxCrackSupport/wiki/index/#wiki_1.1.3_what_is_proton-ge.3F).*

#### What is Proton?

[Proton](https://tinyurl.com/fe5zmz3t) is based on Wine and developed by Valve. It incorporates some libraries, patches and improvements that Wine doesn't, for example it includes [DXVK](https://github.com/doitsujin/dxvk) (a translation layer from [Direct3D](https://en.wikipedia.org/wiki/Direct3D) 9, 10 and 11 to [Vulkan](https://wiki.archlinux.org/title/Vulkan)) and [VKD3D](https://github.com/HansKristian-Work/vkd3d-proton) (a translation layer from Direct3D 12 to Vulkan).

Proton can be used to play Windows games on Linux [using Steam](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_3.1_using_steam), but it can also be [used with Lutris](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_6.3_use_proton_with_lutris).

#### What is Proton-GE?

*[Proton-GE or GE-Proton](https://github.com/GloriousEggroll/proton-ge-custom#overview)* as of late is a fork of Valve's Proton by a developer called *[Glorious Eggroll](https://www.gloriouseggroll.tv/)*. It incorporates even more patches than the original Proton like DXVK patched with Async, [AMD FSR support](https://www.gamingonlinux.com/2021/07/proton-613-ge-1-is-out-now-with-amd-fidelityfx-super-resolution-resizable-bar/) or Protonfixes, which enable more games to be playable on Linux.

GE-Proton is meant for use with Steam. If you want to [use Proton with Lutris](https://www.reddit.com/r/LinuxCrackSupport/wiki/index#wiki_6.3_use_proton_with_lutris), take a look at Glorious Eggroll's [Wine-GE](https://github.com/gloriouseggroll/wine-ge-custom).

Here is also a recent [post by Glorious Eggroll](https://www.reddit.com/r/LinuxCrackSupport/comments/w14fx6/another_protonge_vs_winege_thread/) himself explaining the differences between Proton-GE and Wine-GE.

*Thanks to u/rookielmfao's [post](https://www.reddit.com/r/LinuxCrackSupport/comments/tj80n0/the_definitive_linux_piracy_guidecheatsheet/) for inspiration.*
