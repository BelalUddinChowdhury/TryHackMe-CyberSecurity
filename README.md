# TryHackMe: Pre-Security Learning Path - Comprehensive Lab Notes

This repository contains objective technical documentation, structural notes, and practical outcomes from the Pre-Security learning path on TryHackMe. The content is organized by module, tracking the theoretical blueprints and hands-on exercises executed throughout the curriculum.

---

## 🏛️ Module 1: Introduction to Cyber Security

### 1. Offensive Security
* **Introduction:** Overview of testing security postures by actively identifying vulnerabilities and misconfigurations from an external adversary's perspective.
* **Theory:** Focuses on the core stages of an attack lifecycle: reconnaissance, vulnerability identification, exploitation, and post-exploitation reporting.
* **Lab/Practical:** Interfaced with web applications to observe how automated parameter tampering bypasses standard client-side visibility boundaries.
* **Conclusion:** Defensive teams must analyze offensive testing methodologies to anticipate attacker vectors and secure misconfigured entrance points.

### 2. Defensive Security
* **Introduction:** Focuses on standard corporate infrastructure defense, threat detection, and active blue-team incident response.
* **Theory:** Analyzes log management, security information event monitoring (SIEM), system auditing, and the application of proactive security controls.
* **Lab/Practical:** Analyzed live attack telemetry logs inside a mock Security Operations Center (SOC) dashboard to isolate malicious IP requests.
* **Conclusion:** Effective defense requires complete network visibility, structured log retention, and continuous configuration auditing.

---

## 🌐 Module 2: Network Fundamentals

### 3. Networking & Infrastructure
* **Introduction:** Analysis of enterprise network nodes, data transport mechanisms, and fundamental topologies.
* **Theory:** Examines IP addressing structures (IPv4/IPv6), subnet masks, default gateways, and the functional role of routers and switches.
* **Lab/Practical:** Mapped internal asset structures, identifying configuration flaws in routing tables that allowed unauthenticated access across zones.
* **Conclusion:** Proper segmenting of enterprise networks isolates compromised subnets and limits lateral movement by an attacker.

### 4. Local Area Networks (LAN)
* **Introduction:** Examining internal corporate network architectures, media access controls, and local broadcast domains.
* **Theory:** Covers MAC addressing, Address Resolution Protocol (ARP) handshakes, DHCP lease assignments, and local network boundary separation.
* **Lab/Practical:** Traced local interface handshakes to verify how network nodes map IP addresses to physical hardware addresses.
* **Conclusion:** Securing local domains against unauthenticated device connections prevents inner-perimeter network sniffing and spoofing attacks.

### 5. The OSI Model
* **Introduction:** Theoretical standardization of data communication protocols across isolated processing layers.
* **Theory:** Deep-dive into the 7-layer architecture (Physical, Data Link, Network, Transport, Session, Presentation, Application) and their respective encapsulation processes.
* **Lab/Practical:** Traced a mock network data request layer-by-layer to monitor how application payloads are progressively encapsulated down to physical signals.
* **Conclusion:** Understanding the exact encapsulation layer isolates where network failure or malicious traffic injection occurs during investigations.

### 6. Packets & Frames
* **Introduction:** Structural analysis of data segments moving across physical media and logical networks.
* **Theory:** Examines the composition of layer 2 frames (MAC headers) and layer 3 packets (IP headers, flags, Time-to-Live metrics, and payload areas).
* **Lab/Practical:** Parsed structural data packets to identify anomalies in payload size and header flag manipulation.
* **Conclusion:** Granular packet header analysis is a critical requirement for configuring signature-based Intrusion Detection Systems (IDS).

---

## 💻 Module 3: How the Web Works

### 7. Domain Name System (DNS)
* **Introduction:** Examination of internet name-to-IP resolution mechanisms and the globally distributed DNS hierarchy.
* **Theory:** Covers root servers, Top-Level Domains (TLD), authoritative name servers, and critical record types (A, AAA, CNAME, MX, TXT).
* **Lab/Practical:** Querying and resolving specific server domain addresses to verify exact IP destination records.
* **Conclusion:** Monitoring anomalous DNS lookup queries is vital for identifying command-and-control (C2) communication channels.

### 8. HTTP/S Protocols
* **Introduction:** Standardized review of web client-server communication models and secure transport layers.
* **Theory:** Analyzes HTTP request methods (GET, POST), request/response headers, status code distributions (200, 301, 403, 404), and SSL/TLS asymmetric key encryption handshakes.
* **Lab/Practical:** Monitored web server traffic code patterns to trace parameter routing and check secure certificate verifications.
* **Conclusion:** Enforcing HTTPS ensures transport-layer confidentiality, mitigating eavesdropping and Man-in-the-Middle (MitM) data modification risks.

