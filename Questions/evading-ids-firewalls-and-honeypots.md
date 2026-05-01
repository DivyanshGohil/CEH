### Which of the following indicators falls in the category of general indications of system intrusion?

- Repeated probes of the available services on machines
- Repeated login attempts from remote hosts 
- **Missing logs or logs with incorrect permissions or ownership** 
- Missing files 

Explanation:

>Indications of file system intrusions:
>- If you find new, unknown files/programs on your system, then there is a possibility that the system has been intruded into. The system can be compromised to the extent that it can, in turn, compromise other network systems.
>- When an intruder gains access to a system, he or she tries to escalate privileges to gain administrative access. When the intruder obtains administrator privileges, he/she could change file permissions, for example, from read-only to write.
>- Unexplained modifications in file size are also an indication of an attack. Make sure you analyze all your system files.
>- The presence of rogue suid and sgid files on your Linux system that do not match your master list of suid and sgid files could indicate an attack.
>- You can identify unfamiliar file names in directories, including executable files with strange extensions and double extensions.
>- Missing files are also a sign of a probable intrusion/attack. 
    
>Indications of network intrusions:
>- A sudden increase in bandwidth consumption
>- Repeated probes of the available services on your machines
>- Connection requests from IPs other than those in the network range, which imply that an unauthenticated user (intruder) is attempting to connect to the network
>- Repeated login attempts from remote hosts
>- A sudden influx of log data, which could indicate attempts at DoS attacks, bandwidth consumption, and DDoS attacks
    
>Indications of system intrusions:
>- Sudden changes in logs such as short or incomplete logs
>- Unusually slow system performance
    
>Missing logs or logs with incorrect permissions or ownership 
>- Modifications to system software and configuration files
>- Unusual graphic displays or text messages
>- Gaps in system accounting
>- System crashes or reboots 
>- Unfamiliar processes


### Which of the following attributes in a packet can be used to check whether the packet originated from an unreliable zone?
- Direction
- **Interface**
- Source IP address
- TCP flag bits

Explanation:

>Traditional packet filters make this decision according to the following information in a packet:

>**Direction**: Used to check whether the packet is entering or leaving the private network.

>**Interface**: Used to check whether the packet is coming from an unreliable zone.

>**TCP flag bits**: Used to check whether the packet has SYN, ACK, or other bits set for the connection to be made.

>**Source IP address**: Used to check whether the packet is coming from a valid source. The information about the source IP address can found from the IP header of the packet.

### What is the main advantage that a network-based IDS/IPS system has over a host-based solution?


- They are placed at the boundary, allowing them to inspect all traffic
- They will not interfere with user interfaces
- They are easier to install and configure
- **They do not use host system resources**

Explanation:
> The correct option is “They do not use host system resources”.

> **Host-based intrusion detection systems** (IDSes) protect just that: the host or endpoint. This includes workstations, servers, mobile devices and the like. Host-based IDSes are not just one of the last layers of defense, but they're also one of the best security controls because they can be fine-tuned to the specific workstation, application, user role or workflows required. A network-based IDS often sits on the ingress or egress point(s) of the network to monitor what's coming and going. Given that a network-based IDS sits further out on the network, so it doesn't use any host system resources and it may not provide enough granular protection to keep everything in check -- especially for network traffic that's protected by SSL, TLS or SSH.

### A circuit-level gateway works at which of the following layers of the OSI model?
- Layer 3 – Network
- Layer 4 – Transport
- Layer 2 – Data Link
- **Layer 5 – Session**

Explanation:

>A circuit-level gateway firewall works at the session layer of the OSI model or TCP layer of TCP/IP. It forwards data between networks without verifying it, and blocks incoming packets into the host, but allows the traffic to pass through itself. Information passed to remote computers through a circuit-level gateway will appear to have originated from the gateway, as the incoming traffic carries the IP address of the proxy (circuit-level gateway).

