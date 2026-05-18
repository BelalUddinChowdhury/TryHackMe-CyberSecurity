# TryHackMe-CyberSecurity
# TryHackMe CyberSecurity Journey

## Pre-Security: What is Networking?

### Task 3: Identifying Devices on a Network
In this task, I learned the core differences between an IP Address and a MAC Address. I also practiced **MAC Spoofing** using an interactive lab, simulating how attackers modify their physical address to bypass network controls.

* **Logical Address:** IP Address (Can change dynamically)
* **Physical Address:** MAC Address (Unique identifier burnt into the hardware)

#### Practical Lab Output:
<img width="930" height="892" alt="image" src="https://github.com/user-attachments/assets/d1b179e8-6d96-436b-802b-82aa7ea9e68b" />

## Pre-Security: What is Networking?
### Task 4: Ping (ICMP)
In this task, I explored **Ping**, one of the most fundamental network diagnostics and troubleshooting tools used in cybersecurity. It utilizes the **ICMP (Internet Control Message Protocol)** to determine whether a remote host or server is active and reachable across a network.

* **ICMP Echo Request:** Sent by my machine to the target destination.
* **ICMP Echo Reply:** Received back from the target if it is online and configured to respond.
* **Network Metrics:** Analyzed **RTT (Round Trip Time)** to measure network latency and **TTL (Time to Live)** to understand the packet's lifespan across routers.

#### Practical Lab Output (Ping Success):
<img width="950" height="603" alt="Ping" src="https://github.com/user-attachments/assets/19a53496-ff9b-4497-8c39-14ec3f24679a" />\
#### Real-Life Application in Defensive Security (Blue Team):
1. **System Diagnostics (Alive Checks):** Instantly verifying if a critical enterprise database or server is online or completely crashed before initiating deeper troubleshooting.
2. **Command & Control (C2) Detection:** Monitoring network traffic logs for abnormal, highly repetitive ICMP signals (known as *C2 Beaconing*), which often indicates compromised internal hosts secretly communicating with an attacker's infrastructure.
3. **Flood Attack Mitigation:** Analyzing spikes in RTT and sudden packet drops to identify and defend against malicious ICMP flood patterns (DDoS/Ping Floods).


