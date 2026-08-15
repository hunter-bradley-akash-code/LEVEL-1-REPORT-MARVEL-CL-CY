# CY – Cybersecurity
## UVCE MARVEL Level 1 – TryHackMe
- - -
### **Task 1: Fundamentals of Computer Networking: Introduction**

This task introduced the basic concept of a **network** and how different things can be connected together. A network is not limited to computers. Examples include bus and train systems, electricity grids, postal systems, and even social groups.

In computing, networks connect devices such as phones, laptops, security cameras, traffic lights, and modern machines. A network can be as small as two devices sharing files or as large as billions of devices connected through the Internet.

I learned that networks are involved in almost everything we use today. Since many important systems depend on networks, understanding how they work is an important foundation for cybersecurity.

**Main takeaway:** A network is simply a collection of connected devices or systems that communicate and share information.

---

### **Task 2: Fundamentals of Computer Networking: Internet**

This task explained how the **Internet** developed and how it works as a global network.

The Internet began with **ARPANET**, a project funded by the U.S. Defence Department in the late 1960s. Later, in 1989, **Tim Berners-Lee** created the **World Wide Web (WWW)**, which made sharing and accessing information through the Internet much easier.

I also learned that the Internet can be described as a **network of networks**. Many smaller private networks are connected together to form the large public network that we use today.

The task also introduced the difference between **private networks** and the **public network (Internet)**.

**Main takeaway:** The Internet is a huge collection of interconnected networks that allows devices around the world to communicate.

---

### **Task 3: Fundamentals of Computer Networking: IP Address**

This task explained how devices identify each other on a network using **IP addresses** and **MAC addresses**.

An **IP address** works like a name for a device on a network. It can change depending on the network or configuration. An example of an IPv4 address is `192.168.1.10`.

I learned about **private IP addresses**, which are used inside local networks, and **public IP addresses**, which are used for communication over the Internet. The task also introduced **IPv6**, which was developed because the number of available IPv4 addresses was limited.

A **MAC address** is associated with the network hardware and can be thought of as a device's fingerprint. However, it can be copied using **MAC spoofing**, so it should not be treated as a completely reliable security mechanism.

The questions helped me understand the difference between IP addresses, MAC addresses, private and public IPs, and MAC spoofing.

**Main takeaway:** IP addresses identify devices on a network, while MAC addresses identify network interfaces at the hardware level.

---

### **Task 4: Fundamentals of Computer Networking: Ports**

This task introduced **network ports** and their role in communication.

Ports are numbered communication channels ranging from **0 to 65535**. They help the operating system determine which application or service should handle incoming network traffic.

Some common ports are:

* **21** – FTP
* **22** – SSH
* **80** – HTTP
* **443** – HTTPS

The task also explained that the well-known ports from **0 to 1024** are commonly associated with standard services.

From a cybersecurity perspective, I understood that open ports can act as potential entry points into a system. Services running on unnecessary or poorly secured ports can increase the attack surface.

**Main takeaway:** Ports help direct traffic to the correct application, but unnecessary open ports can create security risks.

---

### **Task 5: Fundamentals of Computer Networking: Packets and Frames**

This task explained how data is transferred across a network by breaking it into smaller units.

At the **Network Layer**, data is handled as **packets**, while at the **Data Link Layer**, packets are encapsulated into **frames**.

Packets contain information such as:

* Source IP address
* Destination IP address
* Data payload
* Checksum
* Time To Live (TTL)

The **TTL** value prevents packets from circulating endlessly around a network. Each router decreases the TTL, and when it reaches zero, the packet is discarded.

Breaking data into smaller packets also improves network efficiency. If part of a transmission is lost, only the required data needs to be retransmitted instead of the entire file.

**Main takeaway:** Packets and frames allow large amounts of data to be transmitted efficiently across different network layers.

---

### **Task 6: Fundamentals of Computer Networking: Networking Devices**

This task introduced the main devices used to connect and secure networks.

A **Hub** operates at Layer 1 and broadcasts incoming data to all connected devices. A **Switch** mainly operates at Layer 2 and uses MAC addresses to forward data to the correct device.

A **Router** operates at Layer 3 and connects different networks using IP addresses. It can also perform functions such as NAT and DHCP.

I also learned about:

* **Access Points** – connect wireless devices to a network.
* **Multilayer Switches** – combine Layer 2 switching and Layer 3 routing.
* **Firewalls** – filter network traffic according to security rules.
* **IDS/IPS** – detect suspicious activity and, in the case of IPS, block threats.
* **VPNs** – create encrypted tunnels for secure communication.