### At which two traffic layers do most commercial IDSes generate signatures? (Select Two)

- **Network layer**
- Application layer
- Session layer
- **Transport layer**

### Which of the following commands is an example of a Snort rule using a bidirectional operator?


- log tcp any any -> 192.168.1.0/24 !6000:6010
- **log !192.168.1.0/24 any <> 192.168.1.0/24 23**
- 192.168.1.0/24 1:1024
- alert tcp !192.168.1.0/24 any -> 192.168.1.0/24 111

Explanation:
>`alert tcp !192.168.1.0/24 any -> 192.168.1.0/24 111`: Example of IP address negation rule

>`log !192.168.1.0/24 any <> 192.168.1.0/24 23`: Example of Snort rule using Bidirectional operator

>`log tcp any any -> 192.168.1.0/24 !6000:6010`: Example of port negation

>`192.168.1.0/24 1:1024`: Log UDP traffic coming from any port and destination ports ranging from 1 to 1024

### Which of the following is a host-based IDS that acts as a honeypot to attract and detect hackers and worms by simulating vulnerable system services and Trojans?


- Snort
- zIPS
- **KFSensor**
- Suricata

Explanation:
>**Snort**: Snort is an open-source network intrusion detection system capable of performing real-time traffic analysis and packet logging on IP networks. It can perform protocol analysis and content searching/matching, and it is used to detect a variety of attacks and probes, such as buffer overflows, stealth port scans, CGI attacks, SMB probes, and OS fingerprinting attempts.

>**Suricata**: Suricata is a robust network threat detection engine capable of real-time intrusion detection (IDS), inline intrusion prevention (IPS), network security monitoring (NSM), and offline pcap processing.

>**KFSensor**: KFSensor is a host-based IDS that acts as a honeypot to attract and detect hackers and worms by simulating vulnerable system services and Trojans. By acting as a decoy server, it can divert attacks from critical systems and provide a higher level of information than that achieved using firewalls and NIDS alone

>**zIPS**: Zimperium’s zIPS™ is a mobile intrusion prevention system app that provides comprehensive protection for iOS and Android devices against mobile network, device, and application cyber-attacks.

### When an alert rule is matched in a network-based IDS like snort, the IDS does which of the following:


- Stops checking rules, sends an alert, and lets the packet continue
- **Continues to evaluate the packet until all rules are checked**
- Blocks the connection with the source IP address in the packet
- Drops the packet and moves on to the next one

Explanation:

>Snort is an open-source network intrusion detection system capable of performing real-time traffic analysis and packet logging on IP networks. Snort uses the popular libpcap library (for UNIX/Linux) or Winpcap (for Windows), the same library that tcpdump uses to perform its packet sniffing. Attaching snort in promiscuous mode to the network media decodes all the packets passing through the network. It generates alerts according to the content of individual packets and rules defined in the configuration file. When an alert rule is matched in a network-based IDS like snort, the IDS continues to evaluate the packet until all rules are checked.


### Which of the following firewalls is used to secure mobile device?


- Comodo firewall 
- TinyWall
- Glasswire
- **NetPatch firewall**

Explanation:

>**NetPatch firewall** is a full-featured advanced android noroot firewall. It can be used to fully control over mobile device network. With NetPatch firewall, you can create network rules based on APP, IP address, domain name, and so on. This firewall is designed to save mobile device’s network traffic and battery consumption, and improve network security and protect privacy.

>**Comodo** firewall, **Glasswire** and **TinyWall** are not used for mobile devices.


### Which of the following firewall solution tool has the following features:
#### - Two-way firewall that monitors and blocks inbound as well as outbound traffic
#### - Allows users to browse the web privately
#### - Identity protection services help to prevent identity theft by guarding crucial data of the users. It also offers PC protection and data encryption
#### - Through Do Not Track, it stops data-collecting companies from tracking the online users
#### - Online Backup to backs up files and restores the data in the event of loss, theft, accidental deletion or disk failure


