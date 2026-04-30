Which of the following techniques makes a web server vulnerable to attacks?


Regularly updating the web server with the latest patches
Using different system administrator credentials everywhere 
Blocking unrestricted internal and outbound traffic
**Running unhardened applications and servers**

Explanation:
The following are some common oversights that make a web server vulnerable to attacks:
    • Failing to update the web server with the latest patches
    • Using the same system administrator credentials everywhere
    • Allowing unrestricted internal and outbound traffic
    • Running unhardened applications and servers


Which of the following stores critical HTML files related to the webpages of a domain name that will be served in response to requests?


Web proxy
Virtual document tree
Server root
**Document root**

Explanation:
    • Document root is one of the webserver’s root file directories that stores critical HTML files related to the webpages of a domain name that will serve in response to requests. For example, if the requested URL is www.certifiedhacker.com and the document root is named as certroot and is stored in /admin/web directory, then /admin/web/certroot is the document directory address. If the complete request is www.certifiedhacker.com/P-folio/index.html, the server will search for the file path /admin/web/certroot/P-folio/index.html.

In which of the following attack types does an attacker exploit the trust of an authenticated user to pass malicious code or commands to a web server?


Unvalidated input and file injection 
SQL injection attack
Cross-site scripting
**Cross-site request forgery** 

Explanation:
    • Unvalidated Input and File Injection Attacks: Unvalidated input and file-injection attacks are performed by supplying an unvalidated input or by injecting files into a web application.
    • SQL Injection Attacks: SQL injection exploits the security vulnerability of a database for attacks. The attacker injects malicious code into the strings, which are later passed on to the SQL server for execution.
    • Cross-Site Scripting (XSS) Attacks: In this method, an attacker injects HTML tags or scripts into a target website
    • Cross-Site Request Forgery (CSRF) Attack: An attacker exploits the trust of an authenticated user to pass malicious code or commands to the web server.

In which of the following attack types does an attacker modify the content of a web page by examining its HTML code and identifying form fields that lack valid constraints?


Directory traversal
Cross-site scripting (XSS) attack
Buffer overflow attack
**Command injection attack**

Explanation:
    • Directory Traversal: Directory traversal is the exploitation of HTTP through which attackers can access restricted directories and execute commands outside of the web server’s root directory by manipulating a URL
    • Buffer Overflow Attacks: The design of most web applications helps them in sustaining some amount of data. If that amount exceeds the storage space available, the application may crash or exhibit some other vulnerable behavior. An attacker uses this advantage and floods the application with an excess amount of data, causing a buffer overflow attack.
    • Command Injection Attacks: In this type of attack, a hacker alters the content of the web page by using HTML code and by identifying the form fields that lack valid constraints.
    • Cross-Site Scripting (XSS) Attacks: In this method, an attacker injects HTML tags or scripts into a target website.

Which of the following is not a session hijacking technique?


Session fixation
Session sidejacking
**DNS hijacking**
Cross-site scripting

Explanation:
    • Session fixation, session sidejacking, and cross-site scripting are some of the techniques for performing session hijacking, whereas DNS hijacking is not part of a session hijacking attack. DNS hijacking is a type of malicious attack that modifies or overrides a systems TCP/IP settings to redirect it at a rogue DNS server, thereby invalidating the default DNS settings.

Which of the following is a web security testing tool that can be used by an attacker to predict and use the next possible session ID token to take over a valid session?


**Burp Suite**
NCollector Studio
Netcraft 
Nikto2

Explanation:
    • Nikto2: Nikto is a vulnerability scanner used extensively to identify potential vulnerabilities in web applications and web servers
    • Netcraft: Netcraft determines the OS of the queried host by examining in detail the network characteristics of the HTTP response received from the website. Netcraft identifies vulnerabilities in the web server via indirect methods; the fingerprinting of the OS, installed software, and configuration of that software yields sufficient information to determine whether the server is vulnerable to an exploit. 
    • NCollector Studio: NCollector Studio is a website mirroring tool used to download content from the web to a local computer. This tool enables users to crawl for specific file types, make any website available for offline browsing, or simply download a website to a local computer.
    • Burp Suite: Burp Suite is a web security testing tool that can hijack session IDs in established sessions. The Sequencer tool in Burp Suite tests the randomness of session tokens. With this tool, an attacker can predict the next possible session ID token and use that to take over a valid session


Which of the following types of payload modules in the Metasploit framework is self-contained and completely stand-alone?


**Singles**
Stagers
Stages
Exploit 

Explanation:
    • Singles: Self-contained and completely standalone
    • Stagers: Sets up a network connection between the attacker and victim
    • Stages: Downloaded by stager modules
    • Exploit Module: It is a basic module in Metasploit used to encapsulate a single exploit, using which users target many platforms. This module has simplified meta-information fields. Using the Mixins feature, users can also dynamically modify exploit behavior, perform brute-force attacks, and attempt passive exploits
    
    
Which of the following countermeasures should be followed for the secure update and patch management of web servers?


Never use virtual patches in the organization
Enable all unused script extension mappings
**Apply all updates, regardless of their type, on an “as-needed” basis**
Use the default configurations that web servers are dispatched with 