The task helped me understand that different networking devices have different roles depending on the layer and purpose.

**Main takeaway:** Networking devices are responsible for connecting systems, directing traffic, and protecting networks from unwanted access.

---

### **Task 7: Protocols: DNS**

This task introduced the **Domain Name System (DNS)**, which can be thought of as the phonebook of the Internet.

DNS converts human-readable domain names into IP addresses. For example:

```text
google.com → IP address
```

This is important because remembering IP addresses for every website would be impractical. DNS allows users to simply enter a domain name while the system handles the IP address lookup in the background.

I also completed the DNS questions and used **nslookup** to perform DNS lookup experiments with different DNS servers.

**Main takeaway:** DNS makes the Internet easier to use by translating domain names into the IP addresses required for communication.

---

### **Task 8: Protocols: DHCP**

This task explained **Dynamic Host Configuration Protocol (DHCP)** and how devices automatically receive network configuration.

DHCP follows a four-step process called **DORA**:

1. **Discover** – The client broadcasts to find a DHCP server.
2. **Offer** – The server offers an available IP address.
3. **Request** – The client requests the offered IP address.
4. **Acknowledge** – The server confirms the IP allocation.

Initially, the client does not have an IP address and uses:

```text
0.0.0.0
```

It communicates using broadcast addresses, including the broadcast MAC address:

```text
ff:ff:ff:ff:ff:ff
```

After the DHCP process, the device receives important configuration such as:

* IP address
* Default gateway
* DNS server

I also learned how to view network configuration using:

```text
ipconfig /all
```

on Windows and:

```text
ip a
```

on Linux.

For renewing the DHCP lease on Windows, the commands covered were:

```text
ipconfig /release
ipconfig /renew
```

The task also introduced **APIPA**, which can be automatically assigned when a DHCP server is unavailable.

**Main takeaway:** DHCP automatically provides the network configuration required for a device to communicate without manually entering every setting.

---

### **Task 9: Protocols: ICMP**

This task introduced the **Internet Control Message Protocol (ICMP)**, which is mainly used for network diagnostics and error reporting.

One of the most common tools using ICMP is **ping**. Ping sends an **Echo Request** and waits for an **Echo Reply** to determine whether a host is reachable. It can also measure **Round-Trip Time (RTT)** and packet loss.

The task also explained **traceroute**. It works by manipulating the **TTL** value of packets. Each router decreases the TTL by one. When the TTL reaches zero, the router drops the packet and sends an **ICMP Time Exceeded (Type 11)** message.

This allows each hop along the route to reveal itself. Sometimes traceroute can display `* * *` because routers may not respond or ICMP messages may be blocked.

**Main takeaway:** ICMP is useful for diagnosing network connectivity and understanding the path packets take between systems.

---

### **Task 10: Protocols: HTTP (S)**

This task covered **HTTP (HyperText Transfer Protocol)** and **HTTPS (HyperText Transfer Protocol Secure)**.

HTTP is the protocol used for communication between a web browser and a web server. The browser sends requests and the server responds with resources such as HTML pages, images, and other content.

**HTTPS** is the secure version of HTTP. It uses **SSL/TLS** to encrypt communication between the client and server. This helps prevent attackers from reading data being transmitted and also provides server authentication.

I tested both HTTP and HTTPS by visiting `example.com` using separate browser tabs. I also explored the browser's **Developer Tools → Network** section to understand the requests made by the browser.

The task also introduced SSL/TLS certificate information, including the **Certificate Authority (CA)** and **Common Name (CN)** of websites.

**Main takeaway:** HTTP provides normal web communication, while HTTPS adds encryption and authentication to protect the communication.

---

### **Task 11: Protocols: Other Important Models**

This task introduced the **OSI model**, which provides a structured way to understand how network communication takes place.

The seven OSI layers are:

1. Physical
2. Data Link
3. Network
4. Transport
5. Session
6. Presentation
7. Application

I also learned how **TCP** and **UDP** operate at the Transport Layer. TCP provides reliable communication using mechanisms such as sequence numbers and error checking, while UDP is simpler and faster but does not provide the same level of reliability.

The task explained how data is encapsulated as it moves through the layers. An HTTP request starts at the Application Layer, then TCP adds transport information, IP adds source and destination addresses, and the Data Link Layer adds MAC information before the data is transmitted as bits.

