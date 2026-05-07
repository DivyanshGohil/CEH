### In which of the following attack techniques does the attacker use a SOCKS proxy to harvest email addresses from web pages or other sources?


- **Spamming**
- Installing advertisement add-ons
- Sniffing traffic
- Google AdSense abuse

Explanation:

>**Sniffing traffic**: A packet sniffer observes the data traffic entering a compromised machine. It allows an attacker to collect sensitive information such as credit card numbers and passwords.

>**Google AdSense abuse**: Some companies permit showing Google AdSense ads on their websites for economic benefits. Botnets allow an intruder to automate clicks on an ad, producing a percentage increase in the click queue.

>**Installing advertisement add-ons**: Botnets can be used to perpetrate a “click fraud” by automating clicks.

>**Spamming**: Attackers use a SOCKS proxy for spamming. They harvest email addresses from web pages or other sources.

### Which of the following scanning methods makes use of the information obtained from an infected machine to find new vulnerable machines in a target network?


- Permutation scanning
- Random scanning
- **Topological scanning**
- Hit-list scanning

Explanation:

> **Topological Scanning**: This technique uses the information obtained from an infected machine to find new vulnerable machines. An infected host checks for URLs in the hard drive of a machine that it wants to infect. Subsequently, it shortlists URLs and targets, and it checks their vulnerability.

> **Permutation Scanning**: In this technique, attackers share a common pseudorandom permutation list of IP addresses of all machines.

> **Hit-list Scanning**: Through scanning, an attacker first collects a list of potentially vulnerable machines and then creates a zombie army. Subsequently, the attacker scans the list to find a vulnerable machine.

> **Random Scanning**: In this technique, the infected machine (an attacker’s machine or a zombie) probes IP addresses randomly in the target network’s IP range and checks their vulnerability.

### In which of the following attacks does an attacker use a combination of volumetric, protocol, and application-layer attacks to take down a target system or service?


- Peer-to-peer attack
- **Multi-vector attack**
- Slowloris attack
- HTTP GET/POST attack

Explanation:

>**Slowloris Attack**: Slowloris is a DDoS attack tool used to perform layer-7 DDoS attacks to take down web infrastructure. It is distinctly different from other tools in that it uses perfectly legitimate HTTP traffic to take down a target server.

>**Peer-to-Peer Attack**: A peer-to-peer attack is a form of DDoS attack in which the attacker exploits a number of bugs in peer-to-peer servers to initiate a DDoS attack.

>**Multi-Vector Attack**: In multi-vector DDoS attacks, the attacker uses combinations of volumetric, protocol, and application layer attacks to take down the target system or service.

>**HTTP GET/POST Attack**: HTTP attacks are layer-7 attacks. HTTP clients, such as web browsers, connect to a web server through HTTP to send HTTP requests, which can be either HTTP GET or HTTP POST. Attackers exploit these requests to perform DoS attacks.

### Which of the following is considered to be a smurf attack?


- **An attacker sends a large amount of ICMP traffic with a spoofed source IPaddress**
- An attacker sends a large number of TCP/user datagram protocol (UDP) connection requests
- An attacker sends a large number of TCP connection requests with spoofed source IPaddress
- An attacker sends a large amount TCP traffic with a spoofed source IPaddress

Explanation:

>In a smurf attack, the attacker sends a large number of ICMP request frames with a spoofed source IP address to the victim’s machine. Options (b), (c), and (d) are incorrect.

### Martha is a network administrator in a company named “Dubrovnik Walls Ltd.” She realizes that her network is under a DDoS attack. After careful analysis, she realizes that large amounts of UDP packets are being sent to the organizational servers that are present behind the “Internet facing firewall.”What type of DDoS attack is this?


- Protocol attack
- Application layer attack
- SYN flood attack
- **Volume (volumetric) attack**

Explanation:

>The answer is volume-based attack which includes UDP floods, ICMP floods, and other spoofed packet floods. It is not protocol attack, which includes SYN floods, fragmented packet attacks, ping of death attack, smurfDDoS, teardrop attack, land attack, and so on. It is not application layer attack, which includes GET/POST floods, attacks that targets web server, application or OS vulnerabilities, Slowloris, and so on. It is not SYN flood since this is part of protocol attacks.

### The DDoS tool created by anonymous sends junk HTTP GET and POST requests to flood the target, and its second version of the tool (the first version had different name) that was used in the so-called Operation Megaupload is called _______.


- Dereil
- Pandora DDoS
- **HOIC**
- BanglaDOS

Explanation:

>**HOIC** is the successor of low orbit ion cannon (**LOIC**) (which was used in operation payback by anonymous), and it is the version that has some additional features like hiding attacker’s geolocation.

>**BanglaDOS**, **Dereil**, and **Pandora DDoS** do not have direct connection with anonymous group.


### Which of the following techniques is a basic access-control list (ACL) filter that limits the impact of DDoS attacks by blocking traffic with spoofed addresses?


- DDoS prevention offerings from ISP or DDoS service
- Cisco IPS source IP reputation filtering
- Black-hole filtering
- **RFC 3704 filtering**

Explanation:

>**Cisco IPS Source IP Reputation Filtering**: Reputation services help in determining if an IP or service is a source of threat.

>**Black Hole Filtering**: Black hole filtering refers to discarding packets at the routing 

>**RFC 3704 Filtering**: RFC 3704 is a basic access-control list (ACL) filter, which limits the impact of DDoS attacks by blocking traffic with spoofed addresses.

>**DDoS Prevention Offerings from ISP or DDoS Service**: Enable IP Source Guard (in CISCO) or similar features in other routers to filter traffic based on the DHCP snooping binding database or IP source bindings, preventing a bot from succeeding with spoofed packets.

