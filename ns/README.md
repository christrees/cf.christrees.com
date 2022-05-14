ns - Netstack

# Netstack Edge Node

- Public [http://24.149.23.184/](http://24.149.23.184/)
  - DMZ Lan [ng.cfu.net - 854G-1 - http://192.168.6.1/](http://192.168.6.1/)
    - [ng.cf.lan -  http://192.168.2.1/](http://192.168.2.1/) ng network gateway (device ASUS RT-AC87U sb pfSense)
    - [sg.cf.lan -  http://192.168.2.2/](http://192.168.2.2/) sg storage gateway (device TrueNAS core)
    - [cg.cf.lan -  http://192.168.2.3/](http://192.168.2.3/) cg compute gateway (device Proxmox)

| IP | lan | purpose | ops | setup |
|----|-----|---------|-----|-------|
| [https://192.168.2.1](https://192.168.2.1) | [https://ng.cf.lan](https://ng.cf.lan) | ng - network gateway | [ ng ops ]() | [ng setup](https://netstack.org/docs/lan/network/pfsense/setup) |
| [https://192.168.2.2](https://192.168.2.2) | [https://sg.cf.lan](https://sg.cf.lan) | sg - storage gateway | [ sg ops ]() | [sg setup](https://netstack.org/docs/lan/storage/freenas/setup) |
| [https://192.168.2.3](https://192.168.2.3) | [https://cg.cf.lan](https://cg.cf.lan) | cg - compute gateway | [ cg ops ]() | [cg setup](https://netstack.org/docs/lan/compute/proxmox/) |

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

## DVR Network Current [http://24.149.23.184/](http://24.149.23.184/)
- [ng.cfu.net - 854G-1 - http://192.168.6.1/](http://192.168.6.1/)
  - [devices on 192.168.6.0/24](http://192.168.6.1/#/html/status/status_devicetable.html)
  - [LAN port status](http://192.168.6.1/#/html/status/status_lanstatus_ipv6.html)
  - [NAT Table status](http://192.168.6.1/#/html/status/status_nattable.html)
  - [DMZ Host](http://192.168.6.1/#/html/advanced/security/advanced_security_dmzhosting.html)
  - [FireWall Filters](http://192.168.6.1/#/html/advanced/security/advanced_security_firewallsettings.html)
  - [PortForward](http://192.168.6.1/#/html/advanced/security/advanced_security_advancedportforwarding.html)
  - [tbd]()
  - [tbd]()
- [ng.cf.lan - ASUS RT-AC87U - http://192.168.2.1/](http://192.168.2.1/)
  - [Port Forward](http://192.168.2.1/Advanced_VirtualServer_Content.asp)
  - [Port Trigger](http://192.168.2.1/Advanced_PortTrigger_Content.asp)
  - [DMZ](http://192.168.2.1/Advanced_Exposed_Content.asp)
  - [DHCP](http://192.168.2.1/Advanced_DHCP_Content.asp)
  - [tbd]()
  - [tbd]()
- [sg.cf.lan - TrueNAS Scale - http://192.168.2.2/](http://192.168.2.2/) root What#Time
  - SMB Share - cfplex - smb://nsadmin@192.168.2.2
  - [tbd]()
  - [tbd]()
  - [tbd]()
- [plex global - https://www.plex.tv/](https://www.plex.tv/)
- [plex on local - http://127.0.0.1:32400/](http://127.0.0.1:32400/)
- [plex on catmini - http://192.168.2.35:32400/](http://192.168.2.35:32400/)
- [plex on admin2cld-win10 - http://192.168.6.15:32400/](http://192.168.6.15:32400/)
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
