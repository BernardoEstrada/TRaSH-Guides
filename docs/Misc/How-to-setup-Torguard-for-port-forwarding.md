# Setup TorGuard for port forwarding

These are our supported and recommended settings.

If you want to support me, please use this [referral link](https://torguard.net/aff.php?aff=5575){:target="_blank" rel="noopener noreferrer"} and enter the following discount code:

Get 50% Off ALL Plans (Anonymous VPN, Anonymous VPN Pro, Anonymous VPN Premium)

```none
TRaSH-Guides-2024
```

[![torguard-FreeTrial-270x90](images/torguard/torguard-FreeTrial-728x90.gif)](https://torguard.net/aff.php?aff=5575){:target="_blank" rel="noopener noreferrer"}

!!! bug "As of 13 March 2022, Torguard Settles Piracy Lawsuit has agreed to use commercially reasonable efforts to block BitTorrent traffic on its servers in the US using firewall technology. :bangbang:<br><br>I talked to several people, and they can still use Torguard for Torrents, perhaps because the connection is encrypted. Others just selected a server in another country.<br>- [Source Torguard](https://torguard.net/blog/why-torguard-is-blocking-bittorrent-on-us-servers/){:target="_blank" rel="noopener noreferrer"}.<br>- [Source Torrentfreak](https://torrentfreak.com/torguard-settles-piracy-lawsuit-and-agrees-to-block-torrent-traffic-on-u-s-servers-220314/){:target="_blank" rel="noopener noreferrer"}."

!!! warning "If servers in the United States are not working for you, please try another country"

---

## Log in to your Client area

Login to your [Client Area](https://torguard.net/clientarea.php){:target="\_blank" rel="noopener noreferrer"}.

??? success "Example - [Click to show/hide]"

    ![!Client Area Login](images/torguard/client-area-login.png)

### Create a user account

First, we're going to create a [User Account](https://torguard.net/clientarea.php?action=changepw){:target="\_blank" rel="noopener noreferrer"} for your VPN so we won't need to use your main account that you use to login to your account on the Torguard site.
This account will be used to authenticate with your VPN service that your Torrent client will use.

`Services` > `My Services` > `Manage` > `Manage Credentials`

??? success "Example - [Click to show/hide]"

    ![!Services > My Services](images/torguard/services-my-services.png)

    ![!Client Area Manage Credentials](images/torguard/client-area-manage-credentials.png)

Create a new username and choose a secure password, or create a random username and password.

??? success "Example - [Click to show/hide]"

    ![!Create User Account](images/torguard/create_user_account.png)

---

## How to setup Port forwarding

From your `Client Area` dashboard, go to [`My Services`](https://torguard.net/clientarea.php?action=products){:target="\_blank" rel="noopener noreferrer"}.

Then click on `Manage` and select `Port Forward Request`.

`Services` > `My Services` > `Manage` > `Port Forward Request`

??? success "Example - [Click to show/hide]"

    ![!Port Forward Request](images/torguard/req_port_fwd.png)

### Port Forward Request

![!Request New Port Forward WireGuard](images/torguard/request-new-pfw-wireguard.png)

1. Select a country near your location from the drop-down box.
1. Select `UDP`. (:bangbang: **KEEP THIS ON UDP FOR WireGuard** :bangbang:)
1. Select `Port/Auth` and select `WireGuard`.
1. Select the `Protocol` `TCP`.
1. We suggest using a high `Port` number 10000+ or a game port you don't use. Do not use the default torrent ports 6881- 6889
    (This is also the port you will use for your torrent client.)
1. Click on the `+` sign, and do the same with the `UDP` `Protocol`.
1. Then click on `Submit Request`.

!!! warning ":bangbang: DON'T CHANGE OPTION 2 `UDP` to `TCP` :bangbang:"

If everything succeeds, you will see the following.

![status](images/torguard/status.png)

You will also receive an e-mail with the ports you forwarded.

!!! note "Normally, it takes only a short while for the ports to be approved. If it takes longer or you get `PENDING,` we suggest retrying the process."

---

## How to create the config file

From your `Client Area` dashboard, go to your [`Config Generator`](https://torguard.net/tgconf.php?action=vpn-openvpnconfig){:target="\_blank" rel="noopener noreferrer"}.

`Tools` > `Config Generator`

??? success "Example Select Tools > Config Generator - [Click to show/hide]"

    ![!Tools - Config Generator](images/torguard/tools-config-generator.png)

### Config Generator

![!WireGuard Config Generator](images/torguard/config-generator-wireguard.png)

1. Choose `WireGuard`.
1. Choose from the dropdown box the `IP` assigned to you earlier and used for the port forwarding.
1. Add your `VPN Username`.
1. Only change this if you know what you're doing :bangbang:
1. [Optional] Choose your preferred DNS Server
1. Only change this if you know what you're doing :bangbang:
1. Click on `Generate Config`

This will generate a `.conf` file for you to download, named with a random number.

Rename the `.conf` file you just downloaded to `wg0.conf` and copy it to the wireguard folder of your VPN torrent client.

## Torrent client port forwarding setup

Follow the torrent client's guides on how to set up port forwarding.

- [qBittorrent](/Downloaders/qBittorrent/Port-forwarding/){:target="\_blank" rel="noopener noreferrer"}
- [Deluge](/Downloaders/Deluge/Port-Forwarding/){:target="\_blank" rel="noopener noreferrer"}

--8<-- "includes/support.md"
