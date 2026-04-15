# Scanning Networks
The objective of this lab is to conduct network scanning, port scanning, analyzing the network vulnerabilities, etc.

Network scans are needed to:

- Check live systems and open ports
- Identify services running in live systems
- Perform banner grabbing/OS fingerprinting
- Identify network vulnerabilities

## Lab 1: Perform Host Discovery

Host discovery is considered the primary task in the network scanning process. It is used to discover the active/live hosts in a network. It provides an accurate status of the systems in the network, which, in turn, reduces the time spent on scanning every port on every system in a sea of IP addresses in order to identify whether the target host is up.

The following are examples of host discovery techniques:

- ARP ping scan
- UDP ping scan
- ICMP ping scan (ICMP ECHO ping, ICMP timestamp, ping ICMP, and address mask ping)
- TCP ping scan (TCP SYN ping and TCP ACK ping)
- IP protocol ping scan

### Task 1: Perform Host Discovery using Nmap

**Command:** nmp -sn -PR 10.10.1.22

> -sn: disables port scan and -PR performs ARP ping scan

**Command:** nmap -sn -PU 10.10.1.22

> -PU: performs the UDP ping scan.

The UDP ping scan sends UDP packets to the target host, a UDP response means that the host is active. If the target host is offline or unreachable, various error messages such as “host/network unreachable” or “TTL exceeded” could be returned.

**Command:** nmap -sn -PE 10.10.1.22

> -PE: performs the ICMP echo ping scan

The ICMP ECHO ping scan involves sending ICMP ECHO requests to a host. If the target host is alive, it will return an ICMP ECHO reply.  This scan is useful for locating active devices or determining if the ICMP is passing through a firewall.

**Command:** nmap -sn -PP 10.10.1.22

> -PP: performs the ICMP timestamp ping scan.

ICMP timestamp ping is an optional and additional type of ICMP ping whereby the attackers query a timestamp message to acquire the information related to the current time from the target host machine.

**Command:** nmap -sn -PM \[target IP address\]

> **ICMP Address Mask Ping Scan**: This technique is an alternative for the traditional ICMP ECHO ping scan, which are used to determine whether the target host is live specifically when administrators block the ICMP ECHO pings.

**Command:** nmap -sn -PS \[target IP address\]

**TCP SYN Ping Scan:** This technique sends empty TCP SYN packets to the target host, ACK response means that the host is active.

**Command:** nmap -sn -PA \[target IP address\]

**TCP ACK Ping Scan**: This technique sends empty TCP ACK packets to the target host; an RST response means that the host is active.

**Command:** nmap -sn -PO \[target IP address\]

**IP Protocol Ping Scan**: This technique sends different probe packets of different IP protocols to the target host, any response from any probe indicates that a host is active.

### Task 2: Perform Host Discovery using Angry IP Scanner

**Other Tools:**

**SolarWinds Engineer's Toolset:** [https://www.solarwinds.com](https://www.solarwinds.com)

