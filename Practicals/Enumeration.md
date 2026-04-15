# Enumeration
The objective of the lab is to extract information about the target organization that includes, but is not limited to:

*   Machine names, their OSes, services, and ports
*   Network resources
*   Usernames and user groups
*   Lists of shares on individual hosts on the network
*   Policies and passwords
*   Routing tables
*   Audit and service settings
*   SNMP and FQDN details

## Lab 1: Perform NetBIOS Enumeration

NetBIOS stands for Network Basic Input Output System. Windows uses NetBIOS for file and printer sharing. A NetBIOS name is a unique computer name assigned to Windows systems, comprising a 16-character ASCII string that identifies the network device over TCP/IP. The first 15 characters are used for the device name, and the 16th is reserved for the service or name record type.

### Task 1: Perform NetBIOS Enumeration using Windows Command-Line Utilities

  
nbtstat -a \[IP address of the remote machine\]  
> In this command, -a displays the NetBIOS name table of a remote computer.

  
nbtstat -c  
> In this command, -c lists the contents of the NetBIOS name cache of the remote computer.  
 

net use

> The output displays information about the target such as connection status, shared folder/drive and network information

### Task 2: Perform NetBIOS Enumeration using NetBIOS Enumerator

  
NetBIOS Enumerator is a tool that enables the use of remote network support and several other techniques such as SMB (Server Message Block). It is used to enumerate details such as NetBIOS names, usernames, domain names, and MAC addresses for a given range of IP addresses.

### Task 3: Perform NetBIOS Enumeration using an NSE Script

nmap -sV -v --script nbstat.nse \[Target IP Address\]  
> \-sV detects the service versions, -v enables the verbose output (that is, includes all hosts and ports in the output), and --script nbstat.nse performs the NetBIOS enumeration.

nmap -sU -p 137 --script nbstat.nse \[Target IP Address\]  
> \-sU performs a UDP scan, -p specifies the port to be scanned, and --script nbstat.nse performs the NetBIOS enumeration.