### Which of the following best practices should be followed to thwart DoS/DDoS attacks?


- Do not implement cognitive radios in the physical layer
- Allow return addresses to be overwritten
- Use functions such as gets and strcpy
- **Block all inbound packets originating from the service ports**

Explanation:

>The following is a list of countermeasures for combating DoS/DDoS attacks:
>- Use strong encryption mechanisms such as WPA2 and AES 256 for broadband networks to defend against eavesdropping
>- Ensure that the software and protocols are up-to-date and scan the machines thoroughly to detect any anomalous behavior
>- Update the kernel to the latest release and disable unused and insecure services
>- Block all inbound packets originating from the service ports to block the traffic from reflection servers
>- Enable TCP SYN cookie protection
>- Prevent the transmission of fraudulently addressed packets at the ISP level
>- Implement cognitive radios in the physical layer to handle jamming and scrambling attacks
>- Configure the firewall to deny external ICMP traffic access
>- Secure remote administration and connectivity testing
>- Perform thorough input validation
>- Stop data processed by the attacker from being executed
>- Prevent the use of unnecessary functions such as gets and strcpy
>- Prevent the return addresses from being overwritten

### Which of the following DoS/DDoS countermeasures strategy can you implement using a honeypot?


- Absorbing attacks 
- Degrading services
- **Deflecting attacks**
- Mitigating attacks

Explanation:

>Honeypots are intentionally set up with low security to gain the attention of the DDoS attackers. A honeypot attracts DDoS attackers, in that they will install handlers or agent code within the honeypot. This avoids compromising of more sensitive systems. Honeypots not only protect the actual system from attackers but also keep track of details about what the attackers are doing by storing the information in a record. This gives the owner of the honeypot a way to keep a record of handler and agent activity. Users can use this knowledge to defend against any future DDoS attacks.

### Which of the following DoS/DDoS protection appliances ensures reliable access to key network services by detecting and blocking external threats such as DDoS and other cyber-attacks before they escalate into costly service outages?


- Imperva Incapsula DDoS Protection
- **A10 Thunder TPS**
- DDoS-GUARD 
- Akamai DDoS Protection

Explanation:

>**Akamai DDoS Protection**: Online service that provides DDoS protection for enterprises regularly targeted by DDoS attacks

>**DDoS-GUARD**: Online service to protect against DDoS

> **A10 Thunder TPS**: Is an appliance that ensures reliable access to key network services by detecting and blocking external threats such as DDoS and other cyber-attacks before they escalate into costly service outages

> **Imperva Incapsula DDoS Protection**: Imperva Incapsula DDoS protection tool quickly mitigates attacks of any size without affecting legitimate traffic or increasing latency.




### In which of the following techniques does the attacking host itself transfer the attack toolkit to a newly discovered vulnerable system, exactly when it breaks into that system?


- Spyware propagation
- **Autonomous propagation**
- Back-chaining propagation
- Central source propagation

Explanation:


>**Back-chaining Propagation: In this technique, the attacker places an attack toolkit on their own system, and a copy of the attack toolkit is transferred to a newly discovered vulnerable system. The attack tools installed on the attacking machine use some special methods to accept a connection from the compromised system and then transfer a file containing the attack tools to it.

>**Autonomous Propagation: In autonomous propagation, the attacking host itself transfers the attack toolkit to a newly discovered vulnerable system, exactly at the time it breaks into that system.

>**Central Source Propagation: In this technique, the attacker places an attack toolkit on a central source and a copy of the attack toolkit is transferred to a newly discovered vulnerable system. Once the attacker finds a vulnerable machine, they instruct the central source to transfer a copy of the attack toolkit to the newly compromised machine, on which attack tools are automatically installed under management by a scripting mechanism.

>**Spyware Propagation: As its name implies, spyware is installed without user knowledge or consent, and this can be accomplished by “piggybacking” the spyware onto other applications.



### Edwards, a professional hacker, has targeted a Linux server hosted on the target organization’s network. To achieve his goal, he initiated sending multiple specially crafted packets to the server with a malformed maximum segment size (MSS). This forced the server’s buffer to exceed its sustainable limit, which led to a DoS attack. Which of the following attacks did Edwards perform in the above scenario?


- **TCP SACK panic attack**
- Misconfigured AP attack
- BlueBorne attack
- Agent smith attack

Explanation:

    
>**TCP SACK Panic Attack**: TCP Selective Acknowledgment (SACK) panic attack is a remote attack vector in which attackers attempt to crash the target Linux machine by sending SACK packets with malformed maximum segment size (MSS). To achieve this, attackers send specially designed SACK packets in sequence to the target server by setting the MSS to the lowest value (48 bytes). The lowest MSS value increases the number of TCP segments that need to be retransmitted. This selective retransmission causes the socket buffer of the target server to exceed the limit of 17 segments. Thus, the socket buffer exceeds the limit and triggers integer overflow, causing a kernel panic that leads to DoS.

>**Misconfigured AP Attack**: Most organizations spend significant amounts of time defining and implementing Wi-Fi security policies, but it may be possible for a client of a wireless network to change the security settings of an AP unintentionally. This, in turn, may lead to misconfigurations in APs.

>**Agent Smith Attack**: Agent Smith attacks are carried out by luring victims into downloading and installing malicious apps designed and published by attackers in the form of games, photo editors, or other attractive tools from third-party app stores such as 9Apps.

>**BlueBorne Attack**: A BlueBorne attack is performed on Bluetooth connections to gain access to and take full control of the target device.