- zIPS
- **ZoneAlarm Free Firewall**
- Vangaurd Enforcer
- Wifi Inspector

Explanation:

>**ZoneAlarm Free Firewall**
>- Two-way firewall that monitors and blocks inbound as well as outbound traffic
>- Allows users to browse the web privately using the Full Stealth Mode
>- Identity protection services help to prevent identify theft by guarding crucial data of the users. It also offers PC protection and data encryption
>- Public network protection and wireless network protection are other key features of this firewall
>- Provides quick real-time security updates

>**zIPS**, **Wifi Inspector**, and **Vangaurd Enforcer** are IDS tools.


### Which of the following is an IDS evasion technique used by an attacker to confuse the IDS by forcing it to read invalid packets as well as blindly trust and accept a packet that an end system rejects?

- Fragmentation attack
- **Insertion attack**
- Obfuscation
- Invalid RST packets

Explanation:

> **Invalid RST Packets**: The TCP uses 16-bit checksums for error checking of the header and data and to ensure that communication is reliable. It adds a checksum to every transmitted segment that is checked at the receiving end. When a checksum differs from the checksum expected by the receiving host, the TCP drops the packet at the receiver's end. The TCP also uses an RST packet to end two-way communications. Attackers can use this feature to elude detection by sending RST packets with an invalid checksum.

>**Fragmentation attack**: Fragmentation can be used as an attack vector when fragmentation timeouts vary between the IDS and the host. Through the process of fragmenting and reassembling, attackers can send malicious packets over the network to exploit and attack systems.

>**Obfuscating**: It is an IDS evasion technique used by attackers to encode the attack packet payload in such a way that the destination host can only decode the packet but not the IDS. An attacker manipulates the path referenced in the signature to fool the HIDS. Using Unicode characters, an attacker can encode attack packets that the IDS would not recognize but which an IIS web server can decode

>**Insertion Attack**: Insertion is the process by which the attacker confuses the IDS by forcing it to read invalid packets (i.e., the system may not accept the packet addressed to it). An IDS blindly trusts and accepts a packet that an end system rejects. If a packet is malformed or if it does not reach its actual destination, the packet is invalid. If the IDS reads an invalid packet, it gets confused. An attacker exploits this condition and inserts data into the IDS

### In which of the following IDS evasion techniques does an attacker use an existing buffer-overflow exploit and set the “return” memory address on the overflowed stack to the entrance point of the decryption code?


- **Polymorphic shellcode**
- Invalid RST packets
- Overlapping fragments
- Urgency flag

Explanation:
>**Invalid RST Packets**: The TCP uses 16-bit checksums for error checking of the header and data and to ensure that communication is reliable. It adds a checksum to every transmitted segment that is checked at the receiving end. When a checksum differs from the checksum expected by the receiving host, the TCP drops the packet at the receiver's end. The TCP also uses an RST packet to end two-way communications. Attackers can use this feature to elude detection by sending RST packets with an invalid checksum, which causes the IDS to stop processing the stream because the IDS thinks that the communication session has ended

>**Urgency Flag**: The urgency flag in the TCP marks data as urgent. TCP uses an urgency pointer that points to the beginning of urgent data within a packet. When the user sets the urgency flag, the TCP ignores all data before the urgency pointer, and the data to which the urgency pointer points is processed. If the URG flag is set, the TCP sets the Urgent Pointer field to a 16-bit offset value that points to the last byte of urgent data in the segment. Some IDS do not consider the TCP’s urgency feature and process all the packets in the traffic, whereas the target system processes only the urgent data. Attackers exploit this feature to evade the IDS, as seen in other evasion techniques.

>**Overlapping Fragments**: Attackers use overlapping fragments to evade IDS. In this technique, attackers generate a series of tiny fragments with overlapping TCP sequence numbers. 

