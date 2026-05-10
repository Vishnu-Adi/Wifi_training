# Wi‑Fi Training Program – Module 3 Assignment

## 1. What are the different 802.11 PHY layer standards? Compare their characteristics.

The IEEE 802.11 PHY layer standards define how wireless signals are transmitted and received in Wi‑Fi networks. Over time, these standards evolved to improve speed, efficiency, reliability, and spectrum utilization.

### 802.11 (Original Standard)

The original 802.11 standard operated in the 2.4 GHz frequency band and supported very low data rates. It used both DSSS and FHSS transmission techniques.

### 802.11b

802.11b operated in the 2.4 GHz band using DSSS technology. It improved data rates significantly compared to the original standard and became popular because of its low cost and better range.

### 802.11a

802.11a operated in the 5 GHz band and introduced OFDM modulation. It provided higher throughput and lower interference compared to 802.11b, although the coverage range was generally lower.

### 802.11g

802.11g combined the advantages of 2.4 GHz coverage with OFDM-based higher throughput. It maintained backward compatibility with 802.11b devices.

### 802.11n

802.11n introduced MIMO technology, channel bonding, and operation in both 2.4 GHz and 5 GHz bands. It greatly improved throughput and signal reliability.

### 802.11ac

802.11ac operated mainly in the 5 GHz band and introduced wider channels, beamforming, and MU‑MIMO. It significantly increased wireless throughput.

### 802.11ax (Wi‑Fi 6 / 6E)

802.11ax improved efficiency in dense deployments using OFDMA, better scheduling, and enhanced power-saving mechanisms. Wi‑Fi 6E extended operation into the 6 GHz band.

### 802.11be (Wi‑Fi 7)

802.11be is designed for extremely high throughput, lower latency, and improved multi-user performance using advanced PHY enhancements such as wider channels and Multi-Link Operation.

---

## 2. What are DSSS and FHSS? How do they work?

DSSS and FHSS are spread spectrum technologies used in early wireless communication systems.

### DSSS – Direct Sequence Spread Spectrum

In DSSS, the original data signal is multiplied with a pseudo-random spreading code before transmission. This spreads the signal over a wider frequency range.

#### Working Principle

- The transmitter combines the data with a spreading code.
- The signal occupies a larger bandwidth.
- The receiver uses the same code to recover the original signal.

#### Advantages

- Better resistance to interference
- Improved reliability
- Better performance in noisy environments

### FHSS – Frequency Hopping Spread Spectrum

In FHSS, the transmitter rapidly changes its carrier frequency according to a predefined hopping sequence shared with the receiver.

#### Working Principle

- Data is transmitted over multiple frequencies.
- The transmitter hops between channels rapidly.
- The receiver follows the same hopping pattern.

#### Advantages

- Reduced effect of narrowband interference
- Improved security
- Lower probability of persistent interference

### Difference Between DSSS and FHSS

DSSS spreads the signal across a wide bandwidth continuously, whereas FHSS changes frequencies repeatedly during transmission.

---

## 3. How do modulation schemes work in the PHY layer? Compare different modulation schemes and their performance across various Wi‑Fi standards.

Modulation is the process of encoding digital data onto radio waves for wireless transmission.

Different modulation schemes represent different numbers of bits per symbol. Higher-order modulation schemes carry more bits but require cleaner signal conditions.

### Common Modulation Schemes

#### BPSK

Binary Phase Shift Keying uses two phase states and carries one bit per symbol. It is highly reliable but supports low throughput.

#### QPSK

Quadrature Phase Shift Keying uses four phase states and carries two bits per symbol. It provides better throughput than BPSK while maintaining good reliability.

#### 16‑QAM

16‑Quadrature Amplitude Modulation carries four bits per symbol. It increases throughput but requires better signal quality.

#### 64‑QAM

64‑QAM carries six bits per symbol and is commonly used in 802.11n and 802.11ac networks.

#### 256‑QAM

256‑QAM carries eight bits per symbol and improves throughput significantly in high-quality channels.

#### 1024‑QAM

1024‑QAM carries ten bits per symbol and is used in Wi‑Fi 6 for very high data rates under excellent signal conditions.

### Performance Comparison

- Lower-order modulation provides better stability and longer range.
- Higher-order modulation provides higher throughput but is more sensitive to noise and interference.
- Modern Wi‑Fi standards use adaptive modulation based on signal quality.

---

## 4. What is the significance of OFDM in WLAN? How does it improve performance?

OFDM stands for Orthogonal Frequency Division Multiplexing.

In OFDM, the available channel bandwidth is divided into multiple orthogonal subcarriers. Each subcarrier carries a portion of the data stream.

### Importance of OFDM

- Improves spectral efficiency
- Reduces the impact of multipath fading
- Supports higher data rates
- Improves reliability in indoor environments
- Allows efficient use of wide channels

### Performance Improvement

Instead of transmitting all data on one carrier, OFDM distributes the transmission across many subcarriers. This reduces interference effects and improves transmission stability.

OFDM became a major improvement in Wi‑Fi standards starting from 802.11a.

---

