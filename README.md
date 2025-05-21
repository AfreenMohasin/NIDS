# Network Intrusion Detection System (NIDS)

This project introduces a fundamental Network Intrusion Detection System (NIDS), meticulously crafted in C++. It's designed to be your network's vigilant observer, continuously analyzing traffic to pinpoint potential security threats and detect any unusual behavior that could signal an intrusion.

## Features

- Real-time Packet Analysis: Captures and processes network packets in real-time, providing immediate insights into traffic flow.
- Attack Pattern Recognition(Specifically identifies and flags common attack vectors, including):
  - TCP SYN Flood attacks
  - Broadcast Ping Flood attacks
  - Random Port Connection Flood detection
  - UDP packet monitoring
- Traffic Statistics Monitoring: Tracks key network metrics to help identify deviations from normal behavior.
- Integrated Logging System: Maintains a detailed log of all alerts, detected events, and system activities.
- Configurable Anomaly Detection: Allows you to adjust thresholds for more precise anomaly detection tailored to your network environment.

## Prerequisites

- Linux operating system.
- The libpcap library for packet capturing.
- A G++ compiler (or compatible C++ compiler).
- Root/sudo privileges are required to capture network traffic.
- A basic understanding of networking concepts.
- Intermediate to advanced knowledge of C/C++ programming.

## Installation

1. Install the required dependencies:
```bash
sudo apt-get update
sudo apt-get install libpcap-dev
```

2. Clone the repository:
```bash
git clone https://github.com/yourusername/NIDS.git
cd NIDS
```

3. Compile the program:
```bash
g++ Intru.cpp -o nids  -lpcap -pthread
```

## Usage

1. Run the program with root privileges:
```bash
sudo ./nids
```

2. Enter the IP address you want to monitor when prompted.

3. The program will start monitoring network traffic and:
   - Display real-time traffic statistics
   - Log alerts to nids_log.txt
   - Show potential security threats

## Logging

The system automatically logs all events to `nids_log.txt`, including:
- Detected attacks
- Traffic statistics
- System errors
- Connection information

## Configuration

You can modify the following parameters in the code:
- `threshold`: Packet count threshold for anomaly detection (default: 100)
- Monitoring intervals
- Port definitions for attack detection

## Acknowledgments

- libpcap library developers
- Network security community
- Contributors and testers