>**Polymorphic Shellcode**: Polymorphic shellcode attacks include multiple signatures, making it difficult to detect the signature. Attackers encode the payload using some technique and then place a decoder before the payload. As a result, the shellcode is completely rewritten each time it is sent, thereby evading detection. With polymorphic shellcodes, attackers hide their shellcode (attack code) by encrypting it with an unknown encryption algorithm and including the decryption code as part of the attack packet. To carry out polymorphic shellcode attacks, they use an existing buffer-overflow exploit and set the “return” memory address on the overflowed stack to the entrance point of the decryption code

### Which of the following techniques is used by an attacker to exploit a host computer and results in the IDS discarding packets while the host that must receive the packets accepts them?


- **Evasion**
- Session splicing
- Obfuscation
- Fragmentation attack

Explanation:
>**Obfuscating**: Obfuscating is an IDS evasion technique used by attackers to encode the attack packet payload in such a way that the destination host can only decode the packet but not the IDS. An attacker manipulates the path referenced in the signature to fool the HIDS. Using Unicode characters, an attacker can encode attack packets that the IDS would not recognize but which an IIS web server can decode

>**Session splicing**: Session splicing is an IDS evasion technique that exploits how some IDS do not reconstruct sessions before pattern-matching the data. It is a network-level evasion method used to bypass IDS where an attacker splits the attack traffic into an excessive number of packets such that no single packet triggers the IDS

>**Evasion**: An “evasion” attack occurs when the IDS discards packets while the host that has to get the packets accepts them. Using this technique, an attacker exploits the host computer. Evasion attacks have an adverse effect on the accuracy of the IDS

>**Fragmentation attack**: Fragmentation can be used as an attack vector when fragmentation timeouts vary between the IDS and the host. Through the process of fragmenting and reassembling, attackers can send malicious packets over the network to exploit and attack systems.

### Which evasion technique is used by attackers to encode the attack packet payload in such a way that the destination host can only decode the packet but not the IDS?


- Session splicing
- Unicode evasion
- Fragmentation attack
- **Obfuscation**

Explanation:

>**Obfuscation**: Obfuscation means to make the code harder to understand or read, generally for privacy or security purposes. A tool called an obfuscator converts a straightforward program into that works the same way but is much harder to understand.

>**Obfuscating**: Obfuscating is an IDS evasion technique used by attackers to encode the attack packet payload in such a way that the destination host can only decode the packet but not the IDS. An attacker manipulates the path referenced in the signature to fool the HIDS.

>**Session splicing**, **unicode evasion**, and **fragmentation attack** are also IDS evading techniques that use different ways to evade IDS.



### Which network-level evasion method is used to bypass IDS where an attacker splits the attack traffic in too many packets so that no single packet triggers the IDS?


- Overlapping fragments
- Unicode evasion
- Fragmentation attack
- **Session splicing**

Explanation:

>**Session splicing**: Session splicing is an IDS evasion technique that exploits how some IDSs do not reconstruct sessions before pattern-matching the data. It is a network-level evasion method used to bypass IDS where an attacker splits the attack traffic in too many packets such that no single packet triggers the IDS. The attacker divides the data into the packets into small portions of bytes and while delivering the data evades the string match. Attackers use this technique to deliver the data into several small-sized packets. Overlapping fragments and fragmentation attack evade IDS by using fragments of packet, whereas in unicode evasion is done by exploiting unicode characters. 


### Which of the following attack techniques is used by an attacker to exploit the vulnerabilities that occur while processing the input parameters of end users and the server responses in a web application?


- MITM attack
- Denial-of-service attack
- Social engineering attack
- **XSS attack**

Explanation:
>**Social engineering Attack**: Social engineering and data-driven attacks whereby the attacker sends malicious links and emails to employees inside the network.

