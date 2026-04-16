# System Hacking
In preparation for hacking a system, you must follow a certain methodology. You need to first obtain information during the footprinting, scanning, enumeration, and vulnerability analysis phases, which can be used to exploit the target system.

There are four steps in the system hacking:

**Gaining Access:** Use techniques such as cracking passwords and exploiting vulnerabilities to gain access to the target system

**Escalating Privileges:** Exploit known vulnerabilities existing in OSes and software applications to escalate privileges

**Maintaining Access:** Maintain high levels of access to perform malicious activities such as executing malicious applications and stealing, hiding, or tampering with sensitive system files

**Clearing Logs:** Avoid recognition by legitimate system users and remain undetected by wiping out the entries corresponding to malicious activities in the system logs, thus avoiding detection.

## Lab 1: Gain Access to the System

### Task 1: Perform Active Online Attack to Crack the System's Password using Responder

LLMNR (Link Local Multicast Name Resolution) and NBT-NS (NetBIOS Name Service) are two main elements of Windows OSes that are used to perform name resolution for hosts present on the same link. These services are enabled by default in Windows OSes and can be used to extract the password hashes from a user.

Responder is an LLMNR, NBT-NS, and MDNS poisoner. It responds to specific NBT-NS (NetBIOS Name Service) queries based on their name suffix. By default, the tool only responds to a File Server Service request, which is for SMB.

Here, we will use the Responder tool to extract information such as the target system's OS version, client version, NTLM client IP address, and NTLM username and password hash.

`sudo responder -I eth0`
> \-I: specifies the interface (here, eth0). However, the network interface might be different in your machine, to check the interface issue ifconfig command.

### Task 2: Audit System Passwords using L0phtCrack

L0phtCrack is a tool designed to audit passwords and recover applications. It recovers lost Microsoft Windows passwords with the help of a dictionary, hybrid, rainbow table, and brute-force attacks. It can also be used to check the strength of a password.

### Task 3: Find Vulnerabilities on Exploit Sites

Exploit sites contain the details of the latest vulnerabilities of various OSes, devices, and applications. You can use these sites to find relevant vulnerabilities about the target system based on the information gathered, and further download the exploits from the database and use exploitation tools such as Metasploit, to gain remote access.

- Exploit Database: https://www.exploit-db.com/  
- VulDB: https://vuldb.com  
- MITRE CVE: https://cve.mitre.org  
- Vulners: https://vulners.com  
- CIRCL CVE Search: https://cve.circl.lu

### Task 4: Exploit Client-Side Vulnerabilities and Establish a VNC Session

Attackers use client-side vulnerabilities to gain access to the target machine. VNC (Virtual Network Computing) enables an attacker to remotely access and control the targeted computers using another computer or mobile device from anywhere in the world. At the same time, VNC is also used by network administrators and organizations throughout every industry sector for a range of different scenarios and uses, including providing IT desktop support to colleagues and friends and accessing systems and services on the move.

### Task 5: Gain Access to a Remote System using Armitage

Armitage is a scriptable red team collaboration tool for Metasploit that visualizes targets, recommends exploits, and exposes the advanced post-exploitation features in the framework. Using this tool, you can create sessions, share hosts, capture data, downloaded files, communicate through a shared event log, and run bots to automate pen testing tasks.

### Task 6: Gain Access to a Remote System using Ninja Jonin

Ninja Jonin is a combination of two tools; Ninja is installed in victim machine and Jonin is installed on the attacker machine. The main functionality of the tool is to control a remote machine behind any NAT, Firewall and proxy.

### Task 7: Perform Buffer Overflow Attack to Gain Access to a Remote System

A buffer is an area of adjacent memory locations allocated to a program or application to handle its runtime data. Buffer overflow or overrun is a common vulnerability in applications or programs that accept more data than the allocated buffer. This vulnerability allows the application to exceed the buffer while writing data to the buffer and overwrite neighboring memory locations. Further, this vulnerability leads to erratic system behavior, system crash, memory access errors, etc. Attackers exploit a buffer overflow vulnerability to inject malicious code into the buffer to damage files, modify program data, access critical information, escalate privileges, gain shell access, etc.

Spike templates define the package formats used for communicating with the vulnerable server. They are useful for testing and identifying functions vulnerable to buffer overflow exploitation.

**generic\_send\_tcp 10.10.1.11 9999 stats.spk 0 0** command to send the packages to the vulnerable server.

>Here, **10.10.1.11** is the IP address of the target machine (**Windows 11**), **9999** is the target port number, **stats.spk** is the spike\_script, and **0** and **0** are the values of **SKIPVAR** and **SKIPSTR**.

