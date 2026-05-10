# Wi‑Fi Training Program – Module 4 Assignment

## 1. What is the significance of the MAC layer and in which position is it placed in the OSI model?

The MAC layer, or Medium Access Control layer, is a sublayer of the Data Link Layer in the OSI model. It is placed at Layer 2, between the Logical Link Control (LLC) layer and the Physical (PHY) layer.

The MAC layer plays a major role in wireless communication because multiple devices share the same wireless medium. It controls how devices access the channel and ensures reliable transmission of frames.

### Significance of the MAC Layer

- Controls access to the wireless medium
- Handles frame addressing using MAC addresses
- Manages retransmissions and acknowledgments
- Supports authentication and association procedures
- Handles fragmentation and aggregation
- Controls power-saving operations
- Maintains communication reliability

In Wi‑Fi networks, the MAC layer is responsible for coordinating communication between stations and access points efficiently.

---

## 2. Describe the frame format of the 802.11 MAC header and explain the purpose of each field.

The 802.11 MAC frame contains several fields used for communication, addressing, control, and error detection.

### Main Fields in the MAC Header

#### Frame Control Field

This field identifies the type and subtype of the frame and contains control information such as protocol version, retry bit, power management bit, and encryption indication.

#### Duration/ID Field

This field specifies how long the wireless medium will remain reserved for the current transmission.

#### Address Fields

The 802.11 frame can contain up to four address fields.

- Source Address: identifies the sender
- Destination Address: identifies the receiver
- BSSID: identifies the access point or wireless network
- Transmitter/Receiver Address: used depending on frame direction

#### Sequence Control Field

This field is used for sequencing and fragmentation management.

#### QoS Control Field

Used in QoS-enabled networks to prioritize traffic.

#### HT Control Field

Used in high-throughput communication for advanced PHY operations.

#### Frame Body

Contains the actual payload or management information.

#### FCS – Frame Check Sequence

Used for error detection to verify frame integrity.

The MAC header structure allows Wi‑Fi devices to coordinate reliable communication over a shared medium.

---

## 3. Please list all the MAC layer functionalities in Management, Control, and Data plane.

The MAC layer functionalities are divided into Management, Control, and Data operations.

### Management Functions

These functions establish and maintain wireless connectivity.

- Beacon transmission
- Authentication
- Association and reassociation
- Probe request and response
- Scanning
- Roaming support
- Power management coordination
- Channel management
- Synchronization

### Control Functions

These functions manage access to the wireless medium.

- RTS/CTS operation
- Acknowledgment handling
- Block ACK operation
- NAV management
- Carrier sensing
- Backoff mechanisms
- Collision avoidance
- Frame retransmission control

### Data Functions

These functions handle actual user traffic.

- Data frame transmission
- Frame aggregation
- Fragmentation handling
- QoS traffic prioritization
- Encryption and decryption support
- Error checking
- Traffic forwarding

Together, these functions allow the MAC layer to manage wireless communication efficiently.

---

## 4. Explain the scanning process and its types in detail.

Scanning is the process by which a wireless client discovers nearby access points and available wireless networks.

### Types of Scanning

#### Passive Scanning

In passive scanning, the client listens for beacon frames transmitted periodically by access points.

##### Process

- The client tunes to a channel.
- It waits for beacon frames.
- The beacon contains SSID, supported rates, security information, and other parameters.
- The client collects information and moves to the next channel.

##### Advantages

- Lower transmission overhead
- Less interference generation
- Energy efficient

##### Disadvantages

- Slower discovery process

#### Active Scanning

In active scanning, the client actively sends probe request frames.

##### Process

- The client broadcasts or unicasts a probe request.
- Nearby APs reply with probe responses.
- The client evaluates the received information.

##### Advantages

- Faster network discovery
- Faster roaming support

##### Disadvantages

- Higher overhead
- Increased wireless traffic

### Importance of Scanning

Scanning is essential for network selection, roaming, and maintaining wireless connectivity.

---

## 5. Brief about the client association process.

The client association process is the sequence of steps through which a wireless client connects to an access point.

### Steps in Client Association

#### Scanning

The client searches for available networks using active or passive scanning.

#### Authentication

The client performs authentication with the AP. In modern Wi‑Fi, this may involve WPA2/WPA3 authentication procedures.

#### Association

The client sends an association request to the AP.

The AP responds with an association response if the request is accepted.

#### Security Handshake

For secured networks, the EAPOL 4-way handshake takes place to derive encryption keys.

#### Data Communication

After successful association and key installation, encrypted data communication begins.

### Purpose of Association

Association formally registers the client with the AP and allows network communication.

---

## 6. Explain each step involved in the EAPOL 4-way handshake and the purpose of each key derived from the process.

