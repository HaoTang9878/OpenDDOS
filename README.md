# OpenDDOS - Open-Source Network Stress Testing Toolkit

[中文说明](/README.zh-CN.md)  

## Overview

OpenDDOS is a comprehensive network testing toolkit built with Bash that provides an interactive menu interface for performing network reconnaissance and stress testing operations. The modular design supports testing across multiple protocols including TCP, UDP, and ICMP.

## Features

### Reconnaissance Module
- **Network Interface Detection** - Identify local and public IP addresses
- **DNS Reconnaissance** - Perform DNS queries and WHOIS lookups
- **Host Discovery** - ICMP ping sweeps for network mapping
- **Port Scanning** - Quick and comprehensive port scanning options
- **Service Identification** - Detect service versions and OS fingerprints
- **VPN Detection** - Identify IPsec VPN endpoints

### Stress Testing Module
- **ICMP Flood** - Traditional ping flood attacks
- **TCP Flood** - SYN/ACK/RST/XMAS flag combination attacks
- **UDP Flood** - High-bandwidth UDP packet floods
- **SSL/TLS Attacks** - Handshake exhaustion attacks
- **Slowloris** - Low-rate HTTP attacks
- **DNS Amplification** - NXDOMAIN query floods

### Data Transfer Utilities
- **File Transfer** - Send files via TCP/UDP
- **Network Listener** - Establish file reception services

## System Requirements

### Operating System
- Linux (Tested on Debian/Arch distributions)

## System Requirements  
- **Operating System**: Linux (Tested on Debian/Arch)  
- **Dependencies**:  
  - bash  
  - sudo  
  - curl  
  - netcat (with -k support)  
  - hping3/nping  
  - openssl  
  - stunnel  
  - nmap  
  - whois  
  - nslookup/host  
  - ike-scan  
  - bind-tools  

### Quick Installation  

- Download the script:

```
$ git clone https://github.com/HaoTang9878/OpenDDOS.git
```

- change dirctory to OpenDDOS :

```
$ cd OpenDDOS
```

- Set execution permissions for OpenDDOS :

```
$ chmod +x OpenDDOS
```
- Run it:

```
$ ./OpenDDOS
```

### Or Download Releases
Download the latest version from [Releases page](https://github.com/HaoTang9878/OpenDDOS/releases)

## Module Details
### Reconnaissance Features
- **Network Interface Detection**: Uses curl to query public IP, ip/ifconfig to display local IP
- **DNS Recon**: Performs forward/reverse DNS queries and WHOIS lookups
- **Quick Scan**: Uses nmap to scan 1000 common TCP ports
- **Comprehensive Scan**: Scans all TCP ports and identifies services/OS
- **UDP Scan**: Scans all UDP ports
- **Service Detection**: Estimates server uptime via TCP timestamps
- **VPN Detection**: Uses ike-scan to detect IPsec VPN servers

### Stress Testing
- **ICMP Flood**: Configurable source IP and packet size
- **TCP SYN Flood**: Configurable source IP, ports and data content
- **SSL Attack**: Resource exhaustion through massive SSL handshakes
- **Slowloris**: Slow HTTP header attack with SSL encryption support
- **DNS Flood**: Sends high volume NXDOMAIN queries

## Legal Disclaimer
⚠ **IMPORTANT LEGAL NOTICE** ⚠
1. This tool is **ONLY** for legally authorized security testing
2. Users must obtain **written authorization** from target systems
3. Developers are not responsible for any misuse
4. Prohibited for illegal network activities
By using this tool you agree to assume full responsibility.

## License
GNU General Public License v3.0

## Contribution Guidelines
Welcome to submit Pull Requests and Issues to report problems or suggest new features.

## Contact
- Author: Hao Tang
- GitHub: [@HaoTang9878](https://github.com/HaoTang9878)
- Project Home: https://github.com/HaoTang9878/OpenDDOS

---
_"With great power comes great responsibility."_ - Please use this tool responsibly.