**Other tools may also be used to perform NetBIOS enumeration on the target network such as:**  
Global Network Inventory (http://www.magnetosoft.com),   
Advanced IP Scanner (https://www.advanced-ip-scanner.com),   
Hyena (https://www.systemtools.com),  
Nsauditor Network Security Auditor (https://www.nsauditor.com).

## Lab 2: Perform SNMP Enumeration

SNMP (Simple Network Management Protocol) is an application layer protocol that runs on UDP (User Datagram Protocol) and maintains and manages routers, hubs, and switches on an IP network. SNMP agents run on networking devices on Windows and UNIX networks.

SNMP enumeration uses SNMP to create a list of the user accounts and devices on a target computer. SNMP employs two types of software components for communication: the SNMP agent and SNMP management station. The SNMP agent is located on the networking device, and the SNMP management station communicates with the agent.

### Task 1: Perform SNMP Enumeration using snmp-check

SNMP uses port 161 by default  
 

### Task 2: Perform SNMP Enumeration using SoftPerfect Network Scanner

SoftPerfect Network Scanner can ping computers, scan ports, discover shared folders, and retrieve practically any information about network devices via WMI (Windows Management Instrumentation), SNMP, HTTP, SSH, and PowerShell.

### Task 3: Perform SNMP Enumeration using SnmpWalk

  
SnmpWalk is a command line tool that scans numerous SNMP nodes instantly and identifies a set of variables that are available for accessing the target network. It is issued to the root node so that the information from all the sub nodes such as routers and switches can be fetched.  

**snmpwalk -v1 -c public \[target IP\]**
 
> -v: specifies the SNMP version number (1 or 2c or 3) and -c: sets a community string.

### Task 4: Perform SNMP Enumeration using Nmap

nmap -sU -p 161 --script=snmp-sysdescr \[target IP Address\]  
> The result appears displaying information regarding SNMP server type and operating system details

>\-sU -p 161 --script=snmp-processes \[target IP Address\]  
The result appears displaying a list of all the running SNMP processes along with the associated ports on the target machine

nmap -sU -p 161 --script=snmp-win32-software \[target IP Address\]  
> The result appears displaying a list of all the applications running on the target machine

nmap -sU -p 161 --script=snmp-interfaces \[target IP Address\]  
> The result appears displaying information about the Operating system, network interfaces, and applications that are installed on the target machine

## Lab 3: Perform LDAP Enumeration

LDAP (Lightweight Directory Access Protocol) is an Internet protocol for accessing distributed directory services over a network. LDAP uses DNS (Domain Name System) for quick lookups and fast resolution of queries. A client starts an LDAP session by connecting to a DSA (Directory System Agent), typically on TCP port 389, and sends an operation request to the DSA, which then responds. BER (Basic Encoding Rules) is used to transmit information between the client and the server. One can anonymously query the LDAP service for sensitive information such as usernames, addresses, departmental details, and server names.

### Task 1: Perform LDAP Enumeration using Active Directory Explorer (AD Explorer)

### Task 2: Perform LDAP Enumeration using Python and Nmap

nmap -sU -p 389 \[Target IP address\]

nmap -p 389 --script ldap-brute --script-args ldap.base='"cn=users,dc=CEH,dc=com"' \[Target IP Address\]  
> \-p: specifies the port to be scanned, ldap-brute: to perform brute-force LDAP authentication. ldap.base: if set, the script will use it as a base for the password guessing attempts.

### Task 3: Perform LDAP Enumeration using ldapsearch

ldapsearch -h \[Target IP Address\] -x -s base namingcontexts  
> \-x: specifies simple authentication, -h: specifies the host, and -s: specifies the scope.

ldapsearch -h \[Target IP Address\] -x -b "DC=CEH,DC=com"  
> \-x: specifies simple authentication, -h: specifies the host, and -b: specifies the base DN for search.

ldapsearch -x -h \[Target IP Address\] -b "DC=CEH,DC=com" "objectclass=\*"  
> \-x: specifies simple authentication, -h: specifies the host, and -b: specifies the base DN for search.

## Lab 4: Perform NFS Enumeration

NFS (Network File System) is a type of file system that enables computer users to access, view, store, and update files over a remote server. This remote data can be accessed by the client computer in the same way that it is accessed on the local system.

### Task 1: Perform NFS Enumeration using RPCScan and SuperEnum

  
RPCScan communicates with RPC (remote procedure call) services and checks misconfigurations on NFS shares. It lists RPC services, mountpoints,and directories accessible via NFS. It can also recursively list NFS shares. SuperEnum includes a script that performs a basic enumeration of any open port, including the NFS port (2049).

## Lab 5: Perform DNS Enumeration

DNS enumeration techniques are used to obtain information about the DNS servers and network infrastructure of the target organization. DNS enumeration can be performed using the following techniques:
- Zone transfer  
- DNS cache snooping  
- DNSSEC zone walking

### Task 1: Perform DNS Enumeration using Zone Transfer

  
DNS zone transfer is the process of transferring a copy of the DNS zone file from the primary DNS server to a secondary DNS server.  

If the DNS transfer setting is enabled on the target DNS server, it will give DNS information; if not, it will return an error saying it has failed or refuses the zone transfer.

dig ns \[Target Domain\]
> In this command, ns returns name servers in the result

dig @\[\[NameServer\]\] \[\[Target Domain\]\] axfr  
> In this command, axfr retrieves zone information.  
 

### Task 2: Perform DNS Enumeration using DNSSEC Zone Walking

DNSSEC zone walking is a DNS enumeration technique that is used to obtain the internal records of the target DNS server if the DNS zone is not properly configured. The enumerated zone information can assist you in building a host network map.

./dnsrecon.py -d \[Target domain\] -z  
> In this command, -d specifies the target domain and -z specifies that the DNSSEC zone walk be performed with standard enumeration.

**Other DNSSEC zone enumerators:**  
- LDNS (https://www.nlnetlabs.nl),   
- nsec3map (https://github.com),   
- nsec3walker (https://dnscurve.org),  
- DNSwalk (https://github.com)   
  
### Task 3: Perform DNS Enumeration using Nmap  
  
nmap --script=broadcast-dns-service-discovery \[Target Domain\]  
> The result appears displaying a list of all the available DNS services on the target host along with their associated ports  
  
nmap -T4 -p 53 --script dns-brute \[Target Domain\]  
> \-T4: specifies the timing template, -p: specifies the target port.  
The result appears displaying a list of all the subdomains associated with the target host along with their IP addresses

nmap --script dns-srv-enum --script-args "dns-srv-enum.domain='\[Target Domain\]'"


## Lab 6: Perform SMTP Enumeration

The Simple Mail Transfer Protocol (SMTP) is an internet standard based communication protocol for electronic mail transmission. Mail systems commonly use SMTP with POP3 and IMAP, which enable users to save messages in the server mailbox and download them from the server when necessary. SMTP uses mail exchange (MX) servers to direct mail via DNS. It runs on TCP port 25, 2525, or 587.

### Task 1: Perform SMTP Enumeration using Nmap

nmap -p 25 --script=smtp-enum-users \[Target IP Address\]  
> \-p: specifies the port, and -script: argument is used to run a given script (here, the script is smtp-enum-users). The result appears displaying a list of all the possible mail users on the target machine

nmap -p 25 --script=smtp-open-relay \[Target IP Address\]  
> \-p: specifies the port, and -script: argument is used to run a given script (here, the script is smtp-open-relay).

nmap -p 25 --script=smtp-commands \[Target IP Address  
> \-p: specifies the port, and -script: argument is used to run a given script (here, the script is smtp-commands).


## Lab 7: Perform RPC, SMB, and FTP Enumeration

**RPC Enumeration:** Enumerating RPC endpoints enables vulnerable services on these service ports to be identified

**SMB Enumeration:** Enumerating SMB services enables banner grabbing, which obtains information such as OS details and versions of services running

**FTP Enumeration:** Enumerating FTP services yields information about port 21 and any running FTP services; this information can be used to launch various attacks such as FTP bounce, FTP brute force, and packet sniffing

### Task 1: Perform SMB and RPC Enumeration using NetScanTools Pro

NetScanTools Pro is an integrated collection of Internet information-gathering and network-troubleshooting utilities for network professionals. The utility makes it easy to find IPv4/IPv6 addresses, hostnames, domain names, email addresses, and URLs related to the target system.

### Task 2: Perform RPC, SMB, and FTP Enumeration using Nmap

nmap -T4 -A \[Target IP Address\]  
In this command, -T4: specifies the timing template (the number can be 0-5) and -A: specifies aggressive scan. The aggressive scan option supports OS detection (-O), version scanning (-sV), script scanning (-sC), and traceroute (--traceroute).

## Lab 8: Perform Enumeration using Various Enumeration Tools

### Task 1: Enumerate Information using Global Network Inventory

Global Network Inventory is used as an audit scanner in zero deployment and agent-free environments. It scans single or multiple computers by IP range or domain, as defined by the Global Network Inventory host file.

### Task 2: Enumerate Network Resources using Advanced IP Scanner

Advanced IP Scanner provides various types of information about the computers on a target network. The program shows all network devices, gives you access to shared folders, provides remote control of computers (via RDP and Radmin), and can even remotely switch computers off.

### Task 3: Enumerate Information from Windows and Samba Hosts using Enum4linux

Enum4linux is a tool for enumerating information from Windows and Samba systems. It is used for share enumeration, password policy retrieval, identification of remote OSes, detecting if hosts are in a workgroup or a domain, user listing on hosts, listing group membership information, etc.

enum4linux -u martin -p apple -n \[Target IP Address\]  
> In this command, -u user: specifies the username to use and -p pass: specifies the password.

enum4linux -u martin -p apple -U \[Target IP Address\]  
> In this command, -u user specifies the username to use, -p pass specifies the password and -U retrieves the userlist.

enum4linux -u martin -p apple -o \[Target IP Address\]  
> In this command, -u user specifies the username to use, -p pass specifies the password and -o retrieves the OS information.

enum4linux -u martin -p apple -P \[Target IP Address\]  
> In this command, -u user specifies the username to use, -p pass specifies the password and -P retrieves the password policy information.

enum4linux -u martin -p apple -G \[Target IP Address\]  
> In this command, -u user specifies the username to use, -p pass specifies the password and -G retrieves group and member list.

enum4linux -u martin -p apple -S \[Target IP Address\]  
> In this command, -u user specifies the username to use, -p pass specifies the password and -S retrieves sharelist.