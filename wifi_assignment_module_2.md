# Wi‑Fi Training Program – Assignment Answers (Module 2)

## 1. Brief about SplitMAC architecture and how it improves AP performance

SplitMAC architecture is a design used in enterprise Wi‑Fi networks where the functionality of an Access Point (AP) is divided between the AP and the Wireless LAN Controller (WLC).

In this architecture:

- Time‑critical operations such as beacon transmission, frame acknowledgment, and encryption/decryption are handled by the AP.
- Centralized operations such as authentication policies, roaming decisions, RF management, and configuration management are handled by the controller.

This division reduces the processing load on the AP and allows centralized management.

### How it improves AP performance

- AP becomes lightweight and easier to manage.
- Configuration changes can be pushed from one central controller.
- Roaming becomes faster because the controller maintains client information.
- RF optimization becomes easier in large environments.
- Troubleshooting and monitoring are centralized.
- Better scalability for large enterprise deployments.

In simple terms, SplitMAC allows APs to focus mainly on wireless transmission while the controller handles intelligence and management.

---

# 2. Describe CAPWAP and explain the flow between AP and Controller

CAPWAP stands for **Control And Provisioning of Wireless Access Points**.

It is a protocol used for communication between Lightweight Access Points and Wireless LAN Controllers.

CAPWAP allows the controller to centrally manage multiple APs.

### Basic CAPWAP Flow

1. AP powers on.
2. AP gets an IP address using DHCP.
3. AP discovers the Wireless LAN Controller.
4. AP establishes a secure CAPWAP tunnel with the controller.
5. AP downloads configuration and firmware if needed.
6. AP starts broadcasting SSIDs.
7. Client traffic and control messages are exchanged through CAPWAP tunnels.

### Why CAPWAP is important

- Centralized management
- Simplified configuration
- Better security
- Easier firmware upgrades
- Better scalability

---

# 3. Where CAPWAP fits in OSI model, and the two tunnels in CAPWAP

CAPWAP mainly operates at the **Application Layer (Layer 7)** of the OSI model because it is a control protocol running over UDP/IP.

It uses:

- UDP port 5246 for control traffic
- UDP port 5247 for data traffic

### Two tunnels in CAPWAP

## a) Control Tunnel

This tunnel carries:

- AP registration messages
- Configuration information
- Heartbeat messages
- RF management information
- Authentication and management traffic

This tunnel is encrypted using DTLS for security.

## b) Data Tunnel

This tunnel carries:

- Actual wireless client data traffic
- User packets between client and controller

Depending on deployment, the data tunnel may or may not be encrypted.

---

# 4. Difference between Lightweight APs and Cloud‑based APs

## Lightweight AP

- Depends on a Wireless LAN Controller.
- Most configurations are managed through the controller.
- Common in enterprise campuses.
- CAPWAP is used between AP and controller.
- Requires controller infrastructure.

## Cloud‑based AP

- Managed through a cloud platform.
- No on‑premise controller is required.
- Management can be done remotely from anywhere.
- Easier deployment for distributed branches.
- Common in modern organizations and SMB environments.

### Main Difference

Lightweight APs use a local controller inside the organization, while cloud APs use cloud management platforms over the internet.

---

# 5. How the CAPWAP tunnel is maintained between AP and Controller

After the CAPWAP tunnel is established, both the AP and controller continuously exchange keepalive or heartbeat messages.

This helps both devices know that the connection is still active.

### Tunnel Maintenance Process

- AP periodically sends keepalive messages.
- Controller responds to confirm connectivity.
- If the AP does not receive responses for a certain time, it assumes the controller is unreachable.
- AP may try to reconnect or discover another controller.

This mechanism ensures reliability and continuous communication.

---

# 6. Difference between Sniffer mode and Monitor mode

## Sniffer Mode

In sniffer mode, the AP captures wireless packets and forwards them to a packet analysis tool like Wireshark.

### Use Cases

- Packet analysis
- Troubleshooting wireless issues
- Protocol debugging
- Security analysis

## Monitor Mode

In monitor mode, the AP does not serve clients. Instead, it scans the wireless environment continuously.

### Use Cases

- Detect rogue APs
- Detect interference
- Wireless intrusion detection
- RF monitoring

### Main Difference

- Sniffer mode focuses on packet capture.
- Monitor mode focuses on wireless environment monitoring and security.

---

# 7. If WLC is deployed in WAN, which AP mode is best for local network and why?

If the Wireless LAN Controller is deployed over a WAN, **FlexConnect mode** is generally the best option.

### Why FlexConnect is preferred

- Client traffic can be switched locally at the branch.
- WAN bandwidth usage is reduced.
- Wireless clients can continue working even if WAN connectivity to the controller fails.
- Better performance for remote branch offices.

### Advantage

FlexConnect provides centralized management while allowing local data forwarding.

---

# 8. Challenges of deploying autonomous APs in large networks

Autonomous APs are standalone APs that are configured individually.

In a large environment like a university with more than 50 APs, several challenges occur.

### Challenges

- Each AP must be configured manually.
- Firmware upgrades become difficult.
- RF optimization becomes complex.
- Roaming may not work efficiently.
- Troubleshooting takes more time.
- Security policies become inconsistent.
- Scaling the network becomes difficult.

### Conclusion

Autonomous APs work well for small networks but become difficult to manage in large enterprise deployments.

---

# 9. What happens to wireless clients connected to a Lightweight AP if the WLC goes down?

The behavior depends on the AP mode.

## Local Mode AP

If the controller goes down:

- Existing clients may temporarily continue working.
- New client authentication usually fails.
- Centralized functions stop working.
- Eventually, clients may disconnect.

This happens because Local Mode APs depend heavily on the controller.

## FlexConnect AP

If local switching is enabled:

- Existing clients can continue accessing the local network.
- Local authentication may continue depending on configuration.
- Internet access may still work.

### Final Point

FlexConnect provides better survivability during controller failures compared to Local Mode APs.
