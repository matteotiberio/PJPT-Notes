# IP Addresses

## IPv4 and IPv6

IPv4 (Internet Protocol version 4) and IPv6 (Internet Protocol version 6) are two versions of the Internet Protocol, the fundamental protocol that enables communication on the internet. They are used to identify and locate devices on a network.

## IPv4

IPv4 addresses are 32-bit numeric addresses represented in dotted decimal format, such as "192.168.0.1".  
Each section, or octet, of the address consists of 8 bits and can range from 0 to 255. This allows for approximately 4.3 billion unique addresses.  
However, due to the rapid growth of the internet, the number of available IPv4 addresses has become limited, leading to the development of IPv6.

### IPv4 Address Classes

IPv4 addresses are divided into classes, which define the size of the network and host portions, and help identify the intended use of the addresses. The main classes are:

| Class | Address Range              | Main Use               | Network/Host Bits          |
|-------|----------------------------|------------------------|---------------------------|
| A     | 0.0.0.0 – 127.255.255.255  | Very large networks    | 8 bits network / 24 bits host |
| B     | 128.0.0.0 – 191.255.255.255| Medium-sized networks  | 16 bits network / 16 bits host|
| C     | 192.0.0.0 – 223.255.255.255| Small networks         | 24 bits network / 8 bits host |
| D     | 224.0.0.0 – 239.255.255.255| Multicast              | Not applicable            |
| E     | 240.0.0.0 – 255.255.255.255| Future or experimental use | Not applicable         |

- **Class A:** Intended for very large networks (e.g., large organizations). The first octet identifies the network, the remaining three are for hosts.  
- **Class B:** Used for medium-sized networks. The first two octets identify the network, the last two are for hosts.  
- **Class C:** For smaller networks, such as small businesses or home networks.  
- **Class D:** Reserved for multicast addresses, used for transmissions to groups of recipients.  
- **Class E:** Reserved for future or experimental use, not used on the public internet.

---

## IPv6

IPv6 addresses are 128-bit addresses represented in hexadecimal format, such as `2001:0db8:85a3:0000:0000:8a2e:0370:7334`.  
The longer length of IPv6 addresses allows for a much larger number of unique addresses, approximately 3.4×10^38.  
IPv6 addresses are divided into eight groups of four hexadecimal digits, separated by colons (`:`).  
Leading zeros in a group can be omitted, and consecutive groups of zeros can be abbreviated with a double colon (`::`) to simplify notation.

---

## Transition from IPv4 to IPv6

The transition from IPv4 to IPv6 is necessary due to the exhaustion of available IPv4 addresses.  
IPv6 offers a solution to the address scarcity problem, introducing improvements in security, auto-configuration, and other features.  
However, IPv4 and IPv6 are not directly compatible with each other, so transition mechanisms and technologies have been developed to enable communication between the two protocols.

---

**In summary:**

- IPv4 and IPv6 are versions of the Internet Protocol that provide unique addresses to devices on a network.  
- IPv4 addresses are 32-bit, while IPv6 addresses are 128-bit.  
- IPv6 offers a much larger address space and additional features compared to IPv4.

---

# MAC Addresses

The first 3 pairs of a MAC address identify the manufacturer.

We can use tools like MAC Address and OUI Lookup to determine specific vendors:

![MAC Address Example](/Images/MAC.png)

In this case, `52:54:00` corresponds to the RealtekU vendor identifier.

---

# TCP, UDP, and Three-Way Handshake

- **TCP** = Transmission Control Protocol - Connection-Oriented Protocol - High reliability (http, https, ssh...)  
- **UDP** = User Datagram Protocol - Connectionless Protocol - (dns, voip...)

**SYN** - SYNCHRONIZE  
**SYN ACK** - SYNCHRONIZE ACKNOWLEDGMENT  
**ACK** - ACKNOWLEDGMENT

The client sends a SYN packet to a specific port or service; the port responds with SYN ACK to indicate availability, then the client responds with an ACK:

![Three-Way Handshake](/Images/TWH.png)

- **Packet 280:** IP `192.169.57.139` sends a SYN packet to IP `74.125.21.155` from port `52610` to port `443`  
- **Packet 284:** IP `74.125.21.155` responds with SYN ACK from port `443` to `52610`  
- **Packet 285:** Connection established

