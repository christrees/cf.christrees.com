[edit this](https://github.com/christrees/cf.christrees.com/edit/main/ns/README.md)

- [framework laptop https://frame.work/](https://frame.work/)
- [google remote](https://remotedesktop.google.com/access)
- [render network diagram in github](https://github.com/christrees/cf.christrees.com/blob/main/ns/cfnetwork.md)

### quick
---
- [cattvwin10 http://test.christrees.com:32400/](http://test.christrees.com:32400/)
- [dockerplex http://test.christrees.com:32500/](http://test.christrees.com:32500/)
- [tnasplex   http://test.christrees.com:32600/](http://test.christrees.com:32600/)
- [bs01ds411  http://test.christrees.com:32700/](http://test.christrees.com:32700/)

---
- [zmodo - web](https://user.zmodo.com/#/home) 
- [tbd laview - web]()
- [tbd blink - web]()
- [tbd energy - web]()
- [tbd vivitar - web]()
- tbd

---

# WIP Portals
- [https://cf.christrees.com/](https://cf.christrees.com/)
- [http://blog.christrees.com/wip/trinkcolab](http://blog.christrees.com/wip/trinkcolab)
- [http://test.christrees.com/](http://test.christrees.com/) 
- [https://whatismyipaddress.com/ip/24.149.22.11](https://whatismyipaddress.com/ip/24.149.22.11) - 24.149.22.11
- [https://whatismyipaddress.com/](https://whatismyipaddress.com/)
- [https://www.plex.tv/](https://www.plex.tv/)
- [https://www.plex.tv/claim/](https://www.plex.tv/claim/)
- [https://www.cfu.net/tv-internet/tv-service-info/channel-guide](https://www.cfu.net/tv-internet/tv-service-info/channel-guide)
- [cattvwin10 channel map](https://docs.google.com/spreadsheets/d/1wjN1_N5Vjji6NQgE3DXi4D-S76sAHppQrdXsqh5qX2E/edit#gid=0) 
- [tbd]()

## 192.168.6.0/24 gw [http://192.168.6.1/](http://192.168.6.1/)

| web proxy    |   Link  | type | description |
|--------------|---------|------|-------------|
| cfu | [http://192.168.6.1/](http://192.168.6.1/) | static | cfu fw19 |
| pfsense | [http://192.168.6.103:91/](http://192.168.6.103:91/) | to 192.168.2.1:80 | gui fw for 192.168.2.0/24 |
| nginx default | [http://192.168.6.103/](http://192.168.6.103/) | static | default nginx proxy page running in portainer |
| nginx proxy admin | [http://192.168.6.103:81](http://192.168.6.103:81) | static | admin for nginx running in portainer |
| -- _Proxy ADMIN_ |---------|------|-------------|
| cg proxmox admin | [https://192.168.6.103:8006](https://192.168.6.103:8006) | to 192.168.2.3:8006 | cg proxmox |
| cg2 proxmox admin | [https://192.168.6.103:8007](https://192.168.6.103:8007) | to 192.168.2.7:8006 | cg2 proxmox |
| portainer admin | [http://192.168.6.103:9000](http://192.168.6.103:9000) | static | portainer admin on proxmox docker 103 |
| truenas-cg admin | [https://192.168.6.103:9090](https://192.168.6.103:9090) | to 192.168.2.2:443 | TrueNAS-cg on proxmox truenas 102 |
| truenas-cg ssh | ssh 192.168.6.103:2021 | to 192.168.2.2:22 | ssh to truenas-cg |
| truenas-cg2 admin | [https://192.168.6.103:9091](https://192.168.6.103:9091) | to 192.168.2.6:444 | TrueNAS-cg2 on proxmox truenas 103 |
| truenas-cg2 ssh | ssh 192.168.6.103:2022 | to 192.168.2.6:22 | ssh to truenas-cg2 |
| bs01ds411 web | [http://192.168.6.103:5000/](http://192.168.6.103:5000/) | to 192.168.2.105:5000 | DS411 Synology |
| nsDiskStation web | [http://192.168.6.159:5000/](http://192.168.6.159:5000/) | macDHCP | DS212i Synology |
| -- TV Admin |---------|------|-------------|
| dockerplex web | [http://192.168.6.103:32400](http://192.168.6.103:32400) | static | 32400 on IP plex on portainer |
| tnasplex web | [http://192.168.6.103:32500](http://192.168.6.103:32500) | static | 32500 on IP plex on portainer |
| bs01ds411 web | [http://192.168.6.103:32700](http://192.168.6.103:32700) | static | 32700 on IP plex on bs01ds411 synology nas |
| cattvwin10 web | [http://192.168.6.180:32400](http://192.168.6.180:32400) | macDHCP | 32600 on IP plex on cattvwin10 |
| nsDiskStation web | [http://192.168.6.159:5000/](http://192.168.6.159:5000/) | macDHCP | DS212i Synology |
| HDHR-10802956 web | [http://192.168.6.160](http://192.168.6.160) | macDHCP | silicondust tuner |
| Security Cameras |---------|------|-------------|
| zmodo camera web | [http://192.168.6.161](http://192.168.6.161) | macDHCP | zmodo |
| zmodo camera web | [http://192.168.6.162](http://192.168.6.162) | macDHCP | zmodo |
| zmodo camera web | [http://192.168.6.163](http://192.168.6.163) | macDHCP | zmodo |
| zmodo camera web | [http://192.168.6.164](http://192.168.6.164) | macDHCP | zmodo |
| zmodo hub web | [http://192.168.6.165](http://192.168.6.165) | macDHCP | zmodo |


## 192.168.2.0/24 gw [http://192.168.2.1/](http://192.168.2.1/)
  
| web proxy    |   Link  | type | description |
|--------------|---------|------|-------------|
| pfsense | [http://192.168.2.1/](http://192.168.2.1/) | static | pfsense ng on subnet |
| truenas | [http://192.168.2.2/](http://192.168.2.2/) | static | truenas sg on subnet |
| proxmox | [https://192.168.2.3:8006/](https://192.168.2.3:8006/) | static | proxmox cg subnet |
| nginx default | [http://192.168.2.103/](http://192.168.2.103/) | static | default nginx proxy page running in portainer |
| nginx proxy admin | [http://192.168.2.103:81](http://192.168.2.103:81) | macDHCP | admin for nginx running in portainer |
| portainer admin | [http://192.168.2.103:9000](http://192.168.2.103:9000) | macDHCP | portainer admin on proxmox docker 103 |
| dockerplex web | [http://192.168.2.103:32400](http://192.168.2.103:32400) | macDHCP | 32400 on IP plex on portainer |
| tnasplex web | [http://192.168.2.2:32500](http://192.168.2.2:32500) | static | 32500 on IP plex on portainer |
| HDHR-1080AD03 web | [http://192.168.2.102](http://192.168.2.102) | macDHCP | tuner |
| bs01ds411 plex web | [http://192.168.2.105:32400](http://192.168.2.105:32400) | static | 32400 on IP plex on bs01ds411 synology nas |
| bs01ds411 admin web | [http://192.168.2.105:5000](http://192.168.2.105:5000) | static | 5000 on admin web bs01ds411 synology nas |

---

| admin web    |   Link  | description |
|--------------|---------|-------------|
| pfsense | [http://192.168.2.1/](http://192.168.2.1/) | pfsense ng on subnet |
| -- DHCP-Lease | [http://192.168.2.1/status_dhcp_leases.php?all=1](http://192.168.2.1/status_dhcp_leases.php?all=1) | DHCP-Lease |
| truenas | [http://192.168.2.2/](http://192.168.2.2/) | truenas sg on subnet |
| -- pools | [http://192.168.2.2/](http://192.168.2.2/) | truenas sg on subnet |
| proxmox | [https://192.168.2.3:8006/](https://192.168.2.3:8006/) | proxmox cg subnet |
| -- storage | [https://192.168.2.3:8006/](https://192.168.2.3:8006/) | proxmox cg subnet |
| nginx proxy admin | [http://192.168.2.103:81](http://192.168.2.103:81) | admin for nginx running in portainer |
| -- sites | [http://192.168.2.103:81](http://192.168.2.103:81) | admin for nginx running in portainer |
| portainer admin | [http://192.168.2.103:9000](http://192.168.2.103:9000) | portainer admin on proxmox docker 103 |
| -- admin | [http://192.168.2.103:9000](http://192.168.2.103:9000) | portainer admin on proxmox docker 103 |
| dockerplex web | [http://192.168.2.103:32400](http://192.168.2.103:32400) | 32400 on IP plex on portainer |
| -- admin | [http://192.168.2.103:32400](http://192.168.2.103:32400) | 32400 on IP plex on portainer |
| tnasplex web | [http://192.168.2.2:32500](http://192.168.2.2:32500) | 32500 on IP plex on portainer |
| -- admin | [http://192.168.2.2:32500](http://192.168.2.2:32500) | 32500 on IP plex on portainer |
| HDHR-1080AD03 web | [http://192.168.2.102](http://192.168.2.102) | tuner |
| -- web | [http://192.168.2.102](http://192.168.2.102) | tuner |
| bs01ds411 plex web | [http://192.168.2.105:32400](http://192.168.2.105:32400) | 32400 on IP plex on bs01ds411 synology nas |
| -- admin web | [http://192.168.2.105:5000](http://192.168.2.105:5000) | 5000 on buadmin web bs01ds411 nas |

---
- Domain [https://domains.google.com/registrar/](https://domains.google.com/registrar/)
  - DNS [https://domains.google.com/registrar/christrees.com/dns](https://domains.google.com/registrar/christrees.com/dns)
- Public [http://24.149.22.11/](http://24.149.22.11/) - as of 20230117

---

## DMZ LAN local
- cfu pop router [ng.cfu.net - 854G-1 - http://192.168.6.1/](http://192.168.6.1/)
  - [current devices](http://192.168.6.1/#/html/status/status_devicetable.html)
  - [DHCP Reservations](http://192.168.6.1/#/html/advanced/ip/advanced_ip_dhcpreservation.html)
  - [Port Forwarding](http://192.168.6.1/#/html/advanced/security/advanced_security_advancedportforwarding.html)
    - 32400 to 32400	192.168.6.180 (cattvWin10 plex)	TCP	32600 to 32600	All IP Addresses	
    - 80    to 80	    192.168.6.103 (nginx proxy man) TCP	80    to 80   	All IP Addresses
    - 32400 to 32400	192.168.6.103 (dockerplex plex)	TCP	32400 to 32400	All IP Addresses	
  - [Firewall Rules](http://192.168.6.1/#/html/advanced/security/advanced_security_firewallsettings.html)
- HDHomeRun Connect [HDHR-10802956 4K Dev - Tuner - http://192.168.6.160/](http://192.168.6.160/) DNS MAC Res
  - [http://192.168.6.160/discover.json](http://192.168.6.160/discover.json)
  - [http://192.168.6.160/lineup.json](http://192.168.6.160/lineup.json)
  - [https://api.hdhomerun.com/api/xmltv?DeviceAuth=EB0wFJ8-Bct5BY-ZS8mF5XRO](https://api.hdhomerun.com/api/xmltv?DeviceAuth=EB0wFJ8-Bct5BY-ZS8mF5XRO)
- Plex Server [cattvWin10 - http://192.168.6.180:32400/](http://192.168.6.180:32400/) DNS MAC Res
- [DHCP Reservations](http://192.168.6.1/#/html/advanced/ip/advanced_ip_dhcpreservation.html) DHCP Range 192.168.6.150-250
  - 192.168.6.159 - macci - i3 - [ghadmin](What#Time) 
  - 192.168.6.160 - HDHR-10802956 4K Dev see above
  - 192.168.6.161-164 - zmodo camera
  - 192.168.6.165 - zmodo hub
  - 192.168.6.180 - cattvWin10 - ISP2150 4core - [tvadmin](What#Time)
- Static IP used in 192.168.6.0/24 subnet
  - 192.168.6.101 - network gport .2 subnet
  - 192.168.6.102 - storage gport .2 subnet
  - 192.168.6.103 - compute gport .2 subnet

---
## ns lan
- ns.cf.lan 192.168.2.0/24 subnet for netstack Static IP used in 192.168.6.0/24 subnet
- 192.168.2.1 - network gport .2 gw pfsense [http://192.168.2.1](http://192.168.2.1) [admin](What#Time)
  - [current arp table http://192.168.2.1/diag_arp.php](http://192.168.2.1/diag_arp.php)
  - [DHCP Leases - http://192.168.2.1/status_dhcp_leases.php](http://192.168.2.1/status_dhcp_leases.php)
  - [Firewall Rules - http://192.168.2.1/firewall_rules.php](http://192.168.2.1/firewall_rules.php)
    - 80    to 80	    192.168.6.103 (nginx proxy man) TCP	80    to 80   	All IP Addresses
    - 32400 to 32400	192.168.6.103 (dockerplex plex)	TCP	32400 to 32400	All IP Addresses	
- 192.168.2.2 - storage gport .2 subnet tbd truenas
- 192.168.2.3 - compute gport [http://192.168.2.3:8006 proxmox admin](http://192.168.2.3:8006) [root](What#Time)
  - [http://192.168.2.103/       nginx proxy default page](http://192.168.2.103/) 
  - [http://192.168.2.103:81     nginx proxy admin](http://192.168.2.103:81) [ghadmin](What#Time)
    - http://testapp.com -> app2:80 [http://testapp.com](http://testapp.com) only c:/Windows/System32/drivers/etc/hosts file on cattvWin10 
    - http://test.christrees.com -> app2:80 [http://test.christrees.com](http://test.christrees.com)
  - [http://192.168.2.103:9000   portainer admin](http://192.168.2.103:9000) [admin](What#Time?)
  - [http://192.168.2.103:32400  dockerplex web](http://192.168.2.103:32400/web/index.html#!/) [christrees https://plex.tv](https://plex.tv)

---
### Reference
- [Plex downloads](https://www.plex.tv/media-server-downloads/)
  - Plex 1.28.2 for OSX 10.9
  - [Plex remote client network issue](https://www.devwithimagination.com/2019/08/21/plex-docker-and-the-problem-of-always-appearing-as-remote/)
  - [Plex remote access pfsense configs](https://www.thesmarthomebook.com/2020/04/16/fixing-remote-access-for-plex-in-pfsense/)
  - [Plex-Reverse-Proxy-for-Docker](https://github.com/fmillion/docs/blob/master/Plex-Reverse-Proxy-for-Docker.md)
- [ZeroTier downloads](https://www.zerotier.com/download/)
  - [cattv - network - 52b337794f721ef7](https://my.zerotier.com/network/52b337794f721ef7) ghadmin
  - [tbd]()
- [pfsense monitor bandwidth useage](https://docs.netgate.com/pfsense/en/latest/monitoring/graphs/bandwidth-usage.html)
- [https://adamtheautomator.com/nginx-proxy-manager/](https://adamtheautomator.com/nginx-proxy-manager/)
- [portainer with nginx proxy manager - install](https://www.howtoforge.com/how-to-install-and-use-portainer-for-docker-management-with-nginx-proxy-manager/)
- [https://nginxproxymanager.com/guide/#quick-setup](https://nginxproxymanager.com/guide/#quick-setup)
- [https://nginxproxymanager.com/advanced-config/#best-practice-use-a-docker-network](https://nginxproxymanager.com/advanced-config/#best-practice-use-a-docker-network)
- [https://github.com/2cld/netstack/tree/master/docs/lan](https://github.com/2cld/netstack/tree/master/docs/lan)
- [https://app.diagrams.net/#Hpitimon%2FspComNet%2Fmain%2Fproxmox22](https://app.diagrams.net/#Hpitimon%2FspComNet%2Fmain%2Fproxmox22)
- [https://www.virtualizationhowto.com/2022/08/pfsense-proxmox-install-process-and-configuration/](https://www.virtualizationhowto.com/2022/08/pfsense-proxmox-install-process-and-configuration/)
- [https://tailscale.com/compare/zerotier/](https://tailscale.com/compare/zerotier/)
- [https://login.tailscale.com/admin/welcome](https://login.tailscale.com/admin/welcome) - ghadmin@horseoff.com login-with-google
- [tbd]()

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
