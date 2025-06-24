# Secure Home Network with TP-Link Mesh Wi-Fi and Pi-hole Ad Blocking
## Overview
- 🖥 This project documents my implementation of a secure home network using a TP-Link Deco XE75 mesh Wi-Fi system combined with Pi-hole on a Raspberry Pi Zero 2 W. The setup is designed to improve performance, reduce tracking/ads, and enhance local network security.

---

## 🎯 Goals  
- Replace ISP Wi-Fi with a more secure and scalable mesh system  
- Deploy **network-wide ad blocking** with Pi-hole DNS  
- Segment IoT and personal devices for better hygiene  
- Learn and apply core networking and security concepts  
- Document the project as a cybersecurity portfolio item  

---

## 🧰 Tech Stack

| Component              | Description                                 |
|------------------------|---------------------------------------------|
| TP-Link Deco XE75      | Tri-band mesh Wi-Fi 6E system               |
| Raspberry Pi Zero 2 W  | Runs Pi-hole DNS sinkhole                   |
| CenturyLink C4000XG    | ISP modem/router (Wi-Fi disabled)           |
| Pi-hole                | DNS-level ad blocker                        |
| GitHub                 | Documentation and professional showcase     |

---

## 🔌 Network Architecture

- [Internet]
    - ↓
- [C4000XG Modem/Router] (Wi-Fi Disabled)
    - ↓ (Ethernet)
- [TP-Link Deco XE75 Mesh System]
    ├── Main Network (Phones, Laptops)
    ├── IoT Network (TV, Smart Plugs, etc.)
    - ↓
- [Pi-hole DNS Server on Raspberry Pi Zero 2 W]

---

## 🔐 Security Considerations  
- WPA2/WPA3-Personal enabled on all SSIDs  
- **UPnP disabled** on both ISP router and Deco system  
- **IoT devices isolated** using Deco's "IoT Network" feature  
- Admin passwords changed from factory defaults  
- Pi-hole admin interface protected with password  
- DNS queries logged locally; no external analytics services used  
- Static IP assigned to Raspberry Pi for DNS reliability  

---

## ⚙️ Configuration Highlights  

- Pi-hole set as primary DNS via Deco app (`More > DHCP Server`)  
- Static IP reservation for Pi-hole on the Deco network  
- Custom blocklists added to Pi-hole:  
  - [StevenBlack/hosts](https://github.com/StevenBlack/hosts)  
  - [OISD blocklist](https://oisd.nl)  
- Pi-hole admin panel configured for local access only  

---