The questions helped reinforce that TCP adds sequence numbers, IP is responsible for routing between networks, and frames are created at the Data Link Layer.

**Main takeaway:** The OSI model is a useful framework for understanding where different protocols and networking functions operate.

---

### **Task 12: Windows: Introduction**

This task introduced the **Windows operating system** and basic system management.

I learned how Windows organizes information using a hierarchical folder structure. Common locations such as **Desktop, Documents, and Downloads** help users organize their files, while **File Explorer** provides an easy way to navigate through them.

The task also covered important system maintenance practices.

**Windows Update** helps:

* Fix security vulnerabilities
* Improve performance
* Resolve bugs and crashes

I also learned about installing applications from trusted sources, uninstalling unused applications, and the difference between **Windows Settings** and **Control Panel**.

**Task Manager** was also introduced as a tool for monitoring the system. It provides information about processes, CPU and memory usage, users, process IDs, and services.

**Main takeaway:** Basic Windows administration is important for keeping a system reliable, updated, and secure.

---

### **Task 13: Windows: PowerShell**

This task introduced **PowerShell**, a command-line shell, scripting language, and automation framework developed by Microsoft.

PowerShell is built on the **.NET framework** and works with **objects** instead of only plain text. Objects contain properties that describe information and methods that allow actions to be performed.

I learned that PowerShell was designed by **Jeffrey Snover** to improve Windows administration and automation. PowerShell was initially released for Windows, while **PowerShell Core** was later introduced as a cross-platform and open-source version.

Important concepts covered included:

* Cmdlets
* Objects
* Properties
* Methods
* Automation
* Configuration management
* Cross-platform support

**Main takeaway:** PowerShell provides much more powerful system administration and automation capabilities than a traditional command shell.

---

### **Task 14: Windows: PowerShell vs CMD**

This task compared **Command Prompt (CMD)** with **PowerShell**.

CMD is an older command shell that is mainly useful for basic commands and batch scripts. It works mostly with text-based output and was not designed for advanced remote system administration.

PowerShell is a more modern administration environment. It uses **cmdlets**, works with objects, supports complex scripts, and can perform remote administration.

I also learned that many traditional CMD commands can still be used in PowerShell through **aliases**. The `Get-Alias` command can be used to check these command mappings.

PowerShell can also access Windows components such as the registry, file system, and Windows Management Instrumentation (WMI).

**Main takeaway:** CMD is suitable for simple command-line tasks, while PowerShell is better suited for advanced administration, automation, and scripting.

---

### **Task 15: Windows: System32**

This task explained the **Windows directory** and the importance of the **System32** folder.

The Windows directory is normally located at:

```text
C:\Windows
```

The system can locate this directory dynamically using the environment variable:

```text
%windir%
```

The Windows directory contains many important subfolders, with **System32** being one of the most critical.

System32 contains essential Windows system files, utilities, and executable programs required for the operating system to function properly.

Because these files are important, modifying or deleting files inside System32 can cause serious system problems.

**Main takeaway:** The Windows directory contains core operating system components, and System32 must be handled carefully because it is essential to Windows.

---

### **Task 16: Windows: User Accounts & UAC**

This task covered **Windows user accounts**, user profiles, groups, and permissions.

The two main types of Windows accounts are:

* **Administrator** – has permission to make system-wide changes.
* **Standard User** – has more limited permissions and mainly manages personal files and applications.

User profiles are stored under:

```text
C:\Users\
```

For example:

```text
C:\Users\Max
```

I also learned about **Local Users and Groups Management**, which can be opened using:

```text
lusrmgr.msc
```

Groups can contain multiple users and allow permissions to be managed more efficiently.

The task also introduced the importance of controlling administrative privileges. Limiting unnecessary privileges helps reduce the impact of accidental or malicious changes.

**Main takeaway:** User accounts, groups, and permissions are important parts of Windows security because they control what each user can access or modify.

---

### **Task 17: Windows: Security**

This task introduced the built-in security features available in Windows.

Important Windows Security features include:

* **Virus & threat protection** – detects and protects against malware.
* **App & browser control** – helps prevent unsafe applications and websites.
* **Device security** – provides additional protection for the device.
* **Windows Firewall** – controls network traffic entering and leaving the system.

The Windows Firewall uses different network profiles:

* **Domain**
* **Private**
* **Public**

A **Public** network is considered less trusted than a Private network, such as a home network.

The task also reinforced the importance of keeping Windows and applications updated and installing software only from trusted sources.