>**Denial of Service Attack**: The attacker identifies a point of network processing that requires the allocation of a resource, causing a condition to occur in which all of that resource is consumed. The resources affected by the attacker are CPU cycles, memory, disk space, and network bandwidth. Attackers monitor and attack the CPU capabilities of the IDS.

>**MITM Attack**: In MITM attacks, attackers use DNS servers and routing techniques to bypass firewall restrictions. They may either take over the corporate DNS server or spoof DNS responses to perform the MITM firewall attack.

>**XSS Attack**: XSS attack exploits vulnerabilities that occur while processing the input parameters of end users and the server responses in a web application. Attackers take advantage of these vulnerabilities to inject malicious HTML code into the victim website to bypass the WAF.

### Which of the following techniques is used by attackers for collecting information about remote networks behind firewalls, where the TTL value is used to determine ACL gateway filters and map networks by analyzing the IP packet response?


- Source routing 
- Tiny fragments
- **Firewalking**
- Banner grabbing

Explanation:

>**Banner Grabbing**: Banner grabbing is a simple method of fingerprinting that helps in detecting the vendor of a firewall and the firmware version. It identifies the service running on the system. Attackers use banner grabbing to fingerprint services and thus discover the services running on firewalls

>**Tiny Fragments**: Attackers create tiny fragments of outgoing packets, forcing some of the TCP packet’s header information into the next fragment. The IDS filter rules that specify patterns will not match with the fragmented packets owing to the broken header information. The attack will succeed if the filtering router examines only the first fragment and allows all the other fragments to pass through. This attack is used to avoid user-defined filtering rules and works when the firewall checks only for the TCP header information

>**Firewalking**: Firewalking is a method of collecting information about remote networks behind firewalls. It is a technique that uses TTL values to determine gateway ACL filters and map networks by analyzing the IP packet response. It probes ACLs on packet filtering routers/firewalls using the same method as tracerouting

>**Source Routing**: Using this technique, the sender of the packet designates the route (partially or entirely) that a packet should take through the network such that the designated route should bypass the firewall node. Thus, the attacker can evade firewall restrictions

### Which of the following tools is used to execute commands of choice by tunneling them inside the payload of ICMP echo packets if ICMP is allowed through a firewall?


- **Loki**
- HTTPTunnel
- AckCmd
- Anonymizer

Explanation:

>**Anonymizer**: Anonymous web-surfing sites help to browse the Internet anonymously and unblock blocked sites.

>**Loki**: ICMP tunneling is used to execute commands of choice by tunneling them inside the payload of ICMP echo packets.

