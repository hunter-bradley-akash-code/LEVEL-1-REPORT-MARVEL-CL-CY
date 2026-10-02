# MARVEL Level-1 – Technical Concepts

## 1. PEM File, PPK File and PuTTY

PEM stands for Privacy-Enhanced Mail. It is a file format used to store cryptographic information such as private keys, public keys and certificates. In AWS, a PEM file is commonly used as a private key when connecting to an EC2 instance through SSH. It helps verify the identity of the user trying to access the server.

PPK stands for PuTTY Private Key. It is a private-key file format traditionally used by PuTTY for SSH authentication. If we have a PEM file and want to connect to a server using PuTTY, we can convert the PEM file into PPK format using PuTTYgen.

PuTTY is a software application used to connect to remote computers and servers over a network. It is commonly used on Windows to connect to Linux servers, including AWS EC2 instances, through SSH. SSH provides an encrypted connection, allowing users to securely access and manage remote servers.

PuTTYgen is a tool provided with PuTTY that can generate SSH key pairs and convert supported private-key formats. When connecting to an AWS EC2 instance, we can use PuTTYgen to convert the PEM file into a PPK file, configure the server's public IP address in PuTTY, select the PPK file for authentication and establish the SSH connection. The EC2 security group must allow SSH traffic, usually through port 22, from the connecting computer.

In simple terms, PEM and PPK are private-key file formats, while PuTTY is the application used to connect to a remote server. The private key is used to prove the user's identity and should always be kept secure.

## 2. Types of Amazon S3 Buckets

Amazon S3 stands for Simple Storage Service. It is an object storage service provided by AWS that allows users to store and retrieve data such as images, videos, documents, backups and application files.

An S3 bucket is a container used to store objects in Amazon S3. Each object contains data and is identified by a unique key within the bucket. Buckets help organize and manage stored data and control access to it.

Amazon S3 provides different bucket types for different requirements. General purpose buckets are the standard bucket type and are used for common storage needs such as backups, application files, static websites and data lakes. Directory buckets are designed for workloads that require very low latency and high request rates. They are associated with the S3 Express One Zone storage class and use a hierarchical directory structure. Table buckets are designed to store tabular data using Apache Iceberg-compatible tables and are useful for analytics workloads.

S3 also provides different storage classes based on how frequently data is accessed and how it needs to be stored. S3 Standard is used for frequently accessed data. S3 Intelligent-Tiering is useful when access patterns change or are difficult to predict. S3 Standard-IA is intended for data that is accessed less frequently but still requires quick access. S3 One Zone-IA stores infrequently accessed data in a single Availability Zone, while S3 Glacier storage classes are used for archival data.

A bucket type defines the structure and capabilities of the bucket, whereas a storage class defines how individual objects are stored. S3 is commonly used for application storage, backups, archives, static website content and sharing data between AWS services. Buckets are private by default in common configurations, and access can be managed using IAM policies, bucket policies and other access-control settings.

## 3. DHCP

DHCP stands for Dynamic Host Configuration Protocol. It is a network protocol that automatically assigns IP addresses and other network configuration details to devices connected to a network.

Whenever a device connects to a network, it needs an IP address to communicate with other devices. Instead of configuring an IP address manually on every device, DHCP allows a DHCP server, often running on a router, to assign the required settings automatically. These settings may include the IP address, subnet mask, default gateway, DNS server address and lease duration.

DHCP commonly follows a four-step process known as DORA: Discover, Offer, Request and Acknowledge.

During the Discover step, a device sends a DHCP Discover message to find available DHCP servers. In the Offer step, a DHCP server responds with an available IP address and other network settings. During the Request step, the device requests to use the offered IP address. Finally, in the Acknowledge step, the DHCP server confirms the assignment, and the device can start using the IP address.

The IP address is generally assigned for a specific period called a DHCP lease. Before the lease expires, the device can request to renew it. This allows IP addresses to be reused when devices disconnect or no longer need them.

DHCP reduces manual configuration, makes network management easier and helps prevent common configuration mistakes and IP address conflicts. For example, when a phone connects to Wi-Fi, the router's DHCP server can automatically assign it an IP address and the other settings required to communicate over the network.

## 4. ICMP

ICMP stands for Internet Control Message Protocol. It is a network protocol used by network devices to send error reports and operational information related to IP communication. It helps identify certain network problems and is commonly used for troubleshooting.

One of the most familiar tools that uses ICMP is ping. The ping command sends ICMP Echo Request messages to a destination and waits for ICMP Echo Reply messages. If replies are received, ping displays information such as the response time and packet loss.

For example, the command `ping 8.8.8.8` sends Echo Request messages to the specified IP address. If the destination is configured to respond and the messages are allowed through the network, it sends Echo Reply messages back.

ICMP also includes messages such as Destination Unreachable, which indicates that a destination or network cannot be reached in a particular way, and Time Exceeded, which indicates that a packet's TTL has expired or that a fragment reassembly timer has expired.

ICMP is different from TCP and UDP. TCP and UDP are transport-layer protocols used to carry application data, while ICMP is used for network control, error reporting and diagnostics. ICMP does not use TCP or UDP port numbers.

ICMP is useful for diagnosing connectivity issues and understanding certain network delivery problems. However, a failed ping does not always mean that a server is down. A firewall or network configuration may block ICMP traffic even when the server and its applications are running.

## 5. Public Key and Private Key

Public-key cryptography uses a pair of mathematically related keys called a public key and a private key. These keys are used for tasks such as encryption, authentication and digital signatures.

A public key can be shared with other people or systems. Depending on the cryptographic method, it can be used to encrypt information or verify a digital signature. A private key must be kept secret by its owner. It can be used to decrypt information encrypted for the corresponding public key or to create digital signatures.

For example, if someone wants to send encrypted information to a recipient, they can use the recipient's public key to encrypt it. The recipient can then use the corresponding private key to decrypt it. For digital signatures, the sender uses their private key to sign information, and others can use the corresponding public key to verify the signature.

Public and private keys are also used in SSH authentication. When connecting to a server using SSH key-based authentication, the server stores the user's public key. The SSH client proves that the user has access to the matching private key through a cryptographic authentication process. If authentication succeeds and the user is authorized, the connection is allowed. The private key remains with the user and should not be shared.

WhatsApp uses end-to-end encryption to protect personal messages and calls. Its encryption system uses public-key and private-key cryptography together with symmetric encryption. Cryptographic keys on users' devices help establish secure communication. Message content is encrypted on the sender's device and decrypted on the recipient's device. WhatsApp's end-to-end encryption is based on the Signal Protocol.

End-to-end encryption is designed so that message content can be read only by the communicating devices, rather than by the service relaying the messages. Some account information and metadata may be handled separately from the encrypted message content.

Public and private keys are important because they support secure communication, authentication, encryption and digital signatures. The public key can be shared, but the private key must remain secret to prevent unauthorized access or impersonation.
