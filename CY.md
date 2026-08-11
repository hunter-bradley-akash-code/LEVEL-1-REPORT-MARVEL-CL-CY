# TASK: TryHackMe UVCE MARVEL Level 1(CL-CY) – Cybersecurity

---

## Introduction

As part of the MARVEL Level 1 activities, I completed the **UVCE MARVEL Level 1** room on TryHackMe. The room provided a practical introduction to important concepts in computer networking, operating systems, cryptography, and cybersecurity.

The tasks were divided into different sections covering networking fundamentals, network protocols, Windows, Linux, cryptography, the CIA triad, and basic red teaming concepts.

I completed all **26 tasks** in the room and gained a better understanding of how computers communicate over networks, how operating systems work, how data can be protected using cryptography, and how cybersecurity principles are applied in real-world situations.

---

## Objectives

The main objectives of completing this room were:

- To understand the fundamentals of computer networking.
- To learn how devices communicate using IP and MAC addresses.
- To understand ports, packets, frames, and networking devices.
- To learn the purpose of important network protocols.
- To understand basic Windows administration and security.
- To learn the basics of Linux and its file system.
- To understand fundamental cryptography concepts.
- To learn about the CIA triad in cybersecurity.
- To get an introduction to red teaming and offensive security concepts.
- To gain practical exposure to cybersecurity through TryHackMe.

---

# Section A – Fundamentals of Computer Networking

## Task 1: Introduction

In the first task, I learned the basic concepts of computer networking.

A computer network is a group of connected devices that communicate with each other and share information or resources. Networks can range from a small local network connecting computers in a home or office to large networks such as the Internet.

I understood that networking is an important foundation of cybersecurity because almost every modern system communicates over a network.

**Key concepts learned**
- Computer networks
- Devices communicating with each other
- Local and large-scale networks
- Network resources
- Importance of networking in cybersecurity

---

## Task 2: Internet

This task introduced me to the Internet and how different networks are connected together.

I learned that the Internet is a huge collection of interconnected networks. Devices communicate with remote systems using standardized networking protocols.

I also understood that when I access a website, my device communicates with servers through several networking components and protocols before receiving the requested information.

**Key concepts learned**
- Internet and interconnected networks
- Clients and servers
- Data communication
- Routing
- Internet infrastructure

---

## Task 3: IP Address

This task focused on IP addresses and how devices are identified on a network.

An IP address acts like an address for a device on a network. I learned about **IPv4** and **IPv6**, as well as the difference between private and public IP addresses.

For example:

```text
Private IP: 192.168.1.10
Public IP:  8.8.8.8
```

Private IP addresses are commonly used inside local networks, while public IP addresses are used to communicate over the Internet.

I also learned that IP addresses can change depending on the network and configuration.

**Key concepts learned**
- IPv4
- IPv6
- Private IP addresses
- Public IP addresses
- Network identification
- IP address allocation

---

## Task 4: Ports

In this task, I learned about ports and their importance in network communication.

A port helps identify a particular service or application running on a device. Different services commonly use different port numbers.

For example:

```text
HTTP  → 80
HTTPS → 443
SSH   → 22
DNS   → 53
```

I understood that checking open ports can help identify which services are running on a system. This is also important during security assessments because unnecessary or vulnerable services can increase the attack surface.

**Key concepts learned**
- Ports
- Services
- Common port numbers
- Open and closed ports
- Network attack surface

---

## Task 5: Packets & Frames

This task explained how data is transferred across a network.

Instead of sending a large amount of data as one piece, information is divided into smaller units. These units are processed and transmitted across the network.

I learned the difference between packets and frames and how they are used at different layers of network communication.

**Key concepts learned**
- Data transmission
- Packets
- Frames
- Network communication
- Encapsulation

Understanding packets and frames is also useful in cybersecurity because network traffic can be analysed to identify suspicious or unusual activity.

---

## Task 6: Networking Devices

In this task, I learned about common devices used in computer networks.

Some important networking devices include:

