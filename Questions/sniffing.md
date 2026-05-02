### In which of the following OSI layers do sniffers operate and perform an initial compromise?


- **Data link layer**
- Physical layer
- Network layer
- Transport layer

Explanation:

>The data link layer is the second layer of the OSI model. In this layer, data packets are encoded and decoded into bits. Sniffers operate at the data link layer and can capture packets from this layer. Networking layers in the OSI model are designed to work independently of each other; thus, if a sniffer sniffs data in the data link layer, the upper OSI layers will not be aware of the sniffing.

### Which of the following protocols is used in the ARPA–Internet community to distribute, inquire into, retrieve, and post news articles through reliable stream-based transmission?


- IMAP
- FTP
- **NNTP**
- POP

Explanation:

>**NNTP**: Network News Transfer Protocol (NNTP) distributes, inquires into, retrieves, and posts news articles using a reliable stream-based transmission of news among the ARPA-Internet community. However, this protocol fails to encrypt the data, which allows attackers to sniff sensitive information

>**IMAP**: Internet Message Access Protocol (IMAP) allows a client to access and manipulate electronic mail messages on a server. This protocol offers inadequate security, which allows attackers to obtain data and user credentials in cleartext

>**POP**: Post Office Protocol (POP) allows a user’s workstation to access mail from a mailbox server. A user can send mail from the workstation to the mailbox server via SMTP. 

>**FTP**: File Transfer Protocol (FTP) enables clients to share files between computers in a network. 


### Which of the following tools helps an attacker perform an ARP poisoning attack?


- Enyx 
- DNSRecon
- Svmap 
- **BetterCAP**

Explanation:

>**BetterCAP**: bettercap is an ARP poisoning tool and also it is the Swiss Army knife for WiFi, Bluetooth Low Energy, wireless HID hijacking and Ethernet networks reconnaissance and MITM attacks.

>**DNSRecon**: DNSRecon is a zone enumeration tool that assists users in enumerating DNS records such as A, AAAA, and CNAME. It also performs NSEC zone enumeration to obtain DNS record files of a target domain. 

>**Svmap**: Svmap is an open-source scanner that identifies SIP devices and PBX servers on a target network. It can be helpful for system administrators when used as a network inventory tool. 

>**Enyx**: Enyx is an enumeration tool that fetches the IPv6 address of a machine through SNMP.

### Which of the following techniques is used by an attacker to connect a rogue switch to the network by tricking a legitimate switch and thereby creating a trunk link between them?


- IRDP spoofing
- Switch port stealing
- **Switch spoofing**
- Double tagging

Explanation:

>**Switch Spoofing**: Attackers connect a rogue switch onto the network by tricking a legitimate switch and thereby creating a trunk link between them

>**Double Tagging**: Attackers add and modify tags in the Ethernet frame, thereby allowing the flow of traffic through any VLAN in the network

>**IRDP Spoofing**: ICMP Router Discovery Protocol (IRDP) is a routing protocol that allows a host to discover the IP addresses of active routers on their subnet by listening to router advertisement and soliciting messages on their network

>**Switch Port Stealing**: The switch port stealing sniffing technique uses MAC flooding to sniff the packets. The attacker floods the switch with forged gratuitous ARP packets with the target MAC address as the source and his/her own MAC address as the destination. 

### Which of the following techniques enables devices to detect the existence of unidirectional links and disable the affected interfaces in the network, in addition to causing STP topology loops?


- Root guard
- BPDU guard
- **UDLD**
- Loop guard

Explanation:
>**BPDU Guard**: BPDU guard must be enabled on the ports that should never receive a BPDU from their connected devices. This is used to avoid the transmission of BPDUs on PortFast-enabled ports. This feature helps in preventing potential bridging loops in the network.

>**Root Guard**: Root guard protects the root bridge and ensures that it remains as the root in the STP topology. It forces the interfaces to become the designated ports (forwarding ports) to prevent the nearby switches from becoming root switches.

>**UDLD (Unidirectional Link Detection)**: UDLD enables devices to detect the existence of unidirectional links and further disable the affected interfaces in the network. These unidirectional links in the network can cause STP topology loops.

>**Loop Guard**: Loop guard improves the stability of the network by preventing it against the bridging loops. It is generally used to protect against a malfunctioned switch.

### Which of the following DNS poisoning techniques uses ARP poisoning against switches to manipulate routing table?