**NetScanTools Pro:** [https://www.netscantools.com](https://www.netscantools.com)

**Colasoft Ping Tool:** [https://www.colasoft.com](https://www.colasoft.com)

**Visual Ping Tester:** [http://www.pingtester.net](http://www.pingtester.net)

**OpUtils:** [https://www.manageengine.com](https://www.manageengine.com)

## Lab 2: Perform Port and Service Discovery

Port scanning techniques are categorized according to the type of protocol used for communication within the network.

- TCP Scanning
    - Open TCP scanning methods (TCP connect/full open scan)
    - Stealth TCP scanning methods (Half-open Scan, Inverse TCP Flag Scan, ACK flag probe scan, third party and spoofed TCP scanning methods)
- UDP Scanning
    - SCTP Scanning
        - SCTP INIT Scanning
        - SCTP COOKIE/ECHO Scanning
    - SSDP and List Scanning
    - IPv6 Scanning

### Task 1: Perform Port and Service Discovery using MegaPing

MegaPing is a toolkit that provides essential utilities for Information System specialists, system administrators, IT solution providers, and individuals. It is used to detect live hosts and open ports of the system in the network, and can scan your entire network and provide information such as open shared resources, open ports, services/drivers active on the computer, key registry entries, users and groups, trusted domains, printers, etc. You can also perform various network troubleshooting activities with the help of integrated network utilities such as DNS lookup name, DNS list hosts, Finger, host monitor, IP scanner, NetBIOS scanner, ping, port scanner, share scanner, traceroute, and Whois.

### Task 2: Perform Port and Service Discovery using NetScanTools Pro

### Task 3: Perform Port Scanning using sx Tool

The sx tool is a command-line network scanner that can be used to perform ARP scans, ICMP scans, TCP SYN scans, UDP scans and application scans such as SOCS5 scans, Docker scans and Elasticsearch scans.

### Task 4: Explore Various Network Scanning Techniques using Nmap

nmap -sT -v \[Target IP Address\]  
> -sT: performs the TCP connect/full open scan and -v: enables the verbose output (include all hosts and ports in the output).

nmap -sS -v \[Target IP Address\]  
> -sS: performs the stealth scan/TCP half-open scan and -v: enables the verbose output (include all hosts and ports in the output).  
> The stealth scan involves resetting the TCP connection between the client and server abruptly before completion of three-way handshake signals, and hence leaving the connection half-open. This scanning technique can be used to bypass firewall rules, logging mechanisms, and hide under network traffic.

nmap -sX -v \[Target IP Address\]
> -sX: performs the Xmas scan and -v: enables the verbose output (include all hosts and ports in the output).  
> Xmas scan sends a TCP frame to a target system with FIN, URG, and PUSH flags set. If the target has opened the port, then you will receive no response from the target system. If the target has closed the port, then you will receive a target system reply with an RST.

nmap -sM -v \[Target IP Address\]  
> -sM: performs the TCP Maimon scan and -v: enables the verbose output (include all hosts and ports in the output).  
> In the TCP Maimon scan, a FIN/ACK probe is sent to the target; if there is no response, then the port is Open|Filtered, but if the RST packet is sent as a response, then the port is closed.

nmap -sA -v \[Target IP Address\]  
> -sA: performs the ACK flag probe scan and -v: enables the verbose output (include all hosts and ports in the output).  
> The ACK flag probe scan sends an ACK probe packet with a random sequence number; no response implies that the port is filtered (stateful firewall is present), and an RST response means that the port is not filtered.

nmap -sU -v \[Target IP Address\]  
> -sU: performs the UDP scan and -v: enables the verbose output (include all hosts and ports in the output).  
> The UDP scan uses UDP protocol instead of the TCP. There is no three-way handshake for the UDP scan. It sends UDP packets to the target host; no response means that the port is open. If the port is closed, an ICMP port unreachable message is received.

nmap -sI -v \[target IP address\]  
> IDLE/IPID Header Scan: A TCP port scan method that can be used to send a spoofed source address to a computer to discover what services are available.

nmap -sY -v \[target IP address\]  
> SCTP INIT Scan: An INIT chunk is sent to the target host; an INIT+ACK chunk response implies that the port is open, and an ABORT Chunk response means that the port is closed.

nmap -sZ -v \[target IP address\]  
> SCTP COOKIE ECHO Scan: A COOKIE ECHO chunk is sent to the target host; no response implies that the port is open and ABORT Chunk response means that the port is closed.

nmap -A \[Target Subnet\]  
> \-A: enables aggressive scan. The aggressive scan option supports OS detection (-O), version scanning (-sV), script scanning (-sC), and traceroute (--traceroute). You should not use -A against target networks without permission.

### Task 5: Explore Various Network Scanning Techniques using Hping3

hping3 -A \[Target IP Address\] -p 80 -c 5  
>In this command, -A specifies setting the ACK flag, -p specifies the port to be scanned (here, 80), and -c specifies the packet count (here, 5).  
The ACK scan sends an ACK probe packet to the target host; no response means that the port is filtered. If an RST response returns, this means that the port is closed.

hping3 -8 0-100 -S \[Target IP Address\] -V  
>In this command, -8 specifies a scan mode, -p specifies the range of ports to be scanned (here, 0-100), and -V specifies the verbose mode.

hping3 -F -P -U \[Target IP Address\] -p 80 -c 5  
>In this command, -F specifies setting the FIN flag, -P specifies setting the PUSH flag, -U specifies setting the URG flag, -c specifies the packet count (here, 5), and -p specifies the port to be scanned (here, 80).  
FIN, PUSH, and URG scan the port on the target IP address. If a port is open on the target, you will receive a response. If the port is closed, Hping will return an RST response.

hping3 --scan 0-100 -S \[Target IP Address\]  
>In this command, --scan specifies the port range to scan, 0-100 specifies the range of ports to be scanned, and -S specifies setting the SYN flag.  
In the TCP stealth scan, the TCP packets are sent to the target host; if a SYN+ACK response is received, it indicates that the ports are open.

hping3 -1 \[Target IP Address\] -p 80 -c 5  
>In this command, -1 specifies ICMP ping scan, -c specifies the packet count (here, 5), and -p specifies the port to be scanned (here, 80).

Apart from the aforementioned port scanning and service discovery techniques, you can also use the following scanning techniques to perform a port and service discovery on a target network using Hping3.

**Entire subnet scan for live host:** hping3 -1 \[Target Subnet\] --rand-dest -I eth0

**UDP scan:** hping3 -2 \[Target IP Address\] -p 80 -c 5


## Lab 3: Perform OS Discovery

As a professional ethical hacker or a pen tester, the next step after discovering the open ports and services running on the target range of IP addresses is to perform OS discovery. Identifying the OS used on the target system allows you to assess the system's vulnerabilities and the exploits that might work on the system to perform additional attacks.

  
Active Banner Grabbing Specially crafted packets are sent to the remote OS, and the responses are noted, which are then compared with a database to determine the OS. Responses from different OSes vary, because of differences in the TCP/IP stack implementation.

Passive Banner Grabbing This depends on the differential implementation of the stack and the various ways an OS responds to packets. Passive banner grabbing includes banner grabbing from error messages, sniffing the network traffic, and banner grabbing from page extensions.  


Parameters such as TTL and TCP window size in the IP header of the first packet in a TCP session plays an important role in identifying the OS running on the target machine. The TTL field determines the maximum time a packet can remain in a network, and the TCP window size determines the length of the packet reported. These values differ for different OSes: you can refer to the following table to learn the TTL values and TCP window size associated with various OSes.

![Scanning Networks_2022-03-25_1.jpg](Practicals/images/Scanning Networks_2022-03-25_1.jpg)

### Task 1: Identify the Target System's OS with Time-to-Live (TTL) and TCP Window Sizes using Wireshark

### Task 2: Perform OS Discovery using Nmap Script Engine (NSE)  
Nmap, along with Nmap Script Engine (NSE), can extract considerable valuable information from the target system. In addition to Nmap commands, NSE provides scripts that reveal all sorts of useful information from the target system. Using NSE, you may obtain information such as OS, computer name, domain name, forest name, NetBIOS computer name, NetBIOS domain name, workgroup, system time of a target system, etc.

nmap -A \[Target IP Address\]  
> The scan results appear, displaying the open ports and running services along with their versions and target details such as OS, computer name, NetBIOS computer name, etc. under the Host script results section.

nmap -O \[Target IP Address\]  
> \-O: performs the OS discovery.

nmap --script smb-os-discovery.nse \[Target IP Address\]  
> \--script: specifies the customized script and smb-os-discovery.nse: attempts to determine the OS, computer name, domain, workgroup, and current time over the SMB protocol (ports 445 or 139).

### Task 3: Perform OS Discovery using Unicornscan
  
Unicornscan is a Linux-based command line-oriented network information-gathering and reconnaissance tool. It is an asynchronous TCP and UDP port scanner and banner grabber that enables you to discover open ports, services, TTL values, etc. running on the target machine. In Unicornscan, the OS of the target machine can be identified by observing the TTL values in the acquired scan result.

unicornscan \[Target IP Address\] -Iv  
> In this command, -I specifies an immediate mode and v specifies a verbose mode.  


## Lab 4: Scan beyond IDS and Firewall

Techniques to evade IDS/firewall:

*   **Packet Fragmentation**: Send fragmented probe packets to the intended target, which re-assembles it after receiving all the fragments
*   **Source Routing**: Specifies the routing path for the malformed packet to reach the intended target
*   **Source Port Manipulation**: Manipulate the actual source port with the common source port to evade IDS/firewall
*   **IP Address Decoy**: Generate or manually specify IP addresses of the decoys so that the IDS/firewall cannot determine the actual IP address
*   **IP Address Spoofing**: Change source IP addresses so that the attack appears to be coming in as someone else
*   **Creating Custom Packets**: Send custom packets to scan the intended target beyond the firewalls
*   **Randomizing Host Order**: Scan the number of hosts in the target network in a random order to scan the intended target that is lying beyond the firewall
*   **Sending Bad Checksums**: Send the packets with bad or bogus TCP/UPD checksums to the intended target
*   **Proxy Servers**: Use a chain of proxy servers to hide the actual source of a scan and evade certain IDS/firewall restrictions
*   **Anonymizers**: Use anonymizers that allow them to bypass Internet censors and evade certain IDS and firewall rules

### Task 1: Scan beyond IDS/Firewall using various Evasion Techniques

nmap -f \[Target IP Address\]  
> \-f switch is used to split the IP packet into tiny fragment packets.

Packet fragmentation refers to the splitting of a probe packet into several smaller packets (fragments) while sending it to a network. When these packets reach a host, IDSs and firewalls behind the host generally queue all of them and process them one by one. However, since this method of processing involves greater CPU consumption as well as network resources, the configuration of most of IDSs makes it skip fragmented packets during port scans.

nmap -g 80 \[Target IP Address\]  
> In this command, you can use the -g or --source-port option to perform source port manipulation.
Source port manipulation refers to manipulating actual port numbers with common port numbers to evade IDS/firewall: this is useful when the firewall is configured to allow packets from well-known ports like HTTP, DNS, FTP, etc.

nmap -mtu 8 \[Target IP Address  
> In this command, -mtu: specifies the number of Maximum Transmission Unit (MTU) (here, 8 bytes of packets).
Using MTU, smaller packets are transmitted instead of sending one complete packet at a time. This technique evades the filtering and detection mechanism enabled in the target machine.

nmap -D RND:10 \[Target IP Address\]  
> In this command, -D: performs a decoy scan and RND: generates a random and non-reserved IP addresses (here, 10).
The IP address decoy technique refers to generating or manually specifying IP addresses of the decoys to evade IDS/firewall. This technique makes it difficult for the IDS/firewall to determine which IP address was actually scanning the network and which IP addresses were decoys. By using this command, Nmap automatically generates a random number of decoys for the scan and randomly positions the real IP address between the decoy IP addresses.

nmap -sT -Pn --spoof-mac 0 \[Target IP Address\]  
> In this command --spoof-mac 0 represents randomizing the MAC address, -sT: performs the TCP connect/full open scan, -Pn is used to skip the host discovery.
MAC address spoofing technique involves spoofing a MAC address with the MAC address of a legitimate user on the network. This technique allows you to send request packets to the targeted machine/network pretending to be a legitimate host.  


### Task 2: Create Custom Packets using Colasoft Packet Builder to Scan beyond the IDS/Firewall

Colasoft Packet Builder is a tool that allows you to create custom network packets to assess network security. You can also select a TCP packet from the provided templates and change the parameters in the decoder editor, hexadecimal editor, or ASCII editor to create a packet. In addition to building packets, the Colasoft Packet Builder supports saving packets to packet files and sending packets to the network.

### Task 3: Create Custom UDP and TCP Packets using Hping3 to Scan beyond the IDS/Firewall

  
Hping3 is a scriptable program that uses the TCL language

hping3 \[Target IP Address\] --udp --rand-source --data 500  
> Here, --udp specifies sending the UDP packets to the target host, --rand-source enables the random source mode and --data specifies the packet body size.

hping3 -S \[Target IP Address\] -p 80 -c 5  
> Here, -S specifies the TCP SYN request on the target machine, -p specifies assigning the port to send the traffic, and -c is the count of the packets sent to the target machine.

hping3 \[Target IP Address\] --flood  
> \--flood: performs the TCP flooding.

## Lab 5: Perform Network Scanning using Various Scanning Tools

### Task 1: Scan a Target Network using Metasploit