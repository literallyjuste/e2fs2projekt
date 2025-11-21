# Progress Steps

- Unbound DNS Setup um dem Webserver eine domain zu geben (b4.server.lan)
- SSH-Service auf dem Webserver aktiviert
- Firewall regeln um SSH auf den Webserver nur vom Management server zu erlauben
- Firewall regel um port 80 und port 443 von der Firewall auf LAN zu blockieren 
- Firewall regel um LAN vom DMZ Netzwerk zu isolieren (Außnahme Webserver)
- Firewall regel um OPNSense nur von Management zu erreichen
- DHCPv6 für LAN und DMZ aufgesetzt. Router Announcements konfiguriert.
- Checkmk WebUI über IPv4/v6 nur von Management erreichbar gemacht
- Port forward auf das WAN Interface von dem Webserver über IPv6 aufgesetzt, damit der Webserver über die Public IPv6 erreichbar ist. 

Lan Interface:
![LAN Interface](/Pasted image 20251121165047.png)

DMZ Interface:
![DMZ Interface](/Pasted image 20251121164956.png)

WAN Interface:
![WAN Interface](/Pasted image 20251121165123.png)

LAN Firewall Regeln:
![LAN Firewall Regeln](/Pasted image 20251121164843.png]

DMZ Firewall Regeln:
![DMZ Firewall Regeln](/Pasted image 20251121164914.png)

NAT Port Forward:
![NAT Port Forward](/Pasted image 20251121170101.png)

DHCP Ranges:
![DHCP Ranges](/Pasted image 20251121165248.png)

Router Advertisements:
![Router Advertisements LAN](/Pasted image 20251121165356.png)
![Router Advertisements DMZ](/Pasted image 20251121165326.png)

DNS Override:
![DNS Override](/Pasted image 20251121165920.png)



### TODO:

- [x] DMZ Netzwerk
- [x] Webserver
- [x] Checkmk server
- [x] Management PC
- [x] LAN Firewall regeln (Internet Zugang, Webserver)
- [x] DMZ Firewall regeln (Webserver gesichert, Management)
- [x] Webserver IPv6 Erreichbarkeit
- [x] Webserver interner DNS eintrag
- [x] Management ssh/opnsense regeln
- [x] CA-Certificate

Arbeitsplatz(192.168.1.167/fdaa:3e59:2146:1::1eca)

Webserver Login: (192.168.2.131/fdaa:3e59:2146:2::1583)
Username: b4-admin
Password: 9pE2tqW2

Checkmk Server (192.168.2.224/fdaa:3e59:2146:2::1f11)

Management PC (192.168.2.164/fdaa:3e59:2146:2::1cf2)

Proxmox Login: 
Username: root
Password: !Qay123!

Firewall/Webserver v6 (2001:7c7:1906:104::4:48)
