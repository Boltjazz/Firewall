# Firewall

This Python script implements a basic intrusion detection and prevention system (IDS/IPS) using `scapy` for packet sniffing and `iptables` for blocking/unblocking IP addresses. It monitors network traffic for suspicious activity, such as SYN scans, and dynamically blocks offending IPs.

## Features

- **Real-Time Packet Monitoring**: Uses `scapy` to sniff TCP packets and detect SYN scans.
- **Dynamic IP Blocking**: Blocks IPs exhibiting suspicious behavior using `iptables`.
- **Time-Based Unblocking**: Automatically unblocks IPs after a configurable block duration (default: 10 minutes).
- **Multi-Threading**: Separates packet sniffing and unblock monitoring into different threads for efficiency.

## Prerequisites

1. **Python**: Ensure Python 3.x is installed.
2. **Dependencies**: Install the required Python libraries:
   ```bash
   pip install scapy