**Main takeaway:** Windows security depends on several layers of protection working together rather than relying on one security feature.

---

### **Task 18: Linux: Introduction**

This task introduced **Linux** and its importance in modern computing.

Linux is not one single operating system. It is an open-source platform used as the foundation for many different **distributions**, also called distros.

Some popular distributions include:

* Ubuntu
* Debian

Linux is widely used in:

* Web servers
* Automotive systems
* Retail Point of Sale systems
* Traffic light systems
* Industrial sensors
* Critical infrastructure

One of the main advantages of Linux is that it is lightweight, flexible, and customizable. Ubuntu can be used as both a desktop and server operating system.

**Main takeaway:** Linux is widely used in servers and critical systems, making Linux knowledge very important in cybersecurity.

---

### **Task 19: Linux: File Systems**

This task introduced practical **Linux file and directory management**.

Some important commands covered were:

| Command | Purpose                       |
| ------- | ----------------------------- |
| `ls`    | Lists directory contents      |
| `find`  | Searches for files            |
| `cd`    | Navigates between directories |
| `touch` | Creates a file                |
| `mkdir` | Creates a directory           |
| `cp`    | Copies files or directories   |
| `mv`    | Moves or renames files        |
| `rm`    | Deletes files or directories  |
| `file`  | Identifies the type of a file |

For example:

```bash
touch note
mkdir mydirectory
cp note note2
mv note2 note3
rm note
```

A directory can be removed recursively using:

```bash
rm -R mydirectory
```

The task also explained that Linux does not depend entirely on file extensions to identify a file. The `file` command can be used to determine what type of data a file actually contains.

**Main takeaway:** Knowing basic Linux file commands is essential for working with Linux systems and is especially useful during cybersecurity investigations and practical tasks.

---

### **Task 20: Cryptography - Part 1**

This task introduced the basic concepts of **cryptography** and how it protects information.

Cryptography helps provide **confidentiality, integrity, and authenticity** when information is stored or transmitted.

The basic process is:

```text
Plaintext + Key → Encryption → Ciphertext
Ciphertext + Key → Decryption → Plaintext
```

I learned the following important terms:

* **Plaintext** – original readable information.
* **Ciphertext** – encrypted and unreadable information.
* **Cipher** – the algorithm used to transform data.
* **Key** – a value used by the cipher.
* **Encryption** – converting plaintext into ciphertext.
* **Decryption** – converting ciphertext back into plaintext.

The task also introduced classical ciphers such as **Caesar Cipher, Vigenère Cipher, and Substitution Cipher**.

Although these classical ciphers are not suitable for modern secure communication, they are useful for understanding the basic ideas behind encryption and cryptanalysis.

**Main takeaway:** Cryptography protects information by transforming readable data into a form that cannot be understood without the correct process and key.

---

### **Task 21: Cryptography - Part 2**

This task introduced the difference between **symmetric and asymmetric encryption**.

**Symmetric encryption** uses a single shared key for both encryption and decryption. Common algorithms include:

* DES
* 3DES
* AES

AES is widely used today with key sizes of 128, 192, and 256 bits. One major challenge with symmetric encryption is securely sharing the secret key.

**Asymmetric encryption** uses two different keys:

* Public key
* Private key

The public key can be shared openly, while the private key must be kept secret. Asymmetric encryption is useful because a secret key does not have to be shared beforehand.

Common technologies include:

* RSA
* Diffie-Hellman
* ECC

I also learned that a **256-bit ECC key** provides security comparable to approximately a **3072-bit RSA key**, while the effective security strength of **3DES** is around **112 bits**.

**Main takeaway:** Symmetric encryption is efficient but has a key-sharing problem, while asymmetric encryption solves key distribution using public and private keys.

---

### **Task 22: Cipher Breaker Challenge**

This task was a practical challenge based on the classical cryptography concepts learned previously.

The challenge involved:

* Caesar Cipher
* Vigenère Cipher
* Substitution Cipher
* Mixed cipher challenges

For the **Caesar Cipher**, I learned that each character is shifted by a fixed value. The basic formula is:

```text
C = (P + K) mod 26
```

where `P` represents the plaintext character position and `K` represents the shift.

The **Vigenère Cipher** uses a keyword to apply different shifts to different characters. This makes it more difficult to break using simple brute force compared to Caesar.

The task helped connect the theoretical cryptography concepts with an actual challenge and showed how simple encryption schemes can be analysed and broken.

**Main takeaway:** Cryptography is not only about creating encryption; understanding how weak ciphers can be analysed is also an important cybersecurity skill.