- Router
- Switch
- Hub
- Firewall
- Access Point

A router connects different networks and forwards traffic between them. A switch connects devices within a local network and forwards traffic to the appropriate device.

I also understood that firewalls play an important role in controlling network traffic based on security rules.

**Key concepts learned**
- Routers
- Switches
- Hubs
- Firewalls
- Access points
- Network traffic management

---

# Section B – Protocols

## Task 7: DNS

DNS stands for Domain Name System.

I learned that DNS converts human-readable domain names into IP addresses.

For example:

```text
example.com → IP address
```

Instead of remembering numerical IP addresses for every website, users can simply enter domain names.

I also understood that DNS is an important part of Internet communication because it allows systems to locate services using readable domain names.

**Key concepts learned**
- Domain names
- IP address resolution
- DNS servers
- Name resolution
- DNS queries

---

## Task 8: DHCP

DHCP stands for Dynamic Host Configuration Protocol.

I learned that DHCP automatically provides network configuration information to devices when they connect to a network.

This can include:

- IP address
- Subnet information
- Default gateway
- DNS server information

Without DHCP, network administrators would have to configure many network settings manually.

**Key concepts learned**
- Automatic IP assignment
- DHCP server
- Network configuration
- Default gateway
- DNS configuration

---

## Task 9: ICMP

ICMP stands for Internet Control Message Protocol.

I learned that ICMP is mainly used for network diagnostics and communication about network conditions.

A common example is the `ping` command, which uses ICMP to check whether a host is reachable.

ICMP can therefore be useful when troubleshooting network connectivity.

**Key concepts learned**
- ICMP
- Ping
- Network diagnostics
- Connectivity testing
- Error and control messages

---

## Task 10: HTTP(s)

This task introduced HTTP and HTTPS.

HTTP (Hypertext Transfer Protocol) is used for communication between web browsers and web servers.

HTTPS provides an encrypted connection using TLS, which helps protect data exchanged between the client and server.

I understood that HTTPS is important when transmitting sensitive information such as login credentials and personal information.

**Key concepts learned**
- HTTP
- HTTPS
- Web servers
- Web browsers
- Encryption
- TLS

---

## Task 11: Other Important Models

This task introduced other important networking models and concepts used to understand communication between systems.

I learned that networking can be divided into layers, with each layer performing a specific role.

The OSI model is one of the important models used to understand network communication. It consists of seven layers:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

Understanding these layers helps in troubleshooting network problems and understanding how different protocols work together.

---

# Section C – Windows

## Task 12: Introduction

This task introduced me to the Windows operating system from a cybersecurity perspective.

I learned about the Windows environment, its basic components, and how users interact with the operating system.

Windows is widely used in organizations, making knowledge of Windows administration and security important for cybersecurity professionals.

**Key concepts learned**
- Windows operating system
- Desktop environment
- System components
- User interaction
- Basic Windows administration

---

## Task 13: PowerShell

PowerShell is a command-line shell and scripting environment provided by Microsoft.

I learned that PowerShell can be used to perform administrative tasks, manage system resources, inspect information, and automate repetitive operations.

Unlike a traditional graphical interface, PowerShell allows many tasks to be performed directly through commands.

**Key concepts learned**
- PowerShell
- Command-line interface
- System administration
- Automation
- PowerShell commands

---

## Task 14: PowerShell vs CMD

This task helped me understand the difference between PowerShell and the traditional Windows Command Prompt (CMD).

CMD is an older command-line environment mainly designed for executing commands and batch scripts.

PowerShell is more advanced and is designed for administration and automation. It works with objects, which makes it more powerful for managing Windows systems.

| CMD | PowerShell |
|---|---|
| Older command-line environment | Modern command-line and scripting environment |
| Mainly text-based command output | Object-based pipeline |
| Batch scripting | Advanced scripting |
| Basic administration | Advanced administration and automation |

---

## Task 15: System32

In this task, I learned about the System32 directory in Windows.

