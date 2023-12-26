<div align="center">

![qBittorrent-logo](/pictures/qBittorrent/qBittorrent-logo.png)

</div>

# Contents
-   [Downloads](#downloads)
-   [Configuration](#configuration)
    -   [Make downloads faster](#make-downloads-faster)
    -   [Install a different qBittorrent theme](#install-a-different-qbittorrent-theme)
-   [Tips and Tricks](#tips-and-tricks)
    -   [How to add torrent files to qBittorrent](#how-to-add-torrent-files-to-qbittorrent)
    -   [How to add magnet links to qBittorrent](#how-to-add-magnet-links-to-qbittorrent)
    -   [Add trackers manually for additional download speed](#add-trackers-manually-for-additional-download-speed)
-   [Why is this important?](#why-is-this-important)
-   [Important things to know while torrenting](#important-things-to-know-while-torrenting)

## Downloads

Windows/Mac: <https://www.qbittorrent.org/>

Linux: <https://flathub.org/apps/details/org.qbittorrent.qBittorrent> (make sure Flatpak is installed)

## Configuration

### Make downloads faster

The default configuration should be fine for most people but these are some major tweaks that you should do/ensure to achieve almost maximum speed.

Head over to the "Connection" section and ensure these settings

<div align="center">
![settings-1](/pictures/qBittorrent/settings-1.jpeg)
</div>

**Note: You don't need to change the Listening Port as it is randomized**

Also, in the BitTorrent section, ensure DHT, PeX and Local Discovery is turned on

<div align="center">
![settings-2.png](/pictures/qBittorrent/settings-2.png)
</div>

 ### Install a different qBittorrent theme

The default user interface of qBittorrent is good but it can be improved.

- There are many themes to choose from but I'll be using `darkstylesheet` theme in this example, you can find a good collection of dark themes in this GitHub repository: <https://github.com/jagannatharjun/qbt-theme>

- Clone the repository and extract it. Now move the required theme to the installation folder of qBittorrent (this is optional I recommend doing this to keep your folders organized and clean)

- Open qBittorrent application and go to Preferences from the Tools tab on the header bar, or simply press `Alt+O` to open it.

- Click on "Use Custom UI Theme", click on the folder button and navigate to the location where your theme is located and select it.

- Click on Apply/OK and restart your qBittorrent client.

<div align="center">
![settings-3](/pictures/qBittorrent/settings-3.png)
</div>

# Tips and Tricks

- If you're downloading a movie, TV show or anime then you should enable "Download in sequential order" and "Download first and last pieces first" in the "Torrents option" dialog box, this will allow you to watch the video while it's downloading

- Here's a voucher for Windscribe that you can use to get 30GB of free bandwidth

```
Windscribe 30GB Voucher
Free Until : Unknown
Key: СВОБОДА
https://windscribe.com/signup
```

## How to add torrent files to qBittorrent

- Download the torrent file
- Open qBittorrent application and go to File from the menu bar, then click on "Add Torrent file", or simply press `Ctrl + O` to open it.
- Navigate to the torrent file and start downloading

## How to add magnet links to qBittorrent

- Copy the magnet link
- Open qBittorrent application and go to File from the menu bar, then click on "Add Torrent link", or simply press `Ctrl + Shift + O` to open it.
- Paste the magnet link and click Download.

## Add trackers manually for additional download speed

Sometimes trackers that come by default with the torrent you're trying to download are not providing extra uploaders (seeds), because more seeds = increase in download speed, so to fix this visit this GitHub repository: <https://github.com/ngosang/trackerslist>

- Choose one of the links by clicking on **link**, this will get you into a RAW page of freshly updated trackers, select all and copy.

<div align="center">
![tracker-list](/pictures/qBittorrent/tracker-list.png)
</div>

- Now in qBittorrent highlight your torrent and switch to the **TRACKERS** tab, then click on the empty space and add new trackers, finally paste copied trackers.

<div align="center">
![peers-tab](/pictures/qBittorrent/peers-tab.png)
</div>

- At this point you're done, sometimes qBittorrent does not contact trackers which is not usually recommended, to enable this feature, in qBittorrent click on the above ribbon **Tools -> Advanced -> scroll down until you see "always announce to all trackers in a tier" and enable it.**

- And that's it, the original github repository gets refreshed in a daily basis to provide all active trackers, this method has been proven and recommended by many users of the pirate community.

### **NOTE: This won't work on torrents downloaded from private trackers, this method becomes useless unless using it on public torrents from public trackers.**

# Why is this important?

Torrenting itself is not illegal, downloading of copyrighted content is illegal, when you are downloading using torrents, then your IP address is available to the public through the "Peers tab". What really happens when you get a C&D (Cease and Desist) letter from your ISP (Internet Service Provider) is anti-piracy companies have their employees go through the list of IP Addresses connected to a torrent swarm and send a request to their respective ISPs for shutting them down. The ISPs, in most cases simply issue the torrenters a C&D letter and that's how it ends up in your mailbox. The first 2 or 3 letters are just warnings but they might terminate your internet connection if you keep downloading content even after getting multiple warnings.

However, this can be easily circumvented by using a VPN, whether it is free or paid doesn't really matter when used for the sole purpose of torrenting. Just make sure it's not from some shady VPN company with Chinese associations.

I personally recommend **Mullvad VPN** since it's simply the best. However if you can't afford to pay for a VPN then try out **Windscribe** and **Proton VPN**. They both provide a really nice free trial.
 
# Important things to know while torrenting

Ideally, everyone should go look up references and study how the BitTorrent protocol works, please know this is a P2P network, you are directly connected to another person who has the file you are looking for, no middlemen (servers) are involved.

- **IMPORTANT FOR VPN USERS**: Please enable Killswitch in your VPN client, what this does is terminate the VPN connection immediately if your internet connection fails, this will ensure that you never are connected to the torrent swarm without a VPN.

- You might want to bind your qBittorrent to a VPN, here's a guide on how to do so: <https://redd.it/ssy8vv>

- qBittorrent uses uPnP to open and close ports on your router to find peers, this can be considered a security risk depending on your threat level however it should be fine in most cases, make sure your router has a good password and not "Username: admin, Password: admin", you can open the router settings by going to the address `192.168.0.1` or `192.168.1.1` 

- To verify that qBittorrent is successfully listening to a port, head to <https://canyouseeme.org/> and type out the port number used by qBittorrent which you can find in the "Connections" tab in qBittorrent settings. If you get a message saying "Success", that means you have successfully forwarded a port, if you get an "Error" that means you aren't forwarding the port qBittorrent is listening on. To overcome this you can either change the port number in settings and restart your client, or you can go into your router settings by going to the adress `192.168.0.1` or `192.168.1.1` in your browser, logging in with your router credentials and manually opening a port there.

- Go to <https://canyouseeme.org/> and ensure you don't have any ports open, ignore any manually opened port

- Port Forwarding can provide better speeds in some cases, especially in torrents with a low amount of seeders. This isn't really required in most cases.

- Adding torrent trackers can improve speeds, but please note that some trackers can be malicious, it is advised to stick to the trackers provided by the torrent itself.
