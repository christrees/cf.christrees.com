

- Public [http://24.149.22.11/](http://24.149.22.11/) - as of 20230117
  - DMZ Lan [ng.cfu.net - 854G-1 - http://192.168.6.1/](http://192.168.6.1/)
    - [current devices](http://192.168.6.1/#/html/status/status_devicetable.html)
    - [DHCP Reservations](http://192.168.6.1/#/html/advanced/ip/advanced_ip_dhcpreservation.html)
    - [Port Forwarding](http://192.168.6.1/#/html/advanced/security/advanced_security_advancedportforwarding.html)
    - [Firewall Rules](http://192.168.6.1/#/html/advanced/security/advanced_security_firewallsettings.html)
    - [~~ng.cf.lan -  http://192.168.2.1/~~](http://192.168.2.1/) ~~ng network gateway (device ASUS RT-AC87U sb pfSense)~~ removed in May
    - [~~sg.cf.lan -  http://192.168.2.2/~~](http://192.168.2.2/) ~~sg storage gateway (device TrueNAS core)~~ removed in May
    - [~~cg.cf.lan -  http://192.168.2.3/~~](http://192.168.2.3/) ~~cg compute gateway (device Proxmox)~~ removed in May
  - HDHomeRun Connect [HDHR-10802956 4K Dev - Tuner - http://192.168.6.160/](http://192.168.6.160/) DNS MAC Res
    - [http://192.168.6.160/discover.json](http://192.168.6.160/discover.json)
    - [http://192.168.6.160/lineup.json](http://192.168.6.160/lineup.json)
    - [https://api.hdhomerun.com/api/xmltv?DeviceAuth=EB0wFJ8-Bct5BY-ZS8mF5XRO](https://api.hdhomerun.com/api/xmltv?DeviceAuth=EB0wFJ8-Bct5BY-ZS8mF5XRO)
  - Plex Server [cattvWin10 - http://192.168.6.180:32400/](http://192.168.6.180:32400/) DNS MAC Res
  - [DHCP Reservations](http://192.168.6.1/#/html/advanced/ip/advanced_ip_dhcpreservation.html) DHCP Range 192.168.6.150-250
    - 192.168.6.159 - macci - i3 - [ghadmin](What#Time) 
    - 192.168.6.160 - HDHR-10802956 4K Dev see above
    - 192.168.6.161 - zmodo camera
    - 192.168.6.162 - zmodo camera
    - 192.168.6.163 - zmodo camera
    - 192.168.6.164 - zmodo camera
    - 192.168.6.165 - zmodo hub
    - 192.168.6.180 - cattvWin10 - ISP2150 4core - [tvadmin](What#Time)
  - Static IP used in 192.168.6.0/24 subnet
    - 192.168.6.101 - network gport .2 subnet
    - 192.168.6.102 - storage gport .2 subnet
    - 192.168.6.103 - compute gport .2 subnet
      - [http://192.168.6.103/ - nginx proxy default page](http://192.168.6.103/)
      - Proposed mappings
      - [http://192.168.6.103:81 nginx proxy admin]()
      - [http://192.168.6.103:8006 proxmox admin]()
      - [http://192.168.6.103:9000 portainer admin]()
      - [http://192.168.6.103:8006 proxmox admin]()


- [Plex downloads](https://www.plex.tv/media-server-downloads/)
    - Plex 1.28.2 for OSX 10.9
- [ZeroTier downloads](https://www.zerotier.com/download/)
    - [cattv - network - 52b337794f721ef7](https://my.zerotier.com/network/52b337794f721ef7) ghadmin


---

Future video services should be in it's on ns managed subnet

---

ns - Netstack

# Netstack Edge Node

| IP | lan | purpose | ops | setup |
|----|-----|---------|-----|-------|
| [https://192.168.2.1](https://192.168.2.1) | [https://ng.cf.lan](https://ng.cf.lan) | ng - network gateway | [ ng ops ]() | [ng setup](https://netstack.org/docs/lan/network/pfsense/setup) |
| [https://192.168.2.2](https://192.168.2.2) | [https://sg.cf.lan](https://sg.cf.lan) | sg - storage gateway | [ sg ops https://192.168.2.2/ui/dashboard](https://192.168.2.2/ui/dashboard) | [sg setup](https://netstack.org/docs/lan/storage/freenas/setup) |
| [https://192.168.2.3](https://192.168.2.3) | [https://cg.cf.lan](https://cg.cf.lan) | cg - compute gateway | [ cg ops https://192.168.2.3:8006/ ](https://192.168.2.3:8006/) | [cg setup](https://netstack.org/docs/lan/compute/proxmox/) |


Future HA nodes


| IP | lan | purpose |
|----|-----|---------|
| [https://192.168.2.4](https://192.168.2.4) | [https://bg2.cf.lan](https://bg2.cf.lan) | bg - backups gateway secondary|
| [https://192.168.2.5](https://192.168.2.5) | [https://ng2.cf.lan](https://ng2.cf.lan) | ng - network gateway secondary| 
| [https://192.168.2.6](https://192.168.2.6) | [https://sg2.cf.lan](https://sg2.cf.lan) | sg - storage gateway secondary| 
| [https://192.168.2.7](https://192.168.2.7) | [https://cg2.cf.lan](https://cg2.cf.lan) | cg - compute gateway secondary| 
| [https://192.168.2.8](https://192.168.2.8) | [https://bg.cf.lan](https://bg.cf.lan) | bg - backups gateway |
| [https://192.168.2.9](https://192.168.2.9) | [https://dg.cf.lan](https://dg.cf.lan) | dg - documents gateway | 

---

#### Old
- [~~ng.cf.lan - ASUS RT-AC87U - http://192.168.2.1/~~](http://192.168.2.1/) removed in May
  - [Port Forward](http://192.168.2.1/Advanced_VirtualServer_Content.asp)
  - [Port Trigger](http://192.168.2.1/Advanced_PortTrigger_Content.asp)
  - [DMZ](http://192.168.2.1/Advanced_Exposed_Content.asp)
  - [DHCP](http://192.168.2.1/Advanced_DHCP_Content.asp)
  - [tbd]()
  - [tbd]()
- [~~sg.cf.lan - TrueNAS Scale - http://192.168.2.2/~~](http://192.168.2.2/) root What#Time removed in May
  - SMB Share - cfplex - smb://nsadmin@192.168.2.2
  - [tbd]()
  - [tbd]()
  - [tbd]()
- [plex global - https://www.plex.tv/](https://www.plex.tv/)
- [plex on local - http://127.0.0.1:32400/](http://127.0.0.1:32400/)
- [~~plex on admin2cld-win10 - http://192.168.6.15:32400/~~](http://192.168.6.15:32400/) turned off in May 
  - SMB Share - smb://ghadmin@192.168.6.15
- [HDHomeRun Connect 4K Dev - Tuner - http://192.168.2.31/](http://192.168.2.31/)
  - [http://192.168.2.31/discover.json](http://192.168.2.31/discover.json)
  - [http://192.168.2.31/lineup.json](http://192.168.2.31/lineup.json)
  - [https://api.hdhomerun.com/api/xmltv?DeviceAuth=EB0wFJ8-Bct5BY-ZS8mF5XRO](https://api.hdhomerun.com/api/xmltv?DeviceAuth=EB0wFJ8-Bct5BY-ZS8mF5XRO)

- was [HDHomeRun Connect 4K - Tuner - http://192.168.2.87/](http://192.168.2.87/)
- [HDHomeRun Connect 4K - Tuner - http://192.168.6.14/](http://192.168.6.14/)
- [HDHomeRun SERVIO - DVR Storage - http://192.168.2.29/](http://192.168.2.29/)
  - [http://192.168.2.29/recorded_files.json](http://192.168.2.29/recorded_files.json)
  - [Forum - Storage space file usage API](https://forum.silicondust.com/forum/viewtopic.php?p=379950&hilit=lineup.json#p379950)

---
