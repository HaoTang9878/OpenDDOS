# OpenDDOS - Open-Source Network Stress Testing Toolkit
[中文说明](/README.zh-CN.md)  
**A Bash-based interactive menu tool for rapid network reconnaissance and stress testing**  
![OpenDDOS Logo](https://via.placeholder.com/150x50?text=OpenDDOS)

## Project Introduction  
OpenDDOS is a powerful network testing toolkit featuring an intuitive interactive menu interface that integrates multiple network reconnaissance and stress testing functions. Designed with modular architecture, it supports various protocol tests including TCP/UDP/ICMP.

## Features  
### Reconnaissance Module  
- **Network Interface Detection**: Displays local and public IP information  
- **DNS Reconnaissance**: Performs DNS queries and WHOIS lookups  
- **Host Discovery**: ICMP Ping sweeps across network segments  
- **Port Scanning**: Quick scan and comprehensive scan options  
- **Service Identification**: Detects service versions and operating systems  
- **VPN Detection**: Identifies IPsec VPN servers  

### Stress Testing Module  
- **ICMP Flood**: Traditional ICMP Echo flood attacks  
- **TCP Flood**: SYN/ACK/RST/XMAS flag combination attacks  
- **UDP Flood**: High-bandwidth UDP packet floods  
- **SSL/TLS Attacks**: Resource exhaustion through handshake process  
- **Slowloris**: Low-speed HTTP header attacks  
- **DNS Cache Poisoning**: NXDOMAIN query floods  

### Data Transfer  
- **File Transfer**: Sends files via TCP/UDP protocols  
- **Network Listener**: Establishes file receiving services  

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

## Installation  
### Quick Installation  
```bash  
git clone https://github.com/HaoTang9878/OpenDDOS.git  
cd OpenDDOS  
chmod +x OpenDDOS  
sudo ./OpenDDOS

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
