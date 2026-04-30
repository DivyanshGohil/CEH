### In which of the following scanning techniques does an attacker send a spoofed source address to a computer to determine the available services?


- Inverse TCP flag scan
- **IDLE/IPID header scan**
- ACK flag probe scan
- TCP Maimon scan

Explanation:

>**Inverse TCP Flag Scan**: Attackers send TCP probe packets with a TCP flag (FIN, URG, PSH) set or with no flags. When the port is open, the attacker does not get any response from the host, whereas when the port is closed, he or she receives the RST from the target 

>**ACK Flag Probe Scan**: Attackers send TCP probe packets with the ACK flag set to a remote device and then analyze the header information (TTL and WINDOW field) of the received RST packets to find out if the port is open or closed. The ACK flag probe scan exploits the vulnerabilities within the BSD-derived TCP/IP stack. Thus, such scanning is effective only on those OSs and platforms on which the BSD derives TCP/IP stacks.
    
>**TCP Maimon scan**: This scan technique is very similar to NULL, FIN, and Xmas scan, but the probe used here is FIN/ACK. In most cases, to determine if the port is open or closed, the RST packet should be generated as a response to a probe request. However, in many BSD systems, the port is open if the packet gets dropped in response to a probe
    
>**IDLE/IPID Header Scan**: The IDLE/IPID Header scan is a TCP port scan method that you can use to send a spoofed source address to a computer to find out what services are available. It offers complete blind scanning of a remote host. Most network servers listen on TCP ports, such as web servers on port 80 and mail servers on port 25. A port is considered “open” if an application is listening on the port

### Which of the following OS discovery techniques is used by an attacker to identify a target machine’s OS by observing the TTL values in the acquired scan result?


- OS discovery using Nmap
- **OS discovery using Unicornscan**
- OS discovery using Nmap Script Engine
- OS discovery using IPv6 fingerprinting

Explanation:

    
>**OS Discovery using Nmap**: Nmap is one of the effective tools for performing OS discovery activities. In Zenmap, the -O option is used to perform OS discovery, which displays the OS details of the target machine.
    
>**OS Discovery using Unicornscan**: In unicornscan, the OS of the target machine can be identified by observing the TTL values in the acquired scan result. To perform Unicornscan, the syntax #unicornscan <target IP address> is used.
    
>**OS Discovery using Nmap Scripting Engine**: NSE in Nmap can be used to automate a wide variety of networking tasks by allowing users to write and share scripts. These scripts can be executed parallelly with the same efficiency and speed as Nmap. Attackers can also use various scripts in the Nmap Script Engine for performing OS discovery on the target machine.
    
>**OS Discovery using IPv6 Fingerprinting**: It is another technique used to identify the OS running on the target machine. It has the same functionality as IPv4, such as sending probes, waiting and collecting the responses, and matching them with the database of fingerprints.



### Which of the following IDS/firewall evasion techniques is used by an attacker to bypass Internet censors and evade certain IDS and firewall rules?


- **Anonymizers**
- IP address decoy
- Source port manipulation
- Sending bad checksums

Explanation:

    
>**IP Address Decoy**: The attacker generates or manually specifies IP addresses of decoys so that the IDS/firewall cannot determine the actual IP address
    
>**Sending Bad Checksums**: The attacker sends packets with bad or bogus TCP/UPD checksums to the intended target.
    
>**Source Port Manipulation**: The attacker manipulates the actual source port with the common source port to evade the IDS/firewall.
    
>**Anonymizers**: The attacker uses anonymizers, which allows them to bypass Internet censors and evade certain IDS and firewall rules.