### 9. Website Workings & Frameworks
* **Introduction:** Analysis of frontend presentation code and backend server logic components.
* **Theory:** Covers the rendering interaction between HTML structures, CSS styling, client-side JavaScript execution, and backend database query processing.
* **Lab/Practical:** Inspected source code structures within a web application to find misconfigured hidden paths omitted from main site maps.
* **Conclusion:** Proper sanitization of frontend-rendered parameters is necessary to secure web interfaces from exploitation.

---

## 🖥️ Module 4: Computer Fundamentals

### 10. Computer Systems
* **Introduction:** Low-level architectural baseline of hardware processing, memory allocation, and operating system control layers.
* **Theory:** Analyzes the physical interaction between the CPU, RAM execution states, hard drive registers, and kernel-level hardware coordination.
* **Lab/Practical:** Monitored active system resources to observe memory utilization metrics and kernel processing workloads.
* **Conclusion:** Solid baseline knowledge of system architectures is essential for analyzing resource exhaustion and software-level crashes.

### 11. Computer Types & Architectures
* **Introduction:** Structural differentiation between personal workstations, heavy enterprise servers, and embedded architecture platforms.
* **Theory:** Explores performance parameters, server rack distributions, file server configurations, and system stability metrics under enterprise loads.
* **Lab/Practical:** Classified diverse infrastructure assets based on processing capability, system roles, and network data throughput demands.
* **Conclusion:** Aligning hardware architecture types with specific corporate tasks optimizes resource monitoring boundaries.

### 12. Client-Server Models
* **Introduction:** Centralized computing model managing service distribution across distributed nodes.
* **Theory:** Covers request-response lifecycles, dedicated server resource handling, concurrent connection states, and client access controls.
* **Lab/Practical:** Configured a mock client terminal to establish verified connections to centralized network storage and web hosting units.
* **Conclusion:** Securing the central server hub against unauthenticated client requests prevents multi-node network degradation.

### 13. Virtualization Technology
* **Introduction:** Examination of software-driven hardware abstraction layers running multiple isolated computing instances.
* **Theory:** Explores Type-1 (Bare Metal) and Type-2 (Hosted) Hypervisor architectures, virtual hardware assignment, and guest OS isolation boundaries.
* **Lab/Practical:** Managed and ran independent virtual instances inside a sandboxed hypervisor container to isolate test workloads.
* **Conclusion:** Virtualized environments provide safe, snapshot-capable sandboxes to analyze malware and test configurations without risking physical infrastructure.

### 14. Cloud Computing
* **Introduction:** Distributed, off-site resource allocation and utility-based infrastructure management models.
* **Theory:** Covers Infrastructure as a Service (IaaS), Platform as a Service (PaaS), Software as a Service (SaaS), and shared responsibility security matrix frameworks.
* **Lab/Practical:** Audited vendor vs. client security boundaries across different cloud service deployments to map data ownership.
* **Conclusion:** Cloud configurations require strict Identity and Access Management (IAM) controls to prevent public exposure of private corporate datastores.

---

## 💾 Module 5: Operating Systems

### 15. Windows OS Architecture
* **Introduction:** Enterprise operating system internals, access management, and system auditing mechanics.
* **Theory:** Covers the Windows Registry database, file permissions (NTFS), active system processes, and the Event Viewer logging architecture.
* **Lab/Practical:** Searched internal system registers and user directories to locate active execution parameters and process origins.
* **Conclusion:** Monitoring Windows event logs is a fundamental requirement for tracking unauthorized permission changes or local privilege escalation attempts.

### 16. Linux OS Architecture
* **Introduction:** Open-source operating system layout, command-line management, and file permission structures.
* **Theory:** Focuses on the Linux directory standard, root privilege management, and using core CLI utilities (`ls`, `cd`, `find`, `grep`) for administration.
* **Lab/Practical:** Operated live inside a Linux CLI to parse system files and monitor host specifications using native commands:
  * `uname -a`: Verified host system kernels and core hardware architectures (`x86_64`).
  * `df -h`: Monitored storage capacity layouts in human-readable notation.
  * `cat`: Extracted raw configuration file payloads directly to the terminal interface.
* **Conclusion:** Command-line efficiency is a prerequisite for parsing Linux server security logs and running remote incident response tasks.

### 17. OS Security Hardening
* **Introduction:** Implementing security configurations to decrease the local attack surface of an operating system.
* **Theory:** Covers disabling unnecessary services, configuring local host firewalls, enforcing strong password rules, and keeping patch cycles up to date.
* **Lab/Practical:** Audited a default operating system configuration to close open vulnerabilities, block unused ports, and restrict user accounts.
* **Conclusion:** Consistent system-level hardening is the first defense line against local exploitation and lateral network attacks.