The EAPOL 4-way handshake is used in WPA/WPA2/WPA3 networks to establish encryption keys securely between the client and access point.

### Purpose of the Handshake

- Confirm both devices possess the same PMK
- Generate fresh session keys
- Install encryption keys securely

### Step 1

The AP sends a nonce value called ANonce to the client.

The client now has:

- PMK
- ANonce
- Client MAC address
- AP MAC address

### Step 2

The client generates its own nonce called SNonce.

Using the PMK, ANonce, SNonce, and MAC addresses, the client derives the PTK.

The client sends the SNonce and a MIC back to the AP.

### Step 3

The AP derives the same PTK and verifies the MIC.

The AP then sends:

- GTK for broadcast traffic
- Installation instructions for encryption keys
- MIC for integrity protection

### Step 4

The client confirms successful installation of the keys.

After this step, encrypted communication begins.

### Keys Derived

#### PMK – Pairwise Master Key

The root key used to derive session keys.

#### PTK – Pairwise Transient Key

Used for unicast encryption between client and AP.

#### GTK – Group Temporal Key

Used for broadcast and multicast traffic.

The handshake ensures secure communication without directly transmitting the encryption keys over the air.

---

## 7. Describe the power saving scheme in the MAC layer and explore the types of power saving mechanisms.

Power-saving mechanisms are used in Wi‑Fi to reduce battery consumption in wireless devices.

### Basic Power Saving Operation

A client can enter sleep mode when it does not need immediate communication.

The AP buffers frames intended for the sleeping client.

The client wakes periodically to check beacon frames for buffered traffic information.

### Types of Power Saving Mechanisms

#### Legacy Power Save Mode

The client sleeps and wakes periodically to receive buffered traffic.

#### U‑APSD – Unscheduled Automatic Power Save Delivery

Used in QoS-enabled networks to improve efficiency for applications like voice and video.

#### Target Wake Time (TWT)

Introduced in Wi‑Fi 6.

The AP schedules communication times with clients to reduce unnecessary wake-ups and improve battery life.

### Advantages of Power Saving

- Reduced battery consumption
- Improved device efficiency
- Better management of wireless resources

---

## 8. Describe the Medium Access Control methodologies.

Medium Access Control methodologies determine how wireless devices share the communication medium.

### CSMA/CA – Carrier Sense Multiple Access with Collision Avoidance

Wi‑Fi mainly uses CSMA/CA.

### Working Process

- A device checks whether the channel is idle.
- If the medium is busy, the device waits.
- A random backoff timer is selected.
- The device transmits only after the timer expires.
- The receiver sends an ACK if the frame is received successfully.

### RTS/CTS Mechanism

RTS/CTS helps reduce collisions caused by hidden nodes.

### NAV – Network Allocation Vector

NAV reserves the channel for a specified duration to reduce collisions.

### Importance

These methodologies ensure fair medium access and reliable communication in shared wireless environments.

---

## 9. Brief about the Block ACK mechanism and its advantages.

The Block ACK mechanism improves transmission efficiency by acknowledging multiple frames together instead of individually.

### Working Principle

- Multiple frames are transmitted in sequence.
- The receiver stores the received frames.
- A single Block ACK frame acknowledges multiple packets.

### Advantages

- Reduced protocol overhead
- Improved throughput
- Lower acknowledgment traffic
- Better efficiency for high-speed communication
- Reduced retransmission overhead

Block ACK is widely used with frame aggregation techniques in modern Wi‑Fi standards.

---

## 10. Explain about A‑MSDU, A‑MPDU and A‑MSDU in A‑MPDU.

Aggregation techniques are used in Wi‑Fi to improve efficiency by combining multiple frames into larger transmissions.

### A‑MSDU – Aggregated MAC Service Data Unit

In A‑MSDU aggregation, multiple MSDUs are combined into a single MPDU.

#### Characteristics

- Lower overhead
- Shared MAC header
- Better efficiency for small packets
- Entire aggregate must be retransmitted if an error occurs

### A‑MPDU – Aggregated MAC Protocol Data Unit

In A‑MPDU aggregation, multiple MPDUs are combined together.

#### Characteristics

- Each MPDU has its own MAC header and checksum
- Better error handling
- Only corrupted MPDUs require retransmission
- Supports Block ACK operation

### A‑MSDU within A‑MPDU

Modern Wi‑Fi standards can combine both methods.

Multiple MSDUs are first aggregated into A‑MSDUs, and then multiple A‑MSDUs are packed into an A‑MPDU.

### Advantages

- Very high transmission efficiency
- Reduced overhead
- Improved throughput
- Better wireless resource utilization

These aggregation techniques are important in high-speed Wi‑Fi standards such as 802.11n, 802.11ac, and 802.11ax.