---

# Common Ports and Protocols

Here are some commonly used ports and associated protocols in networking:

- **FTP** (File Transfer Protocol): Port 21 (TCP)  
- **SSH** (Secure Shell): Port 22 (TCP)  
- **Telnet:** Port 23 (TCP)  
- **SMTP** (Simple Mail Transfer Protocol): Port 25 (TCP)  
- **DNS** (Domain Name System): Port 53 (TCP and UDP)  
- **HTTP** (Hypertext Transfer Protocol): Port 80 (TCP)  
- **HTTPS** (Hypertext Transfer Protocol Secure): Port 443 (TCP)  
- **DHCP** (Dynamic Host Configuration Protocol): Ports 67 (UDP) and 68 (UDP)  
- **POP3** (Post Office Protocol version 3): Port 110 (TCP)  
- **IMAP** (Internet Message Access Protocol): Port 143 (TCP)  
- **SNMP** (Simple Network Management Protocol): Port 161 (UDP)  
- **RDP** (Remote Desktop Protocol): Port 3389 (TCP)  
- **NTP** (Network Time Protocol): Port 123 (UDP)  
- **SMB** (Server Message Block): Port 445 (TCP)  
- **FTPS** (FTP over SSL/TLS): Port 990 (TCP)  
- **TFTP** (Trivial File Transfer Protocol): Port 69 (UDP)  
- **LDAP** (Lightweight Directory Access Protocol): Ports 389 (TCP and UDP)  
- **MySQL:** Port 3306 (TCP)

*Note:* Some protocols use both TCP and UDP depending on specific functionality. Also, these port assignments are not exhaustive—many applications and services may use different or custom ports.

---

# The OSI Model

The **OSI Model** (Open Systems Interconnection) is a conceptual framework that standardizes the functions of a communication system into seven distinct layers. Each layer has specific responsibilities and interacts with the layers above and below it. The OSI model provides a structured approach to understanding and designing network protocols and communication systems. Here is a brief overview of each layer:

- **Physical Layer:**  
  Responsible for transmitting and receiving raw, unstructured bits over a physical medium. Defines the electrical, mechanical, and functional characteristics of the physical interface between devices.

- **Data Link Layer:**  
  Manages reliable transmission of data frames between nodes directly connected on a physical link. Provides error detection and correction, flow control, and manages access to the physical medium. Examples include Ethernet, Wi-Fi, and PPP (Point-to-Point Protocol).

- **Network Layer:**  
  Enables routing of data packets across different networks. Handles logical addressing and determines the best path for data delivery based on network conditions and routing protocols. IP (Internet Protocol) is a key protocol at this layer.

- **Transport Layer:**  
  Ensures reliable and ordered delivery of data between end systems. Segments data into smaller units, manages end-to-end communication, and provides error recovery, flow control, and congestion control. TCP (Transmission Control Protocol) and UDP (User Datagram Protocol) operate at this layer.

- **Session Layer:**  
  Establishes, manages, and terminates communication sessions between applications. Provides synchronization and dialog control mechanisms to enable smooth communication between devices. Also handles checkpointing and session recovery.

- **Presentation Layer:**  
  Responsible for data representation, encryption, compression, and formatting. Ensures that data sent from the application layer of one system is understandable by the application layer of another system. Deals with syntax and semantics of the data.

- **Application Layer:**  
  The closest layer to the end user, providing services directly to user applications. Includes protocols for various application-level services like file transfer, email, web browsing, and remote access. Examples include HTTP, SMTP, FTP, and DNS.

---

There is a mnemonic to remember the OSI layers:

- *Please* : Physical (Data, Cables, Cat6...)  
- *Do* : Data (Switching, MAC Address)  
- *Not* : Network (IP Addresses, Routing...)  
- *Throw* : Transport (TCP/UDP)  
- *Sausage* : Session (Session Management)  
- *Pizza* : Presentation (WMV, JPEG, MOV...)  
- *Away* : Application (HTTP, SMTP...)

---

*Routing* = directing data within a network or between different networks, i.e., deciding the best path a data packet must follow to get from source to destination:  
When you send a message or file over the
