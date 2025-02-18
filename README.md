# Small Office Network Documentation

## 1. [Overview](pplx://action/followup)

This document describes a small office network's setup and basic security measures. This network provides both wired and wireless internet access for employees and resources.

## 2. [Network Topology](pplx://action/followup)

### 2.[1 Physical Topology](pplx://action/followup)

The network consists of the following components:

*   **[ISP Router](pplx://action/followup):** Simulates the internet service provider connection.
*   **[Main Switch](pplx://action/followup):** Provides wired network connections for office PCs and other devices.
*   **[Wireless Router](pplx://action/followup):** Provides Wi-Fi access for laptops, smartphones, and tablets.
*   **[PCs](pplx://action/followup):** Desktop computers connected via Ethernet cables.
*   **[Printer](pplx://action/followup):** A network printer connected via Ethernet cable.
*   **[Laptops](pplx://action/followup):** Portable computers accessing the network via Wi-Fi.
*   **[Smartphones](pplx://action/followup):** Mobile devices accessing the network via Wi-Fi.
*   **[Tablets](pplx://action/followup):** Portable tablet devices accessing the network via Wi-Fi.

### 2.[2 Logical Topology](pplx://action/followup)

The network is structured as follows:

1.  The ISP router connects to the main switch.
2.  The main switch provides wired connections for PCs and the wireless router.
3.  The wireless router provides Wi-Fi access for wireless devices (laptops, smartphones, tablets).

### 2.[3 Packet Tracer Image](pplx://action/followup)

![Image](https://github.com/user-attachments/assets/0b32b4f0-1915-42aa-9008-747b6ebf6a02)

## 3. [Device Configuration (Descriptive)](pplx://action/followup)

### 3.[1 ISP Router](pplx://action/followup)

The "ISP" router was configured to:

*   Simulate an internet connection by assigning itself a public IP address.
*   Act as the default gateway for the internal network.
*   Provide DHCP service, automatically assigning IP addresses to devices on the internal network.

### 3.[2 Main Switch](pplx://action/followup)

*   The switch was set up with basic security by limiting MAC addresses on the network ports and limiting who can connect to it.

### 3.[3 Wireless Router](pplx://action/followup)

The wireless router was configured to:

*   Obtain an IP address from the main router to connect to the internet.
*   Create a separate Wi-Fi network with a chosen network name (Router) and no password.
*   Provide DHCP service for wireless devices, assigning them IP addresses within a different range.

### 3.[4 End Devices (PCs, Laptops, Smartphones, Tablets)](pplx://action/followup)

*   All devices were configured to obtain IP addresses via DHCP automatically.
*   PCs obtained their addresses from the ISP Router.
*   Wireless devices obtained their addresses from the Wireless Router.

## 4. [Security Hardening (Descriptive)](pplx://action/followup)

The following security measures were implemented:

*   **[Strong Passwords](pplx://action/followup):** Strong, unique passwords were set for all devices (routers and switches).
*   **[Disable Unnecessary Services](pplx://action/followup):** Unneeded services were disabled on the routers and switch to reduce the attack surface.
*   **[Firewall Rules](pplx://action/followup):** Basic firewall rules were configured on the ISP router to:
    *   Block Telnet access from outside the network.
    *   Allow SSH access only from a specific management host.
*   **[Wireless Security](pplx://action/followup):** WPA2/WPA3 encryption was enabled on the wireless router with a strong password.

## 5. [Testing](pplx://action/followup)

The following tests were performed to verify the network configuration and security:

1.  Verify that all devices can connect to the network and obtain IP addresses.
2.  Verify that all devices can access the internet.
3.  Test that Telnet access to the ISP router is blocked from outside the network.
4.  Test that SSH access to the ISP router is only allowed from the designated management host.