System32 contains many important Windows system files, libraries, and executable programs required for the operating system to function properly.

I understood that modifying or deleting important system files without proper knowledge can cause serious problems.

**Key concepts learned**
- Windows system files
- System32 directory
- Executable files
- System functionality
- Importance of system directories

---

## Task 16: User Accounts & UAC

This task focused on Windows user accounts and User Account Control (UAC).

UAC helps prevent unauthorized changes to the system by asking for permission before certain administrative actions are performed.

I learned that different users can have different permissions and privileges, and controlling these permissions is an important part of system security.

**Key concepts learned**
- User accounts
- Administrator accounts
- User permissions
- Privileges
- User Account Control
- Least privilege

---

## Task 17: Security

This task introduced basic Windows security concepts.

I learned that securing a Windows system involves multiple layers of protection, including proper account management, permissions, updates, authentication, and security controls.

I also understood that security is not dependent on a single feature. Multiple security mechanisms should work together to reduce risks.

**Key concepts learned**
- System security
- Authentication
- Authorization
- Permissions
- Security controls
- Secure configuration

---

# Section D – Linux

## Task 18: Introduction

This task introduced me to the Linux operating system.

Linux is widely used in servers, cloud environments, networking systems, and cybersecurity.

I learned the basic Linux environment and the importance of using the command line to interact with the system.

**Key concepts learned**
- Linux operating system
- Terminal
- Command line
- Linux environment
- Basic system interaction

---

## Task 19: File Systems

This task introduced the Linux file system.

Unlike Windows, Linux uses a directory structure that begins at the root directory:

```text
/
```

Some important directories include:

- `/home`
- `/etc`
- `/var`
- `/tmp`
- `/usr`
- `/bin`

I learned that each directory has a specific purpose and that understanding the Linux file system is important for system administration and cybersecurity investigations.

**Key concepts learned**
- Linux root directory
- Files and directories
- File system structure
- Important Linux directories
- File management

---

# Section E – Others

## Task 20: Cryptography – Part 1

This task introduced the fundamentals of cryptography.

Cryptography is the process of protecting information so that unauthorized people cannot understand or modify it.

I learned about important concepts such as:

- Plaintext
- Ciphertext
- Encryption
- Decryption
- Keys

For example:

```text
Plaintext
   ↓
Encryption
   ↓
Ciphertext
   ↓
Decryption
   ↓
Plaintext
```

Cryptography is widely used to protect communication, files, passwords, and sensitive information.

---

## Task 21: Cryptography – Part 2

This task continued the concepts of cryptography and introduced more details about how cryptographic techniques are used.

I learned that cryptography can involve different types of algorithms and keys.

Two important categories are:

**Symmetric Cryptography**
The same key is used for encryption and decryption.

```text
Same key → Encrypt + Decrypt
```

**Asymmetric Cryptography**
Different keys are used:

- Public Key
- Private Key

The public key can be shared, while the private key must be kept secret.

I understood that cryptography is an important foundation of secure communication.

---

## Task 22: Cipher Breaker Challenge

This task provided a practical challenge based on cryptography.

Instead of only learning theoretical concepts, I had to apply what I learned about ciphers and encrypted information.

The challenge helped me understand that weak or simple encryption methods can sometimes be analysed and broken if enough information about the cipher is available.

**What I learned**
- Identifying encrypted text
- Understanding basic ciphers
- Applying cryptography concepts
- Analysing patterns
- Solving a practical security challenge

This was one of the more practical parts of the room because it required applying the concepts instead of only reading about them.

---

# Section F – Principles of CyberSecurity

## Task 23: CIA

This task introduced the CIA Triad, one of the most important concepts in cybersecurity.

CIA stands for:

- **C** – Confidentiality
- **I** – Integrity
- **A** – Availability

**Confidentiality**
Confidentiality means ensuring that information is accessible only to authorized users.

Examples include:
- Password protection
- Encryption
- Access control

**Integrity**
Integrity means ensuring that information is not modified or corrupted without authorization.