---

### **Task 23: Principles of CyberSecurity: CIA**

This task introduced the **CIA Triad**, which is one of the fundamental concepts of cybersecurity.

CIA stands for:

* **Confidentiality**
* **Integrity**
* **Availability**

**Confidentiality** means that sensitive information should only be accessible to authorized individuals.

**Integrity** means that information should remain accurate and should not be changed without authorization.

**Availability** means that systems and information should be accessible to authorized users when required.

The task used simple real-world situations to explain these principles and showed how cybersecurity focuses on protecting all three.

**Main takeaway:** The CIA Triad provides a basic framework for understanding what cybersecurity is trying to protect.

---

### **Task 24: Principles of CyberSecurity: CIA - Explanation**

This task went deeper into the three principles of the **CIA Triad** and showed how they apply to real situations.

**Confidentiality** protects information from unauthorized access. Encryption and access controls are examples of methods used to maintain confidentiality.

**Integrity** protects information from unauthorized modification. For example, if someone changes a bank transaction or alters a record without permission, the integrity of the data has been compromised.

**Availability** ensures that systems and services remain accessible when users need them. Backup systems, redundancy, and protection against excessive traffic can help maintain availability.

I also learned how different incidents can affect different CIA principles. Data theft mainly affects confidentiality, unauthorized modification affects integrity, and service outages affect availability.

**Main takeaway:** Identifying which part of the CIA Triad is affected helps understand the type of security problem and the protection required.

---

### **Task 25: Principles of CyberSecurity: Red Teaming**

This task introduced **Offensive Security** and **Red Teaming**.

Offensive security focuses on actively testing systems by thinking and acting from an attacker's perspective. The purpose is to discover weaknesses before real attackers can exploit them.

Some of the questions an offensive security professional may ask include:

* What parts of the system are exposed?
* What resources can be accessed?
* What assumptions does the system make about users?
* What happens when unexpected actions are performed?

The task also clarified that hacking in this context means **legal and ethical penetration testing**. Security professionals must have permission before testing a system and must stay within the defined scope.

I also learned that familiarity with the **command-line interface (CLI)** is useful for offensive security activities.

**Main takeaway:** Offensive security helps organizations identify weaknesses proactively by looking at systems from an attacker's point of view.

---

### **Task 26: Red Teaming Continuation**

This task continued the introduction to **Red Teaming** and focused on the basic terminology used in offensive security.

The main concepts I learned were:

* **Red Teaming** – an authorized simulation of a real-world attack.
* **Penetration Testing** – a structured security assessment performed within an approved scope.
* **Vulnerability** – a weakness in a system or application.
* **Exploit** – a method used to take advantage of a vulnerability.
* **Scope** – the defined boundaries of what can be tested.

I also understood that **permission is essential** in ethical hacking. Security testing should only be performed on systems that have been explicitly authorized for testing.

The task introduced the idea of **web enumeration**, where security professionals look for hidden or unintended resources that may be exposed by a web application. It also introduced **Gobuster** as an example of a tool used to automate this type of enumeration.

The practical exercise helped me understand how attackers think about the **attack surface** and how security testers can identify potentially exposed areas before they are exploited by real attackers.

**Main takeaway:** I learned how Red Teaming and penetration testing are used to identify weaknesses from an attacker's perspective, while keeping the testing legal, authorized, and within the defined scope.
- - - 

### **Overall Conclusion**

Completing these 26 TryHackMe tasks gave me a strong foundation in the basic areas of **cybersecurity and networking**.

I started by learning how networks work, including **IP addresses, MAC addresses, ports, packets, frames, DNS, DHCP, and ICMP**. I then moved into Windows and Linux, where I learned basic system administration, file management, user accounts, PowerShell, and built-in security features.

The cryptography tasks helped me understand **encryption, decryption, symmetric encryption, asymmetric encryption, and classical ciphers**. The Cipher Breaker challenge gave me a practical way to apply those concepts.

The **CIA Triad** helped me understand the main goals of cybersecurity: protecting confidentiality, maintaining data integrity, and ensuring availability. Finally, the Red Teaming tasks introduced the attacker's perspective, ethical hacking, vulnerabilities, exploits, scope, and basic web enumeration.

**The main takeaway from the entire set of tasks was that cybersecurity starts with understanding how systems actually work.** Once I understand networks, operating systems, protocols, and applications, it becomes much easier to identify where security weaknesses can exist and how they can be protected.