- **Intranet DNS spoofing**
- DNS cache poisoning
- Proxy server DNS poisoning
- Internet DNS spoofing

Explanation:
> DNS poisoning techniques to sniff the DNS traffic of a target network. Using this technique, an attacker can obtain the ID of the DNS request by sniffing and can send a malicious reply to the sender before the actual DNS server. 

>DNS poisoning is possible using the following techniques:
>- **Intranet DNS spoofing**: An attacker can perform an intranet DNS spoofing attack on a switched LAN with the help of the ARP poisoning technique. To perform this attack, the attacker must be connected to the LAN and be able to sniff the traffic or packets. An attacker who succeeds in sniffing the ID of the DNS request from the intranet can send a malicious reply to the sender before the actual DNS server.
>- **Internet DNS spoofing**: Attackers perform Internet DNS spoofing with the help of Trojans when the victim’s system connects to the Internet. It is an MITM attack in which the attacker changes the primary DNS entries of the victim’s computer.
>- **Proxy server DNS poisoning**: In the proxy server DNS poisoning technique, the attacker sets up a proxy server on the attacker’s system. The attacker also configures a fraudulent DNS and makes its IP address a primary DNS entry in the proxy server.
>- **DNS cache poisoning**: Attackers target this DNS cache and make changes or add entries to the DNS cache. If the DNS resolver cannot validate that the DNS responses have come from an authoritative source, it will cache the incorrect entries locally and serve them to users who make the same request.

### What is the length of ID number of an organization in a MAC address?


- 48 bits
- 26 bits
- **24 bits**
- 12 bits

Explanation:

>A MAC address is 48 bits, which splits into two sections, each containing 24 bits. The first section contains the ID number of the organization that manufactured the adapter and is called the organizationally unique identifier. The next section contains the serial number assigned to the NIC adapter and is called the network interface controller (NIC) specific.

### Which of the following command is used to set the maximum number of secure MAC addresses for the interface on a Cisco switch?


- switchport port-security violation restrict
- snmp-server enable traps port-security trap-rate 5
- **switchport port-security maximum 1 vlan access**
- switchport port-security aging time 2

Explanation:
>Configuring Port Security on Cisco switch: You can use the following Cisco port security feature to defend against MAC attacks:
>- **switchport port-security**: Enables port security on the interface.
>- **switchport port-security maximum 1 vlan access**: Sets the maximum number of secure MAC addresses for the interface. The range is 1 to 3072. The default is 1.
>- **switchport port-security violation restrict**: Sets the violation mode, the action to be taken when a security violation {restrict | shutdown} is detected.
>- **switchport port-security aging time 2**: Sets the aging time for the secure port.
>- **switchport port-security aging type inactivity**: The type keyword sets the aging type as absolute or inactive.
>- **snmp-server enable traps port-security trap-rate 5**: Controls the rate at which SNMP traps are generated.


### Which of the following is a defense technique for MAC spoofing used in switches that restricts the IP traffic on untrusted Layer 2 ports by filtering traffic based on the DHCP snooping binding database?


- **IP Source Guard**
- DHCP snooping binding table
- Dynamic ARP inspection
- Authentication, authorization, and accounting (AAA)

Explanation:

>Following some of the techniques to defend against MAC address spoofing attacks:
>- **IP Source Guard**: IP Source Guard is a security feature in switches that restricts the IP traffic on untrusted Layer 2 ports by filtering traffic based on the DHCP snooping binding database. It prevents spoofing attacks when the attacker tries to spoof or use the IP address of another host.
>- **DHCP Snooping Binding Table**: The DHCP snooping process filters untrusted DHCP messages and helps to build and bind a DHCP binding table. This table contains the MAC address, IP address, lease time, binding type, VLAN number, and interface information to correspond with untrusted interfaces of a switch. It acts as a firewall between untrusted hosts and DHCP servers. It also helps in differentiating between trusted and untrusted interfaces.
>- **Dynamic ARP Inspection**: The system checks the IP to MAC address binding for each ARP packet in a network. While performing a Dynamic ARP inspection, the system will automatically drop invalid IP to MAC address bindings.
>- **AAA (Authentication, Authorization and Accounting)**: Use of AAA (Authentication, Authorization and Accounting) server mechanism in order to filter MAC addresses subsequently.


