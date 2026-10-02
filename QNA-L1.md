# MARVEL Level-1 Q and A

## 1. PEM File PPK File and PuTTY

PEM stands for Privacy Enhanced Mail. It is a file format used to store keys and certificates. In AWS a PEM file is commonly used as a private key to connect to an EC2 instance using SSH. It helps verify the identity of the user who is trying to access the server.

PPK stands for PuTTY Private Key. It is a file format used by PuTTY for SSH authentication. If we have a PEM file and want to connect to a server using PuTTY we can convert it into a PPK file using PuTTYgen.

PuTTY is a software used to connect to remote computers and servers. It is commonly used on Windows to connect to Linux servers such as AWS EC2 instances. It uses SSH to provide a secure connection between the local computer and the remote server.

PuTTYgen is a tool that comes with PuTTY. It is used to generate SSH keys and convert key files from one format to another. When connecting to an AWS EC2 instance we can convert the PEM file into a PPK file and use it in PuTTY. We also need the public IP address of the EC2 instance and the correct username. The security group must allow SSH traffic through port 22.

PEM and PPK are file formats used for private keys while PuTTY is the software used to connect to a remote server. The private key should always be kept safe and should not be shared with others.

## 2. Types of Amazon S3 Buckets

Amazon S3 stands for Simple Storage Service. It is a storage service provided by AWS that is used to store and retrieve files such as images videos documents and backups.

An S3 bucket is a container where we store data in Amazon S3. The files stored inside a bucket are called objects. Each object has a unique key that helps identify it within the bucket.

Amazon S3 provides different types of buckets based on their usage. General purpose buckets are used for common storage needs such as application files backups static websites and data lakes.

Directory buckets are designed for applications that need very fast data access and high request rates. They are associated with the S3 Express One Zone storage class and use a hierarchical directory structure.

Table buckets are used to store tabular data and are designed for analytics workloads. They support Apache Iceberg compatible tables.

Amazon S3 also provides different storage classes depending on how frequently the data is accessed. S3 Standard is used for frequently accessed data. S3 Intelligent Tiering is useful when the access pattern is not predictable. S3 Standard IA is used for data that is accessed less frequently but still needs quick access. S3 One Zone IA stores data in a single Availability Zone. S3 Glacier storage classes are mainly used for long term data storage and archiving.

A bucket type defines the features and structure of the bucket while a storage class defines how the data is stored. S3 is commonly used for storing application data backups and files. Access to buckets and objects can be managed using IAM policies and bucket policies.

## 3. DHCP

DHCP stands for Dynamic Host Configuration Protocol. It is a network protocol that automatically assigns IP addresses and other network settings to devices connected to a network.

When a device connects to a network it needs an IP address to communicate with other devices. Instead of assigning an IP address manually DHCP provides one automatically through a DHCP server. This server is often available on a router.

DHCP can provide an IP address subnet mask default gateway DNS server address and lease duration to a device.

DHCP works through a process called DORA. It has four steps which are Discover Offer Request and Acknowledge.

In the Discover step the device sends a message to find a DHCP server. In the Offer step the server offers an available IP address. In the Request step the device requests to use that IP address. Finally in the Acknowledge step the server confirms the assignment and the device can start using the address.

The IP address assigned by DHCP is usually given for a limited period called a lease. Before the lease expires the device can request to renew it.

DHCP makes network management easier because we do not have to manually configure every device. It also helps reduce IP address conflicts and configuration errors.

For example when we connect our phone to WiFi the router can automatically assign an IP address using DHCP. This allows the phone to communicate with other devices and access the internet.

## 4. ICMP

ICMP stands for Internet Control Message Protocol. It is a network protocol used to send error messages and information related to IP communication. It is mainly used for network troubleshooting and diagnostics.

One common tool that uses ICMP is ping. The ping command checks whether a destination responds over a network. It sends an ICMP Echo Request message and waits for an ICMP Echo Reply.

For example we can use the command `ping 8.8.8.8` to check whether that IP address responds. If replies are received ping displays information such as response time and packet loss.

ICMP has different types of messages. Destination Unreachable is used when a destination or network cannot be reached in a particular way. Time Exceeded is sent when a packet's TTL expires or when a fragment reassembly timer expires. Echo Request and Echo Reply are used by ping to check connectivity.

ICMP is different from TCP and UDP. TCP and UDP are used to transfer application data while ICMP is mainly used for error reporting and network diagnostics. ICMP does not use TCP or UDP port numbers.

ICMP helps us find network connectivity problems. However if ping does not receive a reply it does not always mean that the server is down. Sometimes a firewall or network setting may block ICMP traffic even when the server is working properly.

## 5. Public Key and Private Key

Public key and private key are two parts of a cryptographic key pair. They are used to secure communication and verify identity.

A public key can be shared with other people or systems. It can be used to encrypt information or verify a digital signature depending on the cryptographic method.

A private key must be kept secret by its owner. It can be used to decrypt information or create digital signatures. The public and private keys are mathematically related but the private key cannot practically be calculated from the public key when secure algorithms are used.

For example if someone wants to send an encrypted message to another person they can use the receiver's public key to encrypt it. The receiver can then use their private key to decrypt the message.

These keys are also used in SSH. When a user connects to a server using SSH key authentication the server has the user's public key. The user proves that they have the matching private key. If the authentication is successful and the user is allowed to access the server the connection is established.

WhatsApp also uses public key and private key cryptography as part of its end to end encryption system. It uses these keys along with symmetric encryption to protect messages and calls.

When a message is sent it is encrypted on the sender's device and decrypted on the receiver's device. WhatsApp uses the Signal Protocol for end to end encryption. The purpose of this system is to protect message content so that only the communicating devices can read it.

Some account information and metadata may be handled separately from the encrypted message content.

Public and private keys are important for secure communication authentication encryption and digital signatures. The public key can be shared but the private key must always remain secret.
