# Wi-Fi Assignment

-----

## 1. In which OSI layer the Wi-Fi standard/protocol fits?

Wi-Fi mainly works in two OSI layers:

- **Physical Layer (Layer 1)** — handles radio transmission, frequencies, modulation, and signal sending.
- **Data Link Layer (Layer 2)** — handles MAC addressing, framing, medium access, authentication, and association.

So, Wi-Fi is not just one layer; it is mainly a **Layer 1 and Layer 2** technology.

-----

## 2. Wi-Fi devices used in daily life and their wireless capabilities/properties after connecting to network

Common Wi-Fi devices are:

- Smartphones
- Laptops
- Smart TVs
- Tablets
- IoT devices like smart speakers, watches, cameras, and printers

After connecting to a network, these devices usually show properties such as:

- **Frequency band:** 2.4 GHz / 5 GHz / 6 GHz
- **Wi-Fi standard:** 802.11n / ac / ax / be
- **Link speed / data rate**
- **Channel width:** 20 MHz, 40 MHz, 80 MHz, 160 MHz
- **Security type:** WPA2 / WPA3
- **Signal strength (RSSI)**
- **MIMO stream count**
- **IP address** assigned by DHCP

### Matching device to Wi-Fi generation

|Standard|Generation  |Key Features                                      |
|--------|------------|--------------------------------------------------|
|802.11n |Wi-Fi 4     |2.4 GHz and 5 GHz, MIMO, up to 600 Mbps           |
|802.11ac|Wi-Fi 5     |Mainly 5 GHz, wider channels, beamforming, 256-QAM|
|802.11ax|Wi-Fi 6 / 6E|2.4/5/6 GHz, OFDMA, 1024-QAM, TWT                 |
|802.11be|Wi-Fi 7     |Higher throughput, 320 MHz channels, MLO, 4096-QAM|

So, if a device supports OFDMA and 1024-QAM, it belongs to Wi-Fi 6 or later. If it supports 6 GHz, it is Wi-Fi 6E or Wi-Fi 7.

-----

## 3. What is BSS and ESS?

### BSS – Basic Service Set

A BSS is the basic wireless network formed by one Access Point and the clients connected to it.

- One AP
- One group of associated stations
- Identified by a BSSID

### ESS – Extended Service Set

An ESS is a collection of multiple BSSs connected together through a wired backbone.

- Multiple APs
- Same SSID across APs
- Allows roaming between APs
- Used in offices, colleges, and large buildings

### Simple difference

- **BSS** = one AP cell
- **ESS** = multiple AP cells working together

-----

## 4. What are the basic functionalities of Wi-Fi Access Point?

A Wi-Fi Access Point performs the following tasks:

- Broadcasts the SSID
- Allows clients to discover the network
- Manages client association and disassociation
- Handles authentication
- Bridges wireless traffic to the wired network
- Controls channel and radio settings
- Supports encryption and security
- Helps in roaming coordination in enterprise networks
- Buffers frames for power-saving clients

In short, the AP acts as the **central point** that connects wireless devices to the network.

-----

## 5. Difference between Bridge mode and Repeater mode

### Bridge mode

In bridge mode, the device connects two network segments and forwards traffic between them.

- Mostly used to connect separate networks
- Works like a link between two LANs
- Can be used for wired-to-wireless or wireless-to-wired connectivity

### Repeater mode

In repeater mode, the device receives the wireless signal and retransmits it to extend coverage.

- Used to increase Wi-Fi range
- Rebroadcasts the same signal
- Helps where signal is weak

### Main difference

- **Bridge mode** connects networks.
- **Repeater mode** extends range.

-----

## 6. What are the differences between 802.11a and 802.11b?

|Feature       |802.11a                   |802.11b                     |
|--------------|--------------------------|----------------------------|
|Frequency band|5 GHz                     |2.4 GHz                     |
|Data rate     |Up to 54 Mbps             |Up to 11 Mbps               |
|Interference  |Less interference         |More interference           |
|Range         |Shorter                   |Better range                |
|Modulation    |OFDM                      |DSSS                        |
|Use case      |Higher speed, cleaner band|Better coverage, lower speed|

### Summary

802.11a is faster and uses 5 GHz, while 802.11b is slower but offers better range in 2.4 GHz.

-----

## 7. Configure modem/hotspot to operate only in 2.4 GHz and 5 GHz and compare the properties

When you force a device to use only one band, the observed properties change.

|Property                 |2.4 GHz|5 GHz |
|-------------------------|-------|------|
|Range                    |Higher |Lower |
|Speed                    |Lower  |Higher|
|Interference             |More   |Less  |
|Wall penetration         |Better |Poorer|
|Channel count            |Fewer  |More  |
|Stability in crowded area|Lower  |Better|

### Observation

> After connecting to the 2.4 GHz band, the device showed better range but lower speed and more interference. After switching to 5 GHz, the speed increased and interference reduced, but the coverage area became shorter.

-----

## 8. What is the difference between IEEE and WFA?

### IEEE

IEEE stands for **Institute of Electrical and Electronics Engineers**.

- It creates the technical standards
- For Wi-Fi, IEEE defines the 802.11 standards

### WFA

WFA stands for **Wi-Fi Alliance**.

- It certifies Wi-Fi products
- Ensures devices from different vendors work together
- Gives interoperability and compliance certification

### Difference

- **IEEE** writes the standard.
- **WFA** tests and certifies products based on the standard.

-----

## 9. Types of Wi-Fi internet connectivity backhaul

Backhaul is the connection that carries traffic from the AP or network edge to the main network or internet.

### Common types

- Fiber backhaul
- Ethernet backhaul
- Wireless point-to-point backhaul
- Microwave backhaul
- DSL/Cable backhaul
- Cellular backhaul
- Mesh backhaul

### Properties of common backhauls

|Backhaul Type          |Properties                                     |
|-----------------------|-----------------------------------------------|
|Fiber                  |Very high speed, low latency, highly reliable  |
|Ethernet               |Stable, easy to manage, common inside buildings|
|Wireless point-to-point|Useful where cable laying is difficult         |
|Mesh backhaul          |APs connect wirelessly to each other           |
|Cellular               |Used where no wired line is available          |

### For home or college

Most homes and colleges use **fiber backhaul** from the ISP to the router, and then **Ethernet backhaul** inside the building to access points or switches.

If your campus has APs connected through cables, the backhaul is usually Ethernet or fiber.

-----

## 10. Wi-Fi topologies and use cases

### 1. Infrastructure topology

This is the most common Wi-Fi topology.

- Clients connect through an AP
- AP connects to wired network
- **Used in:** homes, offices, colleges, and public Wi-Fi

### 2. Ad hoc topology

Devices communicate directly without an AP.

- No central access point
- Useful for temporary direct connections
- Rare in modern networks

### 3. Mesh topology

Multiple APs connect to each other wirelessly.

- Good for large coverage
- **Used in:** homes, campuses, and smart buildings
- Useful where cable installation is difficult

### 4. Point-to-point topology

Two wireless devices connect directly.

- Used to connect two buildings
- Long-distance wireless link
- Common in campus inter-building connectivity

### 5. Point-to-multipoint topology

One central node connects to multiple remote nodes.

- Used in wireless distribution systems
- Common in campus or outdoor deployments

### Summary

|Topology           |Use Case                 |
|-------------------|-------------------------|
|Infrastructure     |Normal Wi-Fi use         |
|Ad hoc             |Direct device-to-device  |
|Mesh               |Extended coverage        |
|Point-to-point     |Building-to-building     |
|Point-to-multipoint|One-to-many wireless link|