---

## ⚙️ Module 6: Software Basics

### 18. Data Representation
* **Introduction:** Fundamental systems used by computers to process, store, and display information.
* **Theory:** Covers numerical bases including Binary (base 2), Decimal (base 10), and Hexadecimal (base 16), and how processors read machine logic states.
* **Lab/Practical:** Converted plain text indicators into binary streams and hexadecimal values to map exact data storage values.
* **Conclusion:** Reading hexadecimal values is necessary for analyzing low-level memory states and raw file signatures during forensics.

### 19. Data Encoding Mechanics
* **Introduction:** Reversible text formatting transformations used for standardized data transmission and storage.
* **Theory:** Analyzes encoding standards like ASCII, UTF-8, URL encoding, and Base64, emphasizing that encoding is for compatibility, not security.
* **Lab/Practical:** Decoded obfuscated script payloads from Base64 and URL-encoded formats back into plaintext to view the source code.
* **Conclusion:** Recognizing encoding patterns allows analysts to decode obfuscated web payloads and spot evasion attempts by hyaackers.

### 20. Python Scripting Logic
* **Introduction:** High-level scripting logic used for task automation and log analysis.
* **Theory:** Covers basic syntax structures, data types, variable declarations, procedural loops (`for`/`while`), and conditional blocks (`if`/`else`).
* **Lab/Practical:** Reviewed core procedural code structures to understand log parsing logic and automation playbook workflows.
* **Conclusion:** Developing Python literacy allows security teams to automate repetitive data parsing and threat monitoring scripts.

### 21. JavaScript Execution
* **Introduction:** Client-side scripting language used to drive web browser interaction and logic.
* **Theory:** Focuses on Document Object Model (DOM) manipulation, client-side input checking, and how browsers process script elements.
* **Lab/Practical:** Inspected client-side web variables and functions to trace data handling and identify broken logic flows.
* **Conclusion:** Understanding JavaScript mechanics is vital for analyzing Cross-Site Scripting (XSS) and client-side web bypass vectors.

### 22. Database & SQL Infrastructure
* **Introduction:** Relational storage systems and the structured queries used to manage records.
* **Theory:** Covers tables, relational indexing, primary keys, and structured query language syntax (SELECT, INSERT, UPDATE, WHERE).
* **Lab/Practical:** Interfaced with a relational datastore using SQL queries to filter table rows and audit specific dataset fields.
* **Conclusion:** Mastery of database structures is needed to audit user access, verify record changes, and detect SQL Injection attempts.

---

## 📊 Module 7: Attacks and Defenses

### 23. The CIA Triad
* **Introduction:** The core framework that guides information security policy design and incident classification.
* **Theory:** Defining Confidentiality (preventing unauthorized reading), Integrity (preventing unauthorized changing), and Availability (ensuring uptime).
* **Lab/Practical:** Evaluated data breaches step-by-step to classify the main target pillar and determine the incident severity score.
* **Conclusion:** Using the CIA Triad allows incident response teams to prioritize mitigations based on the type of impact.

### 24. Practical Cryptography
* **Introduction:** Mathematical frameworks used to secure data secrecy and ensure authentication.
* **Theory:** Explores symmetric key systems, public/private key distributions (asymmetric), cryptographic hash functions (MD5, SHA-256), and key-space sizing.
* **Lab/Practical:** Checked file hashes to ensure files were not tampered with and evaluated cipher mechanisms against simple frequency attacks.
* **Conclusion:** Strong cryptographic deployments ensure data-in-transit confidentiality and verify data-at-rest integrity.

### 25. Hacking & Automated Exploitation
* **Introduction:** Analysis of tactical security bypasses using automated scanning and brute-forcing utilities.
* **Theory:** Covers path discovery via wordlists and brute-force authentication testing against login fields using dictionary files.
* **Lab/Practical:** Executed an automated attack workflow within a live sandbox environment:
  * **Gobuster:** Ran path brute-forcing to discover an unlinked, hidden administrative login portal (`/login`).
  * **Hydra:** Deployed automated dictionary attacks targeting the form's failed string parameter until the exact credential was isolated.
* **Conclusion:** Understanding automated attack patterns allows defenders to configure rate-limiting policies and signature rules.

### 26. Defending & Incident Response
* **Introduction:** Continuous monitoring, active threat mitigation, and data restoration workflows.
* **Theory:** Covers multi-layered defense frameworks, containment strategies, log tracking, and data integrity verification.
* **Lab/Practical:** Evaluated a database breach scenario. Checked data Integrity by systematically comparing the compromised tables against a known good backup to isolate corrupted records before service restoration.
* **Conclusion:** Incident response requires rapid containment actions followed by thorough data verification to ensure reliable recovery.