### During the penetration testing, Marin identified a web application that could be exploited to gain the root shell on the remote machine. The only problem was that in order to do that he would have to know at least one username and password usable in the application. Unfortunately, guessing usernames and brute-forcing passwords did not work. Marin does not want to give up his attempts. Since this web application, was being used by almost all users in the company and was using http protocol, so he decided to use Cain & Abel tool in order to identify at least one username and password. After a few minutes, the first username and password popped-up and he successfully exploited the web application and the physical machine. What type of attack did he use in order to find the username and password to access the web application?


- TCP protocol hijacking
- UDP protocol hijacking
- DNS spoofing
- **ARP spoofing**

Explanation:

>**ARP spoofing** is the correct answer, and since there are no configuration or management options on switches it means that there is no ARP spoofing protection.

>**DNS spoofing** is more complex and it is never the first option.

>**TCP and UDP protocol hijacking** does not make any sense here – after ARP spoofing all the traffic will be hijacked.

### Martin, a security professional, was tasked with enhancing the security of the switches connected to their organizational network. For this purpose, he applied MAC limiting feature on the switches. Now, Martin executed a command to verify if the MAC limiting process is perfectly implemented on each switch. Identify the command executed by Martin to verify MAC limiting process on a specific switch.


- switchport port-security violation restrict 
- ip dhcp snooping vlan number [number] | vlan {vlan range}]
- **show ethernet-switching table**
- switchport port-security aging time 2

Explanation:

>**switchport port-security aging time 2**: The switchport port-security aging time command configures the secure MAC address aging time on the port. The switchport port-security aging time 2 command sets the aging time as 2 minutes.

>**switchport port-security violation restrict**: The switchport port-security violation command sets the violation mode and the necessary action in case of detection of a security violation.

>**ip dhcp snooping vlan number [number] | vlan {vlan range}]**: Enables or disables DHCP snooping on one or more VLANs.

>**show ethernet-switching table**: Command to verify the MAC limiting process on the specific switch.


### Ben, a professional hacker, exploited obsolete DNS software on a target organization’s server to inject harmful DNS records into the server’s DNS cache and divert all traffic to his servers. With this technique, he attempted to mislead client browsers to fake websites infected with malicious files, instead of the legitimate website. Which of the following types of attacks did Ben perform in the above scenario?


- **SAD DNS attack**
- DNS amplification attack
- Chi-square attack
- Dictionary attack

Explanation:

>**Dictionary Attack**: A dictionary file is loaded into the cracking application that runs against user accounts .

>**Chi-square Attack**: The chi-square method is based on probability analysis to test whether a given stegoobject and the original data are the same or not.

>**SAD DNS Attack**: SAD DNS is a new variant of DNS cache poisoning, in which an attacker injects harmful DNS records into a DNS cache to divert all traffic toward their own servers. With this technique, attackers attempt to mislead client browsers to fake websites infected with malicious files, instead of the legitimate website. Attackers exploit side channels; flaws such as dnsmasq, unbound, and BIN in the latest OSes; and obsolete DNS software used to resolve DNS queries to perform SAD DNS attacks.

>**DNS amplification attack**: Recursive DNS query is a method of requesting DNS mapping. The query goes through DNS servers recursively until it fails to find the specified domain name to IP address mapping. Attackers exploit recursive DNS queries to perform a DNS amplification attack that results in DDoS attacks on the victim’s DNS server.


### Karbon, a professional hacker, targeted an organization to bypass the network traffic. For this purpose, he used a network forensic analysis tool that can monitor and extract information from network traffic as well as capture application data contained in the network traffic. Which of the following tools did Karbon utilize in the above scenario?


- AnDOSid
- **Xplico**
- Vindicate
- Akamai

Explanation:

>**AnDOSid**: AnDOSid allows the attacker to simulate a DoS attack (an HTTP POST flood attack to be precise) and DDoS attack on a web server from mobile phones.

>**Xplico**: The goal of Xplico is extract from an internet traffic capture the applications data contained. Xplico is an open source Network Forensic Analysis Tool (NFAT). Xplico is released under the GNU General Public License.

>**Akamai**: Akamai provides DDoS protection for enterprises regularly targeted by DDoS attacks. Akamai Kona Site Defender delivers multi-layered defense that effectively protects websites and web applications against the increasing threat, sophistication, and scale of DDoS attacks.

>**Vindicate**: Vindicate is an LLMNR/NBNS/mDNS spoofing detection toolkit for network administrators. Security professionals use this tool to detect name service spoofing. 
