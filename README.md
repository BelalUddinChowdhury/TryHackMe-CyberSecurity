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

## Pre-Security: Network Fundamentals

### Task 1: Introduction to LAN Topologies
In this task, I explored **Network Topologies**, which define the geometric structure and layout of how devices connect and communicate within a Local Area Network (LAN). Understanding these structures is crucial for identifying structural vulnerabilities during security audits.

* **Star Topology:** Cost-efficient and the most common modern layout. Devices connect to a central **Switch**. Its critical flaw is that the switch represents a **Single Point of Failure (SPOF)**—if it goes down, the entire network collapses.
* **Bus Topology:** Legacy architecture where all devices share a single backbone cable. Data is broadcast to everyone, creating a significant **Packet Sniffing** risk for offensive actors.
* **Ring Topology:** Devices connect in a circular loop. If any single device or cable segment breaks, the entire network ring is severed and goes offline.
* **Mesh Topology:** Highly redundant and reliable as every device connects to every other device, but extremely **expensive** to implement and maintain.

#### Practical Lab Output (Topology Vulnerabilities Exposed):

<img width="948" height="858" alt="image" src="https://github.com/user-attachments/assets/a8c6e9f5-4f12-4a0f-a023-0e07b935fbed" />
#### Real-Life Application in Cybersecurity:
1. **Infrastructure Hardening (SPOF Identification):** As a security analyst, auditing network designs to ensure central switches or routers have redundant backups (Failovers) to prevent complete network blackouts during a DDoS attack or hardware failure.
2. **Lateral Movement Assessment:** Understanding how different topologies handle data transmission helps in predicting how malware or an attacker might pivot (move laterally) from a single compromised host to the rest of the enterprise network.

# 🌐 TryHackMe: OSI Model Challenge - Completed 🚀

I have successfully completed the **OSI Model** room on TryHackMe! This room covers the foundational 7 layers of the Open Systems Interconnection (OSI) model, their real-world applications in network communication, and how security analysts monitor or protect each layer.

---

## 🏛️ The 7 Layers of OSI Model & My Key Learnings

| Layer Number | Layer Name | Core Data Unit | My Practical Takeaways & Security Insights |
| :---: | :--- | :---: | :--- |
| **7** | **Application** | Data | Directly interacts with users via GUI or protocols (HTTP/S, FTP, DNS). **Security Focus:** Mitigating Layer 7 attacks like SQL Injection (SQLi) and Cross-Site Scripting (XSS) using Web Application Firewalls (WAF). |
| **6** | **Presentation**| Data | Acts as a network translator. Handles data formatting, standardization, and compression. **Security Focus:** Managing Data Encryption/Decryption (SSL/TLS). |
| **5** | **Session** | Data | Creates, maintains, and terminates communication paths between devices. Uses checkpoints to prevent data loss. **Security Focus:** Detecting Session Hijacking and Cookie Stealing. |
| **4** | **Transport** | Segments | Manages end-to-end data transmission using **TCP** (Reliable, error-checking) or **UDP** (Fast, connectionless). **Security Focus:** Monitoring Port Scanning activities (e.g., Nmap SYN scans). |
| **3** | **Network** | Packets | Handles logical addressing (**IP Addresses**) and determines the optimal path for data via routing protocols (OSPF, RIP). **Security Focus:** Implementing IP Blocking and Firewall Rules. |
| **2** | **Data Link** | Frames | Manages physical addressing (**MAC Addresses**) and packages packets into frames for local network switches. **Security Focus:** Preventing MAC Spoofing and setting up Port Security. |
| **1** | **Physical** | Bits | The hardware layer dealing with raw electrical/optical signals, cables (Copper/Fiber), and hubs. **Security Focus:** Preventing unauthorized physical wiretapping or access. |

---

## 🎮 Lab Practical: OSI Dungeon Escaped
As a final challenge in this room, I completed the **OSI Dungeon** hands-on lab game where I successfully navigated through the dungeon by correctly identifying and organizing all 7 layers of the OSI model in their exact hierarchical order.

**Captured Flag:** `THM{OSI_DUNGEON_ESCAPED}` ✅

---

## 🛠️ Skills Demonstrated
* Deep understanding of Network Architecture and Protocols.
* Knowledge of Defensive Security and traffic monitoring for a **SOC Analyst** perspective.
* Practical troubleshooting and core network-layer analysis.

* ## 📦 Module: Packets & Frames — Practical Lab Analysis

### 1. Transmission Control Protocol (TCP) Architecture
* **Stateful Connection Establishment (Three-Way Handshake):** Analyzed the precise mechanism used by end-hosts to synchronize and establish a reliable session.
  1. `SYN` (Synchronize): Client initiates the connection by transmitting a dynamic sequence number.
  2. `SYN-ACK` (Synchronize-Acknowledge): Server acknowledges the client's request and sends its own synchronization sequence.
  3. `ACK / DATA` (Established): Client sends the final acknowledgement packet, injecting the initial data payload into this frame to finalize the connection state.

* **Stateful Connection Teardown (Four-Way Handshake):** Simulated the graceful termination of a TCP session to prevent orphaned sockets or data loss.
  1. `FIN-ACK` (Client): Client requests session termination after completing data transmission.
  2. `ACK` (Server): Server acknowledges the termination request.
  3. `FIN-ACK` (Server): Server closes its downstream socket and sends its final close notification.
  4. `ACK` (Client): Client transmits the final `ACK` (`Okay, Goodbye`), transitioning the session into a closed state.

### 2. User Datagram Protocol (UDP) Mechanics
* **Stateless Communication:** Evaluated the operational logic of connectionless traffic, where data delivery tracking, sequence numbering, and acknowledgements are omitted to eliminate processing overhead.
* **Header Structure:** Investigated the minimal 8-byte UDP header configuration:
  * `Source Port` & `Destination Port`: Routing entry and exit points.
  * `Length`: Defines the total size of the UDP segment (header + payload).
  * `Checksum`: Provides optional integrity verification against bit-level corruption.
* **Use Cases:** Latency-sensitive environments such as live video streaming, DNS (Port 53), VoIP, and multiplayer online gaming.

### 3. Port Security & Layer 4 Service Binding
* **Well-Known Ports (0 - 1023):** Reviewed core protocol-to-port mappings critical for infrastructure security and firewall rule configuration:
  * `Port 21`: File Transfer Protocol (FTP)
  * `Port 22`: Secure Shell (SSH)
  * `Port 80`: HyperText Transfer Protocol (HTTP)
  * `Port 443`: HyperText Transfer Protocol Secure (HTTPS)
  * `Port 445`: Server Message Block (SMB)
* **Practical Challenge Implementation:** Conducted targeted socket connectivity testing to a specific host IP (`8.8.8.6`) on a non-standard port (`1234`), successfully verifying service responsiveness and retrieving the session flag: `THM{TCP_CHATTER}`.

* ---
### 🛠️ Lab Verifications & Artifacts
* **Simulation Environment:** TryHackMe Interactive Network Sandbox
* **Lab Completion Status:** 100% Successfully Completed
* **Captured Session Flag:** `THM{TCP_CHATTER}`

*"The best way to secure a network is to understand how it communicates from the ground up."* 💻🛡️