Examples include:
- File hashes
- Digital signatures
- Access controls

**Availability**
Availability means ensuring that systems and information are available when authorized users need them.

Examples include:
- Backups
- Redundant systems
- Disaster recovery
- Protection against denial-of-service attacks

The CIA triad helped me understand the three major goals of information security.

---

## Task 24: CIA – Explanation

This task provided a deeper understanding of the CIA triad.

I learned that cybersecurity is not only about keeping information secret. A secure system must also ensure that information remains accurate and that services remain available.

For example:

| Principle | Main Goal |
|---|---|
| Confidentiality | Prevent unauthorized access |
| Integrity | Prevent unauthorized modification |
| Availability | Keep systems and services accessible |

I understood that a security control can sometimes improve one aspect while affecting another, so organizations need to maintain a proper balance between all three principles.

---

# Section G – Red Teaming

## Task 25: Path 1 – Red Teaming

This task introduced the concept of Red Teaming.

A red team performs authorized security testing from an attacker's perspective. The objective is to identify weaknesses in systems, networks, applications, and processes so that they can be fixed.

I learned that red teaming is different from simply attacking a system. It is a controlled and authorized security activity carried out within a defined scope.

**General red team process**

```text
Reconnaissance
      ↓
Information Gathering
      ↓
Identifying Attack Surface
      ↓
Security Testing
      ↓
Assessment
      ↓
Reporting
```

The goal is to help an organization understand how an attacker could potentially compromise its environment.

**Key concepts learned**
- Red team
- Offensive security
- Attack surface
- Attack vectors
- Security assessment
- Authorized testing
- Reporting

---

## Task 26: Red Teaming Continuation

The final task continued the introduction to red teaming and helped me understand how offensive security fits into the larger cybersecurity process.

I learned that identifying a vulnerability is only one part of a security assessment. The findings need to be documented and communicated so that organizations can take corrective action.

I also understood the importance of conducting security testing only with proper authorization and within the defined scope.

**Key concepts learned**
- Red team methodology
- Attack surface
- Vulnerability identification
- Security assessment
- Risk awareness
- Responsible security testing
- Reporting and remediation

---

## Overall Learning

After completing all 26 tasks, I gained a strong foundation in several important areas of cybersecurity.

The main concepts I learned were:

**Networking**
- IP addresses
- IPv4 and IPv6
- Private and public IP addresses
- Ports
- Packets and frames
- Routers and switches
- DNS
- DHCP
- ICMP
- HTTP and HTTPS
- Network models

**Windows**
- Windows basics
- PowerShell
- CMD
- System32
- User accounts
- UAC
- Windows security

**Linux**
- Linux basics
- Terminal
- File system
- Linux directories
- Basic system interaction

**Cryptography**
- Encryption
- Decryption
- Plaintext and ciphertext
- Symmetric cryptography
- Asymmetric cryptography
- Cipher analysis

**Cybersecurity**
- CIA Triad
- Confidentiality
- Integrity
- Availability
- Attack surface
- Attack vectors
- Red teaming
- Security assessment

---

## Conclusion

Completing the UVCE MARVEL Level 1 TryHackMe room gave me a practical introduction to cybersecurity and helped me connect theoretical concepts with hands-on learning.

The networking section helped me understand how devices communicate and how protocols such as DNS, DHCP, ICMP and HTTP/HTTPS work. The Windows and Linux sections improved my understanding of operating systems and command-line environments.

The cryptography tasks helped me understand how information can be protected, while the CIA Triad introduced the fundamental security goals of confidentiality, integrity, and availability.

Finally, the red teaming section gave me an introduction to offensive security and showed me how security professionals think from an attacker's perspective while working within an authorized environment.

Overall, this room helped me build a strong foundation in networking, operating systems, cryptography, and cybersecurity principles, and it also gave me more confidence in exploring practical cybersecurity challenges.

**I successfully completed all 26 tasks in the UVCE MARVEL Level 1 room (Room completed: 100%).**
