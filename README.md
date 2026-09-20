# Configure-a-wireless-router-and-clients
Setting up a Home wireless router and establishing connectivity between the router and various devices in the home.

A Cisco Packet Tracer lab that sets up a small home network: a cable modem provides internet access, a wireless router distributes it to wired and wireless devices, and a laptop connects to the resulting Wi-Fi network to reach an external web server.

Topology
Network Topology

The network spans three rooms and an external internet segment:

Office — Cable Modem, Home Wireless Router, and a wired Office PC
Bedroom — Bedroom PC, wired into the router
Living Room — a Laptop (wireless) and a TV (wired)
Internet — a Cable Splitter feeding the modem, connected through the cloud to an external server hosting skillsforall.srv
Objectives
Configure a wireless router's basic and wireless settings from its web-based GUI
Secure a wireless network with WPA2-Personal encryption
Connect a laptop's wireless adapter to a secured SSID
Verify end-to-end connectivity by browsing to an external server
Configuration Steps
1. Verify wired client addressing The Office PC pulls an IPv4 address via DHCP (192.168.0.2) from the router, confirming the LAN side is already functional.

Office PC IP Configuration

2. Access the router's basic setup Logged into the router's web GUI (192.168.0.1) to confirm DHCP server settings — start address 192.168.0.1, pool of 10 users.

Router Basic Setup

3. Configure the wireless network name Under Wireless > Basic Wireless Settings, set the 2.4 GHz SSID to MyHome and enabled SSID broadcast so the network is discoverable.

Wireless Basic Settings

4. Set the security mode Under Wireless > Wireless Security, changed the security mode from Disabled to WPA2 Personal.

Selecting WPA2 Personal

5. Set the passphrase Configured AES encryption with the passphrase MyPassPhrase1!.

Wireless Passphrase

6. Connect the laptop to the SSID On the Laptop's wireless adapter, selected the MyHome network from the site list and clicked Connect.

Laptop Site Survey

7. Enter the pre-shared key Prompted for the WPA2-Personal pre-shared key; entered the matching passphrase.

Pre-shared Key Prompt

8. Confirm the connection The adapter reports a successful connection to the access point.

Connection Successful

9. Verify link details Link Information shows the laptop received 192.168.0.3 via DHCP, with WPA2-Personal security active.

Wireless Link Status

10. Test connectivity From the laptop's browser, navigated to http://skillsforall.srv and received the expected page, confirming full connectivity from wireless client to the external server across the internet cloud.

Browser Test

Key Results
Device	Connection Type	IP Address
Office PC	Wired (DHCP)	192.168.0.2
Laptop	Wireless (DHCP)	192.168.0.3
Home Wireless Router	LAN Gateway	192.168.0.1
SSID: MyHome
Security: WPA2-Personal (AES)
Passphrase: MyPassPhrase1!
Files
Configure a Wireless Router and Client.pka — the Packet Tracer project file
images/ — screenshots documenting the topology and configuration steps
Requirements
Cisco Packet Tracer (version 8.x or later recommended) — available free via Cisco Networking Academy.

How to Open:
1. Download Configure a Wireless Router and Client.pka
2. Open it in Cisco Packet Tracer
3. Click each device to review its configuration under the Config and Desktop tabs.