>**AckCmd** (http://ntsecurity.nu) use ACK tunneling.

>**HTTPTunnel** uses technique of tunneling traffic across TCP port 80 to bypass firewall. 

### Which feature of Secure Pipes tool open application communication ports to remote servers without opening those ports to public networks?


- Remote forwards
- **Local forwards**
- SOCKS proxies
- Remote backwards

Explanation:

>Local forwards open application communication ports to remote servers without opening those ports to public networks. It brings the security of VPN communication to clients and servers on an ad hoc basis without the configuration and management hassle.

### Which term is used to refer service announcements provided by services in response to connection requests and often carry vendor’s version of information?


- Network discovery phase
- **Banner**
- Port
- Scanning phase

Explanation:

>**Port**: Through ports computers send or accept information from network resources.

>**Network discovery phase** and a scanning phase are two phases involved in Firewalking.

>**Banner** is used to refer to service announcements provided by services in response to connection requests and often carry vendor’s version of information.

### In which of the following techniques do attackers first send payloads to the WAF connected to their local network to identify the payloads that can be used for evasion and then send those payloads to the target WAF for evasion?


- Function testing
- Runtime execution path profiling
- Code emulation
- **Fuzzing/brute-forcing**

Explanation:

>**Code Emulation**: Using code emulation, antivirus software executes a virtual machine to mimic CPU and memory activities. Here, virus code is executed on the virtual machine instead of the real processor. Code emulation efficiently deals with encrypted and polymorphic viruses.

>**Fuzzing/Brute-forcing**: Attackers first send payloads to the WAF connected to their local network to identify the payloads that can be used for evasion. They then send those payloads to the target WAF for evasion. In this process, attackers use wordlists such as SecLists Fuzzing Database (https://github.com) and FuzzDB Attack Patterns (https://github.com) to perform fuzzing on the target network. Attackers first load the wordlist into a fuzzer to start the brute-forcing attempts. They record all the responses received for the fuzzed payloads. Now, they use random user-agents and proxy chains to evade WAF.

>**Runtime Execution Path Profiling**: The runtime execution path profiling technique compares runtime execution path profiling of all system processes and executable files. The rootkit adds a new code near to a routine’s execution path to destabilize it. The method hooks several instructions executed before and after a certain routine, as these can be significantly different. 

>**Function Testing**: Function testing is a type of software testing technique whereby a software or a system is tested against a set of inputs according to the end user’s needs.

### Which of the following tools is used by attackers to bypass antivirus software by utilizing binary deconstruction, insertion of arbitrary assembly code, and reconstruction?


- **Ghostwriting.sh** 
- Colasoft Packet Builder
- FaceNiff
- KFSensor

Explanation:

>**Ghostwriting.sh**: Ghostwriting is used to bypass antivirus software by utilizing binary deconstruction, insertion of arbitrary assembly code, and reconstruction. It uses the built-in Metasploit tools to perform these actions. Ghostwriting.sh is a tool to automate this process.

>**Colasoft Packet Builder**: Colasoft Packet Builder is used to create custom network packets and fragmenting packets. Attackers use this tool to create custom malicious packets and fragment them such that firewalls cannot detect them.

>**KFSensor**: KFSensor is a host-based IDS that acts as a honeypot to attract and detect hackers and worms by simulating vulnerable system services and Trojans.

>**FaceNiff**: FaceNiff is an Android app that can sniff and intercept web session profiles over a Wi-Fi connection to a mobile.


### Identify the evasion technique in which attackers perform DDL hijacking to place a malicious DLL with a legitimate name that the application is looking for in the same directory where the executable resides and then the malicious DLL gets executed along with the application to disable the endpoint security.


- Using blacklist detection
- Overlapping fragments
- Fake security applications
- **Application whitelisting**

Explanation:
>**Overlapping Fragments**: Attackers use overlapping fragments to evade IDS. In this technique, attackers generate a series of tiny fragments with overlapping TCP sequence numbers.

>**Application Whitelisting**: Application whitelisting is a security feature in Windows systems to defend against insecure or malicious application execution. It contains the list of signed applications that are allowed to run in the system. While executing a legitimate and signed application, it looks for the required DLLs in the current location where the executable is saved and then searches in other locations. Attackers perform DDL hijacking to place a malicious DLL with a legitimate name that the application is looking for in the same directory where the executable resides. Then, the malicious DLL gets executed along with the application to disable endpoint security.

>**Using Blacklist Detection**: Attackers can abuse the WAF blacklist detection mechanism to bypass WAF. For this purpose, attackers fingerprint the target WAF to identify blacklisted keywords. By identifying the blacklisted keywords, attackers create new regex and payloads with keywords not included in the blacklists.

>**Fake Security Applications**: Attackers may send a fake security application to perform mobile-based social engineering. In this attack, the attacker first infects the victim’s computer by sending something malicious. They then upload a malicious application to an app store.

### Which of the following is a cyber defense software suite with antivirus, anti-malware, and intrusion detection capabilities?


- Followerwonk
- Mention
- Euromonitor
- **Symantec Endpoint Protection** 

Explanation:

>**Symantec Endpoint Protection**: Symantec Endpoint Protection (SEP) is a cyber defense software suite with antivirus, anti-malware and intrusion detection capabilities. Attackers use the following steps to bypass the SEP solution to execute malicious payload, gain persistence, and dump credentials from the target machine.

>**Euromonitor**: Euromonitor provides strategy research capabilities for consumer markets. It publishes reports on industries, consumers, and demographics.

>**Mention**: Mention is an online reputation tracking tool that helps attackers in monitoring the web, social media, forums, and blogs to learn more about the target brand and industry.

>**Followerwonk**: Followerwonk helps you explore and grow your social graph: Dig deeper into Twitter analytics: Who are your followers? Where are they located? When do they tweet?

### Which of the following techniques helps an attacker circumvent blacklists and hide the C&C server behind the compromised systems operating as reverse proxies?


- WHOIS lookup
- Web application fuzz testing
- **Fast flux DNS method**
- Reverse DNS lookup

Explanation:

>**Whois Lookup**: An attacker can query a Whois database server to obtain information regarding the target domain, and the Whois server responds to the query with the requested information. Using this information, an attacker can create a map of the organization’s network, mislead domain owners with social engineering, and obtain internal details of the network.

>**Reverse DNS Lookup**: DNS lookup is used to find the IP addresses for a given domain name, and a reverse DNS operation is performed to obtain the domain name of a given IP address.

>**Web Application Fuzz Testing**: Web application fuzz testing (fuzzing) is a blackbox testing method. It is a quality checking and assurance technique used to identify coding errors and security loopholes in web applications.

>**Fast Flux DNS Method**: Attackers can implement malware that uses various tricks for executing code that cannot be detected by security solutions. The fast flux method allows attackers to change both the IP addresses and DNS names rapidly and is typically utilized by large botnets. This technique allows attackers to evade various security controls. It also helps the attacker to circumvent blacklists and hide the C&C server behind the compromised systems operating as reverse proxies. In this process, a victim system will only connect to the fast flux agents instead of the legitimate C&C server.

### Which of the following is a honeypot application that captures rootkits and other malicious malware that hijacks the read() system call?


- Fake AP
- Bait and switch 
- Tar pits
- **Sebek**

Explanation:

>**Fake AP**: Fake access points are those that create fake 802.11b beacon frames with randomly generated ESSID and BSSID (MAC address) assignments. Fake access points only send beacon frames but do not produce any fake traffic on the access points, and an attacker can monitor the network traffic and quickly note the presence of fake AP.

>**Sebek**: Sebek is a server/client-based honeypot application that captures the rootkits and other malicious malware that hijacks the read() system call. Such honeypots record all the data accessed via reading () call. Attackers can detect the existence of Sebek-based honeypots by analyzing the congestion in the network layer, as Sebek data communication is usually unencrypted

>**Bait and Switch Honeypots**: Bait and switch honeypots actively participate in security mechanisms that are employed to respond quickly to incoming threats and malicious attempts. They redirect all malicious network traffic to a honeypot after any intrusion attempt is detected. An attacker can identify the presence of such honeypots by looking at specific TCP/IP parameters such as the Round-Trip Time (RTT), the Time To Live (TTL), and the TCP timestamp.

>**Tar Pits**: Tar pits are security entities that are similar to honeypots, which are designed to respond slowly to incoming requests. They slow down unauthorized attempts of hackers.

### Which of the following practices helps security professionals defend their network against firewall bypass attempts?


- The firewall should be configured such that the IP address of an intruder should not be filtered out
- By default, enable all FTP connections to or from the network
- **Use HTTP Evader to run automated testing for suspected firewall evasions**
- Never configure a remote syslog server

Explanation:

>How to Defend Against Firewall Evasion: 
>- Use HTTP Evader to run automated testing for suspected firewall evasions.
>- The firewall should be configured such that the IP address of an intruder should be filtered out.
>- Configure a remote syslog server and apply strict measures to protect it from malicious users.
>- Monitor firewall logs at regular intervals and investigate all suspicious log entries.
>- By default, disable all FTP connections to or from the network.