## 5. How are frequency bands divided for Wi‑Fi? Explain different bands and their channels.

Wi‑Fi operates mainly in the 2.4 GHz, 5 GHz, and 6 GHz frequency bands.

### 2.4 GHz Band

- Longer coverage range
- Better wall penetration
- Higher interference from Bluetooth, microwaves, and other devices
- Limited non-overlapping channels

### 5 GHz Band

- Higher throughput
- More available channels
- Reduced interference
- Shorter range compared to 2.4 GHz

### 6 GHz Band

- Used in Wi‑Fi 6E and Wi‑Fi 7
- Large amount of clean spectrum
- Supports high-capacity deployments
- Lower interference and congestion

### Channels

Each band is divided into channels used for communication. Channel overlap can cause interference, so non-overlapping channels are preferred for efficient WLAN operation.

---

## 6. What is the role of Guard Intervals in WLAN transmission? How does a short Guard Interval improve efficiency?

A Guard Interval is a small time gap inserted between OFDM symbols to reduce inter-symbol interference caused by delayed reflections.

### Role of Guard Interval

- Prevents overlap between consecutive symbols
- Reduces multipath distortion
- Improves decoding accuracy at the receiver

### Short Guard Interval

A Short Guard Interval reduces the duration of the guard period.

### Advantages

- Higher throughput
- Better spectral efficiency
- More symbols transmitted per second

### Limitation

Short GI performs best in environments with minimal multipath delay.

---

## 7. Describe the structure of an 802.11 PHY layer frame. What are its key components?

The PHY layer frame in Wi‑Fi is responsible for carrying MAC layer data over the wireless medium.

### Main Components

#### Preamble

The preamble helps the receiver synchronize with the incoming transmission and detect signal timing.

#### PHY Header

The PHY header contains transmission-related information such as data rate, modulation scheme, and frame length.

#### Payload

The payload carries the actual MAC frame or higher-layer data.

### Importance

The PHY frame structure ensures proper synchronization, decoding, and reliable wireless transmission.

---

## 8. What is the difference between OFDM and OFDMA?

### OFDM

OFDM divides a wireless channel into multiple subcarriers, but typically one user occupies the channel during a transmission period.

### OFDMA

OFDMA divides the channel into smaller resource units, allowing multiple users to transmit simultaneously.

### Key Differences

- OFDM serves one user at a time.
- OFDMA serves multiple users simultaneously.
- OFDMA improves efficiency and reduces latency in dense networks.
- OFDMA is widely used in Wi‑Fi 6.

---

## 9. What is the difference between MIMO and MU‑MIMO?

### MIMO

MIMO stands for Multiple Input Multiple Output.

It uses multiple antennas to transmit and receive multiple spatial streams between one transmitter and one receiver.

### MU‑MIMO

MU‑MIMO stands for Multi‑User Multiple Input Multiple Output.

It allows an access point to communicate with multiple users simultaneously using separate spatial streams.

### Difference

- MIMO improves throughput for a single device.
- MU‑MIMO improves overall network efficiency for multiple devices.

---

## 10. What are PPDU, PLCP, and PMD in the PHY layer?

### PPDU – Physical Layer Protocol Data Unit

PPDU is the complete PHY transmission unit sent over the wireless medium.

### PLCP – Physical Layer Convergence Procedure

PLCP acts as the interface between the MAC layer and the PHY layer. It formats MAC data into a PHY-compatible frame.

### PMD – Physical Medium Dependent

PMD is responsible for the actual radio transmission functions such as modulation, coding, signal generation, and reception.

### Relationship

- PLCP prepares the frame.
- PMD handles radio transmission.
- PPDU is the final transmitted PHY frame.

---

## 11. What are the types of PPDU? Explain the PPDU frame format across different Wi‑Fi generations.

Different Wi‑Fi generations introduced different PPDU formats to support newer PHY technologies.

### Non‑HT PPDU

Used in legacy Wi‑Fi systems before 802.11n.

### HT PPDU

Introduced with 802.11n to support High Throughput features such as MIMO.

### VHT PPDU

Used in 802.11ac to support Very High Throughput features such as wider channels and MU‑MIMO.

### HE PPDU

Introduced in 802.11ax for High Efficiency operation using OFDMA and improved scheduling.

### EHT PPDU

Used in 802.11be for Extremely High Throughput features.

### Evolution of PPDU

As Wi‑Fi standards evolved, PPDU formats became more advanced to support higher throughput, multi-user communication, wider bandwidth, and lower latency.

---

## 12. How is the data rate calculated?

Wi‑Fi data rate depends on multiple PHY parameters.

### Factors Affecting Data Rate

- Channel width
- Modulation scheme
- Coding rate
- Number of spatial streams
- Guard interval duration
- Number of subcarriers

### General Concept

Higher modulation order, larger channel width, more spatial streams, and shorter guard intervals increase throughput.

### Data Rate Calculation Principle

Data rate is determined by the number of bits transmitted per symbol, multiplied by the symbol rate and the number of spatial streams.

Modern Wi‑Fi dynamically adjusts these parameters depending on signal quality and network conditions.