Explanation:
The following are various countermeasures for secure update and patch management of web servers
    • Apply all updates, regardless of their type, on an “as-needed” basis
    • Avoid using default configurations that web servers are dispatched with
    • Use virtual patches in the organization because they provide additional identification/logging capabilities
    • Disable all unused script extension mappings
    • Test service packs and hotfixes on a representative non-production environment prior to deployment in production.
    • Ensure that server outages are scheduled and that a complete set of backup tapes and emergency repair disks are available.
    • Before applying any service pack, hotfix, or security patch, read and peer review all relevant documentation
    • Scan for existing vulnerabilities; patch and update the server software regularly.

Which of the following techniques is NOT a countermeasure to defend against web server attacks?


**Install IIS server on a domain controller**
Relocate sites and virtual directories to non-system partitions
Use a dedicated machine as a web server
Secure the SAM

Explanation:
The following are some other measures to defend against web server attacks.
    • Apply restricted ACLs and block remote registry administration.
    • Secure the SAM (stand-alone servers only).
    • Ensure that security-related settings are configured appropriately and that access to the metabase file is restricted with hardened NTFS permissions.
    • Remove unnecessary Internet Server Application Programming Interface (ISAPI) filters from the web server.
    • Remove all unnecessary file shares including the default administration shares, if they are not required.
    • Secure the shares with restricted NTFS permissions.
    • Relocate sites and virtual directories to non-system partitions and use IIS web permissions to restrict access.
    • Remove all unnecessary IIS script mappings for optional file extensions to avoid exploitation of any bugs in the ISAPI extensions that handle these types of files.
    • Enable a minimum level of auditing on the web server and use NTFS permissions to protect log files.
    • Use a dedicated machine as a web server.
    • Create URL mappings to internal servers cautiously.
    • Do not install the IIS server on a domain controller.
    • Use server-side session ID tracking and match connections with timestamps, IP addresses, etc.

Which of the following tools is a web-application security scanner that searches for vulnerabilities to attacks such as clickjacking, SQL injection, and XSS?


Immunity Debugger 
**N-Stalker X**
Vindicate
Mimikatz 

Explanation:
    • Mimikatz: Mimikatz allows attackers to pass Kerberos TGT to other computers and sign in using the victim’s ticket. The tool also helps in extracting plaintext passwords, hashes, PIN codes, and Kerberos tickets from memory. 
    • N-Stalker: N-Stalker is a web application security scanner that searches for vulnerabilities to attacks such as clickjacking, SQL injection, and XSS. It allows spider crawling throughout the application and the creation of web macros for form authentication. It also provides proxy capabilities for “drive-thru” attacks and identifies components through reverse proxies that distribute different platforms in the same application URL
    • Vindicate: Vindicate is an LLMNR/NBNS/mDNS spoofing detection toolkit for network administrators. Security professionals use this tool to detect name service spoofing.
    • Immunity Debugger: Immunity Debugger is a tool used to write exploits, analyze malware, and reverse engineer binary files.

Which of the following tools is employed by a pen tester to find vulnerabilities in an organization’s web server and evaluate its security posture by using the same techniques as those currently employed by cybercriminals? 


Netcraft 
**CORE Impact**
Pupy 
NetVizor

Explanation:
    • CORE Impact: CORE Impact finds vulnerabilities in an organization’s web server. This tool allows a user to evaluate the security posture of a web server by using the same techniques currently employed by cyber criminals.
    • Pupy: Pupy is a cross-platform, multi function RAT and post-exploitation tool used for executing applications remotely.
    • NetVizor: NetVizor is a desktop and child monitoring spyware that comes with an unparalleled task recording feature-set that in secret records everything employees do on your network. 
    • Netcraft: Netcraft provides Internet security services, including anti-fraud and anti-phishing services, application testing, and PCI scanning. They also analyze the market share of web servers, operating systems, hosting providers and SSL certificate authorities, and other parameters of the Internet.

A security administrator is looking for a patch management tool which scans organizational network and manages security and non-security patches. Which of the following patch management tool, he/she can use in order to perform the required task?


Netscan Pro
Nikto
Burp suite
**GFI LanGuard**

Explanation:
    • Among these, GFI LanGuard is the only patch management tool. It is a patch management tool that scans your network automatically and also installs and manages security and non-security patches. It supports machines across Microsoft®, MAC OS X® and Linux® operating systems as well as many third-party applications.
    • Netscan Pro is a network scanning tool and Nikto is a vulnerability assessment tool. Burp suite is a session hijacking tool.


Which of the following is true for automated patch management process?


Assess -> detect -> acquire -> deploy -> test -> maintain
Acquire -> assess -> detect -> deploy -> test -> maintain
Acquire -> assess -> detect -> test -> deploy -> maintain
**Detect -> assess -> acquire -> test -> deploy -> maintain**

Explanation:
    • In an automated patch management process, detect -> assess -> acquire -> test -> deploy -> maintain is the process that is followed. 

Which of the following terms refers to a set of hotfixes packed together? 


Patch
**Service pack**
Hotfix pack
Repair pack

Explanation:
    • Hotfixes are an update to fix a specific customer issue and not always distributed outside the customer organization. Vendors occasionally deliver hotfixes as a set of fixes called a combined hotfix or service pack.
    • A patch is a small piece of software designed to fix problems, security vulnerabilities, and bugs, and improve the usability or performance of a computer program or its supporting data. A patch can be considered as a repair job done to a programming problem.
