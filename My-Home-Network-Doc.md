# Home Network Documentation

## Physical Topology

I live in a house with three levels: the basement, the first floor, and the second floor. My network devices are distributed across all three levels.

### First Floor (Main Network Floor)

This is where my main router is located.

**Devices:**
- Main Router (LAN ports + Wi-Fi 2.4/5 GHz)
- Smart TV (Wi-Fi)

**Connections:**
- ISP line → Router WAN port  
- Router LAN Port 1 → Ethernet cable going up to the 2nd floor (switch)  
- Router LAN Port 2 → Ethernet cable going down to the basement laptop  

---

### Second Floor

This floor has the switch and three rooms with wired PCs.

**Devices:**
- Network Switch  
- Room 1 PC (LAN)  
- Room 1 Printer (LAN)  
- Room 2 PC (LAN)  
- Room 3 PC (LAN)

**Connections:**
- Cable from Router LAN Port 1 → Switch uplink  
- Switch Port 1 → Room 1 PC  
- Switch Port 2 → Room 1 Printer  
- Switch Port 3 → Room 2 PC  
- Switch Port 4 → Room 3 PC  

---

### Basement

**Devices:**
- Basement Laptop (LAN)

**Connections:**
- Cable from Router LAN Port 2 → Basement laptop  

---

## Physical Topology Diagram
<img width="774" height="852" alt="image" src="https://github.com/user-attachments/assets/7897cd06-8218-4536-b4fa-1fe549d1c4de" />

---

## Logical Topology

My home network uses a single LAN.

**Network Information:**
- Network: 192.168.10.0/24  
- Gateway: 192.168.10.1 (Main Router)  
- DNS: 8.8.8.8, 1.1.1.1  
- DHCP Range: 192.168.10.100 – 192.168.10.150  
- Static IPs used for all wired devices  

**Topology Type:**  
- Star (switch → devices)  
- Router acts as the wireless access point  

**Network Segmentation:**  
- One network, no VLANs  

---

## Addressing Documentation

| Device | Floor/Room | Connection | Interface | IP Address | Notes |
|--------|------------|------------|-----------|-------------|--------|
| Main Router | 1st Floor | LAN/Wi-Fi | WAN/LAN | 192.168.10.1 | Gateway, DHCP |
| Network Switch | 2nd Floor | LAN | Ports 1–4 | N/A | Extends LAN |
| Room 1 PC | 2nd Floor | LAN | Ethernet | 192.168.10.11 | Static |
| Room 1 Printer | 2nd Floor | LAN | Ethernet | 192.168.10.40 | Static |
| Room 2 PC | 2nd Floor | LAN | Ethernet | 192.168.10.12 | Static |
| Room 3 PC | 2nd Floor | LAN | Ethernet | 192.168.10.13 | Static |
| Basement Laptop | Basement | LAN | Ethernet | 192.168.10.20 | Static |
| 1st Floor TV | 1st Floor | Wi-Fi | Wireless | 192.168.10.30 | Static |
| Phones/Tablets | Various | Wi-Fi | Wireless | DHCP 100–150 | Dynamic |

---

## Network Devices and Services

### Router Services
- DHCP  
- NAT  
- DNS forwarding  
- Wi-Fi 2.4/5 GHz  
- Firewall enabled  
- Remote admin off  

### Switch
- Unmanaged Layer 2  
- No config needed  

### End Devices
- Wired PCs (static IPs)  
- Printer (static IP)  
- Basement laptop  
- Smart TV (Wi-Fi)  

---

## Devices Configurations

### Router Configuration
- Default admin username changed  
- Strong password set  
- WPA2/WPA3 Wi-Fi security  
- SSIDs renamed  
- DHCP excludes static IP range  
- Remote access disabled  
- UPnP disabled  

### PCs
- Static IPs  
- Subnet mask 255.255.255.0  
- Gateway 192.168.10.1  

### Printer
- Wired (Ethernet)  
- Static IP  
- DHCP disabled  

---

## Secure Storage of Credentials

I do not store passwords in plain text.  
All router, Wi-Fi, and device passwords are stored in an encrypted password manager (Bitwarden). 
No credentials appear in this documentation.

---

### Version History

| Version | Date       | Author    | Description of Changes |
|---------|------------|-----------|-------------------------|
| v1      | 2025-11-21 | Jaered B.  | Initial creation of the network documentation. |
| v2      | 2025-11-22 | Jaered B.  | Updated structure, added new sections, and improved clarity. |
| v3      | 2025-11-23 | Jaered B.  | Final revisions, formatting cleanup, and added missing details. |