>Overwriting the EIP register can allow us to gain shell access to the target system.

**Stack-Based Buffer Overflow**

Occurs when overflow happens in the stack memory. The stack stores, Local variables, Function return addresses, Overwriting the return address (EIP) allows attackers to redirect execution flow.

**Role of Registers**

- `EIP (Instruction Pointer):` Controls the next instruction to execute. Overwriting it gives full control of execution.  
- `ESP (Stack Pointer):` Points to the top of the stack where data or shellcode may reside.  
- `EAX, EBP:` General-purpose and base pointer registers affected during overflow.

**Spiking**

Spiking is used to identify vulnerable functions in an application. It involves sending crafted inputs using spike scripts. If the application crashes, the function is considered vulnerable.

**Fuzzing**

Fuzzing sends large or random data to the application. Purpose of fuzzing is to Identify crash points, Determine approximate buffer size, Helps in locating where overflow occurs.  
 

**Pattern Creation and Offset**

A unique pattern is generated and sent to the target.. When the program crashes, the overwritten EIP value is analyzed. The offset is the exact number of bytes required to reach and overwrite EIP.

**EIP Overwrite**

After finding the offset, controlled input is sent. This confirms whether the attacker can control execution flow. Successful overwrite means exploit development can proceed.

**Bad Characters**

