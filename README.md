# README: Darktrace Malicious Activity Simulation

## Overview
This script simulates various cyber attacks to train Darktrace for detecting malicious activities in a controlled environment. It includes aggressive port scanning, malware traffic generation, SSH brute force attacks, data exfiltration, ARP spoofing, and ransomware-like file encryption.

### **Warning**
🚨 **Use this script in a controlled test environment only. Running this in a production network may cause security incidents and violate laws. Proceed with caution.** 🚨

## Prerequisites
Ensure you have the following installed on your system:

- Python 3.x
- Required Python libraries:
  - `scapy`
  - `requests`
  - `paramiko`
  - `socket`
  - `threading`

You can install missing dependencies using:
```bash
pip install scapy requests paramiko
```

## How to Run

1. **Modify Target IPs:**
   - Update the `target_ip` variable in the script with the IP address of the machine you want to simulate attacks on.
   - Update `gateway_ip` with the network gateway address.

2. **Run the Script:**
   ```bash
   python darktrace_malicious_sim.py
   ```

## Attack Simulations Included

1. **Aggressive Port Scanning**
   - Scans all 65535 ports on the target machine.

2. **Advanced Malware Traffic**
   - Sends simulated requests to malicious URLs.

3. **SSH Brute Force Attack**
   - Attempts login with common passwords and injects a malicious command if successful.

4. **Large-Scale Data Exfiltration**
   - Sends large volumes of data to an external fake server.

5. **ARP Spoofing with Packet Injection**
   - Manipulates ARP tables to intercept traffic.

6. **Ransomware-Like File Encryption**
   - Encrypts specified files using XOR encryption and deletes the originals.

## Stopping the Script
The script runs indefinitely due to continuous ARP spoofing. To stop it, press:
```bash
CTRL+C
```

## Disclaimer
This script is for cybersecurity training and testing **only**. Unauthorized usage may lead to severe legal consequences. Use responsibly in isolated test networks.