Certain characters (e.g., \`\\x00\`) can terminate or alter payload execution. These are called bad characters. They must be identified and excluded from shellcode.

**Vulnerable Modules and Memory Protection**

Modern systems use protections like:
- ASLR (Address Space Layout Randomization)  
- DEP (Data Execution Prevention)

Attackers look for modules without protection.  Tools like **mona.py** help identify such modules.

**JMP ESP Technique**

Used to redirect execution to attacker-controlled data. The instruction JMP ESP points execution to the stack. The attacker places shellcode at the location pointed by ESP.

**Exploitation Flow**

1.  Identify vulnerable function
2.  Crash application
3.  Determine offset
4.  Overwrite EIP
5.  Redirect execution
6.  Inject shellcode
7.  Gain remote access

## Lab 2: Perform Privilege Escalation to Gain Higher Privileges

Privileges are a security role assigned to users for specific programs, features, OSes, functions, files, or codes. They limit access by type of user. Privilege escalation is required when you want to access system resources that you are not authorized to access. It takes place in two forms: vertical privilege escalation and horizontal privilege escalation.

*   **Horizontal Privilege Escalation**: An unauthorized user tries to access the resources, functions, and other privileges that belong to an authorized user who has similar access permissions
*   **Vertical Privilege Escalation**: An unauthorized user tries to gain access to the resources and functions of a user with higher privileges such as an application or site administrator

### Task 1: Escalate Privileges by Bypassing UAC and Exploiting Sticky Keys

`**Tool Used: metasploit-framework**`

## Lab 3: Maintain Remote Access and Hide Malicious Activities
 

**Remote Access:** Remote code execution techniques are often performed after initially compromising a system and further expanding access to remote systems present on the target network.

Discussed below are some of the remote code execution techniques:
- Exploitation for client execution  
- Scheduled task  
- Service execution

**Hiding Files:** Hiding files is the process of hiding malicious programs using methods such as rootkits, NTFS streams, and steganography techniques to prevent the malicious programs from being detected by protective applications such as Antivirus, Anti-malware, and Anti-spyware applications that may be installed on the target system. This helps in maintaining future access to the target system as a hidden malicious file provides direct access to the target system without the victim's consent.

### Task 1: User System Monitoring and Surveillance  
Refog facilitates monitoring of user activities in a controlled environment. It provides activity tracking through a secure account, recording keystrokes, monitoring application usage, and tracking website visits. It also captures screenshots of user activity for review purposes. The collected data can be accessed and analyzed to understand user behavior patterns and identify any unauthorized actions within an authorized setup.

### Task 2: Maintain Persistence by Modifying Registry Run Keys
Registry keys labeled as Run and RunOnce are crafted to automatically run programs upon each user login to the system. The command line specified as a key's data value is restricted to 260 characters or fewer. If attackers discover a service connected to a registry key with full permissions, they can execute persistence attacks or exploit privilege escalation. Upon any authorized user's login attempt, the associated service link within the registry triggers automatically.  
 

## Lab 4: Clear Logs to Hide the Evidence of Compromise

To remain undetected, the intruders need to erase all evidence of security compromise from the system. To achieve this, they might modify or delete logs in the system using certain log-wiping utilities, thus removing all evidence of their presence.

Various techniques used to clear the evidence of security compromise are as follow:

- **Disable Auditing:** Disable the auditing features of the target system  
- **Clearing Logs:** Clears and deletes the system log entries corresponding to security compromise activities  
- **Manipulating Logs:** Manipulate logs in such a way that an intruder will not be caught in illegal actions  
- **Covering Tracks on the Network:** Use techniques such as reverse HTTP shells, reverse ICMP tunnels, DNS tunneling, and TCP parameters to cover tracks on the network.  
- **Covering Tracks on the OS:** Use NTFS streams to hide and cover malicious files in the target system  
- **Deleting Files:** Use command-line tools such as Cipher.exe to delete the data and prevent its future recovery  
- **Disabling Windows Functionality:** Disable Windows functionality such as last access timestamp, Hibernation, virtual memory, and system restore points to cover tracks

### Task 1: Clear Windows Machine Logs using Various Utilities

  
Clear\_Event\_Viewer\_Logs.bat is a utility that can be used to wipe out the logs of the target system. This utility can be run through command prompt or PowerShell, and it uses a BAT file to delete security, system, and application logs on the target system. You can use this utility to wipe out logs as one method of covering your tracks on the target system.

A Command Prompt window with Administrator privileges appears. Run **wevtutil el** command to display a list of event logs.  

> el | enum-logs lists event log names.  
run wevtutil cl \[log\_name\] command (here, we are clearing system logs) to clear a specific event log.  

> cl | clear-log: clears a log, log\_name is the name of the log to clear, and ex: is the system, application, and security.  

wevtutil is a command-line utility used to retrieve information about event logs and publishers. You can also use this command to install and uninstall event manifests, run queries, and export, archive, and clear logs.

### Task 2: Clear Linux Machine Logs using the BASH Shell

The BASH or Bourne Again Shell is a sh-compatible shell that stores command history in a file called bash history. You can view the saved command history using the more **~/.bash\_history** command. This feature of BASH is a problem for hackers, as investigators could use the bash\_history file to track the origin of an attack and learn the exact commands used by the intruder to compromise the system.

run **export HISTSIZE=0** command to disable the BASH shell from saving the history.  
>HISTSIZE: determines the number of commands to be saved, which will be set to 0.

**history -c** command to clear the stored history.  
This command is an effective alternative to the disabling history command; with history -c, you have the convenience of rewriting or reviewing the earlier used commands.

**history -w** command to delete the history of the current shell, leaving the command history of other shells unaffected.

  
**shred ~/.bash\_history** command to shred the history file, making its content unreadable.

## Lab 5: Perform Active Directory (AD) Attacks Using Various Tools

Active Directory (AD) range attacks in ethical hacking involve exploiting vulnerabilities within AD's infrastructure. These attacks can include password spraying, Kerberoasting, and exploiting misconfigurations. Ethical hackers use these techniques to assess an organization's security, identify weaknesses, and recommend improvements to protect against real-world threats and unauthorized access.

### Task 1: Perform Initial Scans to Obtain Domain Controller IP and Domain Name

nmap shows that host 10.10.1.22 has port 88/TCP kerberos-sec and port 389/TCP LDAP opened which confirms that our DC IP address is 10.10.1.22.

scan 10.10.1.22 in more detail to obtain more information. Execute the **nmap -A -sC -sV 10.10.1.22** command.

### Task 2: Perform AS-REP Roasting Attack

An AS-REP roasting attack targets user accounts in AD that do not require Kerberos pre-authentication, exploiting the DONT\_REQ\_PREAUTH setting. Attackers can request a ticket-granting ticket (TGT) for these accounts without needing the user's password.

The DC responds with an encrypted TGT, which the attacker captures. This TGT, encrypted with the user's password hash, is then subjected to offline password-cracking tools such as **Hashcat** or **John the Ripper**. By rapidly guessing the password, the attacker can eventually decrypt the TGT, revealing the user's password.

`python3 GetNPUsers.py CEH.com/ -no-pass -usersfile /root/ADtools/users.txt -dc-ip 10.10.1.22`

>GetNPUsers.py: Python script to retrieve AD user information.

>CEH.com/: Target AD domain.

>-no-pass: Flag to find user accounts not requiring pre-authentication.

>-usersfile ~/ADtools/users.txt: Path to the file with the user account list.

>-dc-ip 10.10.1.22: IP address of the DC to query.  

`john --wordlist=/root/ADtools/rockyou.txt joshuahash.txt`
>This will crack the password hash and will give us the password in plain text.

### Task 3: Spray Cracked Password into Network using CrackMapExec.

Using CrackMapExec for password spraying involves leveraging its capabilities to automate the process. For instance, if "cupcake" is a cracked password, CME can be used to test this password against numerous user accounts and services across a network. This approach helps identify other accounts that may be using the same password, facilitating further penetration testing or security assessments.

`cme rdp 10.10.1.0/24 -u /root/ADtools/users.txt -p "cupcake"` to perform password spraying.  
> rdp: Targets the Remote Desktop Protocol (RDP) service.

> 10.10.1.0/24: IP address range to target, encompassing all hosts within the subnet 10.10.1.0 with a subnet mask of 255.255.255.0.

> \-u /root/ADtools/users.txt: Specifies the path to the file containing user accounts for authentication.

> \-p "cupcake": Password which we cracked using AS-REP Roasting to test against the RDP service on the specified hosts.

### Task 4: Perform Post-Enumeration using PowerView

PowerView is a PowerShell tool designed for network and AD enumeration. It helps security professionals gather detailed information about user accounts, groups, computers, and domain trusts. PowerView is used to identify potential security weaknesses and misconfigurations in an AD environment.

**Get-NetComputer** command in PowerShell. This command will display all the information related to computers in AD. It lists all computer objects in AD, which can help in identifying network targets and mapping the AD environment.

The **Get-NetGroup** command in PowerView lists all groups in AD, which helps in identifying group memberships and potential targets for privilege escalation.

**Get-NetUser** in PowerView retrieves detailed information about AD user accounts, such as usernames and group memberships.

Here are some other listed commands that you can use with PowerView.ps1 for enumeration:

- **Get-NetOU** - Lists all organizational units (OUs) in the domain.  
- **Get-NetSession** - Lists active sessions on the domain.  
- **Get-NetLoggedon** - Lists users currently logged on to machines.  
- **Get-NetProcess** - Lists processes running on domain machines.  
- **Get-NetService** - Lists services on domain machines.  
- **Get-NetDomainTrust** - Lists domain trust relationships.  
- **Get-ObjectACL** - Retrieves ACLs for a specified object.  
- **Find-InterestingDomainAcl** - Finds interesting ACLs in the domain.  
- **Get-NetSPN** - Lists service principal names (SPNs) in the domain.  
- **Invoke-ShareFinder** - Finds shared folders in the domain.  
- **Invoke-UserHunter** - Finds where domain admins are logged in.  
- **Invoke-CheckLocalAdminAccess** - Checks if the current user has local admin access on specified machines.  
   

### Task 5: Perform Attack on MSSQL service

**xp\_cmdshell** is a SQL server stored procedure enabling command shell execution. Misconfigured xp\_cmdshell can lead to arbitrary command execution, data exfiltration, and potential network compromise, posing significant security risks.

`hydra -L user.txt -P /root/ADtools/rockyou.txt 10.10.1.30 mssql` to brute force the MSSQL service password.

Execute command: `python3 /root/impacket/examples/mssqlclient.py CEH.com/SQL\_srv:batman@10.10.1.30 -port 1433`

Execute the SQL query `SELECT name, CONVERT(INT, ISNULL(value, value\_in\_use)) AS IsConfigured FROM sys.configurations WHERE name='xp\_cmdshell';`, returning a value of 1, indicating that xp\_cmdshell is enabled on the server.

Now, as we know that xp\_cmdshell is enabled on SQL server we can use Metasploit to exploit this service. 

### Task 6: Perform Privilege Escalation

WinPEASx64.exe is a tool for Windows privilege escalation, identifying misconfigurations and vulnerabilities for potential exploitation.

### Task 7: Perform Kerberoasting Attack

Rubeus is a tool for exploiting Kerberos weaknesses in Windows environments. Kerberoasting is a method to extract ticket granting ticket (TGT) hashes from AD. Attackers target service accounts with associated Kerberos service principal names (SPNs). TGTs are requested from the DC for these accounts, then cracked offline to reveal user passwords. Kerberoasting exploits weak service account passwords and the nature of Kerberos authentication.

`hashcat -m 13100 --force -a 0 hash.txt /root/ADtools/rockyou.txt`

> \-m 13100: This specifies the hash type. 13100 corresponds to Kerberos 5 AS-REQ Pre-Auth etype 23 (RC4-HMAC), a specific format for Kerberos hashes.

>\--force: This option forces Hashcat to ignore warnings and run even if there are compatibility issues. Use this with caution, as it might cause instability or incorrect results.

>\-a 0: This specifies the attack mode. 0 stands for a straight attack, which is a simple dictionary attack where Hashcat tries each password in the dictionary as it is.