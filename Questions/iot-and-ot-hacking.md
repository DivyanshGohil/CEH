### Which of the following long-range wireless communication protocols is used for data transfer through small dish antennas for both broadband and narrowband data?


- QUIC
- **VSAT**
- PLC
- NFC

Explanation:

>**Very Small Aperture Terminal (VSAT)**: VSAT is a communication protocol that is used for data transfer using small dish antennas for both broadband and narrowband data.

>**QUIC**: Quick UDP Internet Connections (QUICs) are multiplexed connections between IoT devices over the User Datagram Protocol (UDP); they provide security equivalent to SSL/TLS.

>**Near-Field Communication (NFC)**: NFC is a type of short-range communication that uses magnetic field induction to enable communication between two electronic devices. It is primarily used in contactless mobile payment, social networking, and the identification of documents or other products.

>**Power-Line Communication (PLC)**: This is a type of protocol that uses electrical wires to transmit power and data from one endpoint to another. PLC is required for applications in different areas such as home automation, industrial devices, and broadband over power lines (BPL).


### Which of the following protocols is used to enable fast and seamless interaction with nearby IoT devices and reveals the list of URLs being broadcasted by nearby devices with BLE beacons?


- XMPP
- **Physical Web**
- LWM2M
- CoAP

Explanation:

>**LWM2M**: Lightweight Machine-to-Machine (LWM2M) is an application-layer communication protocol used for application-level communication between IoT devices; it is used for IoT device management.

>**CoAP**: Constrained Application Protocol (CoAP) is a web transfer protocol used to transfer messages between constrained nodes and IoT networks. This protocol is mainly used for machine-to-machine (M2M) applications such as building automation and smart energy.

>**XMPP**: eXtensible Messaging and Presence Protocol (XMPP) is an open technology for real-time communication used for IoT devices. This technology is used for developing interoperable devices, applications, and services for the IoT environment.

>**Physical Web**: Physical Web is a technology used to enable faster and seamless interaction with nearby IoT devices. It reveals the list of URLs being broadcast by nearby devices with BLE beacons.

### In which of the following IoT communication models does a device upload its data to the cloud to be later accessed or analyzed by third parties?


- **Back-end data-sharing communication model**
- Device-to-cloud communication model
- Device-to-device communication model
- Device-to-gateway communication model

Explanation:

>**Device-to-Gateway Communication Model**: In this model, the IoT device communicates with an intermediate device called a gateway, which in turn communicates with the cloud service.

>**Device-to-Cloud Communication Model**: In this type of communication, devices communicate with the cloud directly, rather than directly communicating with the client to send or receive data or commands. It uses communication protocols such as Wi-Fi or Ethernet, and sometimes uses Cellular as well.

>**Back-End Data-Sharing Communication Model**: This type of communication model extends the device-to-cloud communication type such that the data from the IoT devices can be accessed by authorized third parties. Here, devices upload their data onto the cloud, which is later accessed or analyzed by third parties.

>**Device-to-Device Communication Model**: Device-to-device communication is most commonly used in smart home devices such as thermostats, light bulbs, door locks, CCTV cameras, and fridges, which transfer small data packets to each other at a low data rate.

### Which of the following IoT technology components bridges the gap between the IoT device and the end user?


- Cloud server/data storage
- **IoT gateway**
- Sensing technology
- Remote control using mobile app

Explanation:

>**Sensing Technology**: Sensors embedded in the devices sense a wide variety of information from their surroundings like temperature, gases, location, working of some industrial machine as well as sensing health data of a patient.

>**IoT Gateways**: Gateways are used to bridge the gap between the IoT device (internal network) and the end user (external network) and thus allowing them to connect and communicate with each other. The data collected by the sensors in IoT devices send the collected data to the concerned user or cloud through the gateway.

>**Cloud Server/Data Storage**: The collected data after travelling through the gateway arrives at the cloud, where it is stored and undergoes data analysis. The processed data is then transmitted to the user where he/she takes certain action based on the information received by him/her.

>**Remote Control using Mobile App**: The end user uses remote controls such as mobile phones, tabs, laptops, etc. installed with a mobile app to monitor, control, retrieve data, and take a specific action on IoT devices from a remote location.

### Which of the following IoT architecture layers carries out communication between two end points such as device-to-device, device-to-cloud, device-to-gateway, and back-end data-sharing?


- **Internet layer**
- Edge technology layer
- Middleware layer
- Application layer
- Access gateway layer

Explanation:
> IoT Architecture

> The functions performed by each layer in the architecture are given below:
>- **Edge Technology Layer**: This layer consists of all the hardware parts like sensors, RFID tags, readers or other soft sensors and the device itself. These entities are the primary part of the data sensors that are deployed in the field for monitoring or sensing various phenomena. This layer plays an important part in data collection, connecting devices within the network and with the server.
>- **Access Gateway Layer**: This layer helps to bridge the gap between two endpoints like a device and a client. The very first data handling also takes place in this layer. It carries out message routing, message identification and subscribing.
>- **Internet Layer**: This is the crucial layer as it serves as the main component in carrying out the communication between two endpoints such as device-to-device, device-to-cloud, device-to-gateway and back-end data-sharing.
>- **Middleware Layer**: This is one of the most critical layers that operates in two-way mode. As the name suggests this layer sits in the middle of the application layer and the hardware layer, thus behaving as an interface between these two layers. It is responsible for important functions such as data management, device management and various issues like data analysis, data aggregation, data filtering, device information discovery and access control.
>- **Application Layer**: This layer placed at the top of the stack, is responsible for the delivery of services to the respective users from different sectors like building, industrial, manufacturing, automobile, security, healthcare, etc.

### Name the communication model where the IoT devices communicate with the cloud service through gateways?


- Device-to-cloud communication model
- Back-end data-sharing communication model
- Device-to-device communication model
**Device-to-gateway communication model**

Explanation:

>**Device-to-Device Communication Model**: In this type of communication, devices that are connected interact with each other through the internet but mostly they use protocols like ZigBee, Z-Wave or Bluetooth.

>**Device-to-Cloud Communication Model**: In this type of communication, devices communicate with the cloud directly rather than directly communicating with the client in order to send or receive the data or commands.

>**Device-to-Gateway Communication Model**: In the Device-to-Gateway communication, Internet of Things device communicates with an intermediate device called a Gateway, which in turn communicates with the cloud service.

>**Back-End Data-Sharing Communication Model**: This type of communication model extends the device-to-cloud communication type in which the data from the IoT devices can be accessed by authorized third parties. Here devices upload their data onto the cloud which is later accessed or analyzed by the third parties.

### Which of the following IoT threats is prone to various attacks such as buffer overflow that result in denial of service, leaving the device inaccessible to the user?


- Insecure default settings
- Insecure ecosystem interfaces
- Insecure data transfer and storage
- **Insecure network services**

Explanation:

>**Insecure Data Transfer and Storage**: Lack of encryption and access control of data that is in transit or at rest may result in leakage of sensitive information to malicious users.

>**Insecure Network Services**: Insecure network services are prone to various attacks like buffer overflow attacks, which cause a denial-of-service scenario, thus leaving the device inaccessible to the user.

>**Insecure Ecosystem Interfaces**: Insecure ecosystem interfaces such as web, backend API, mobile, and cloud interfaces outside the device lead to compromised security of the device and its components.

>**Insecure Default Settings**: Insecure or insufficient device settings restrict the operators from modifying configurations to make the device more secure.


### Name the IoT security vulnerability that gives rise to issues such as weak credentials, lack of account lockout mechanism, and account enumeration?


- Insecure network services
- Privacy concerns
- Insufficient authentication/authorization
- **Insecure web interface**

Explanation:

>**Insufficient Authentication/Authorization**: Insufficient authentication refers to using weak credentials such as an insecure or weak password which offers poor security, thus allowing a hacker to gain access to the user account, and causing loss of data, loss of accountability and denying user to access the account.

>**Insecure Network Services**: Insecure network services are prone to various attacks like buffer overflow attacks, attacks that cause denial-of-service scenario, thus leaving the device inaccessible to the user. An attacker uses various automated tools such as port scanners and fuzzers to detect the open ports and exploit them to gain unauthorized access to the services.

>**Insecure Web Interface**: Insecure web interface occurs when certain issues arise such as weak credentials, lack of account lockout mechanism and account enumeration. These issues result in loss of data, loss of privacy, lack of accountability, denial of access and complete device access takeover.

>**Privacy Concerns**: IoT devices generate some private and confidential data but due to lack of proper protection schemes, it leads to privacy concerns, which makes it is easy to discover and review the data that is being produced, sent, and collected.



### In which of the following attacks does an attacker use a malicious script to exploit poorly patched vulnerabilities in an IoT device?


- Replay attack
- **Exploit kits**
- Sybil attack
- Side channel attack

Explanation:

>**Sybil Attack**: An attacker uses multiple forged identities to create a strong illusion of traffic congestion, affecting communication between neighboring nodes and networks.

>**Side Channel Attack**: Attackers perform side channel attacks by extracting information about encryption keys by observing the emission of signals i.e. "side channels" from IoT devices.

>**Replay Attack**: Attackers intercept legitimate messages from a valid communication and continuously send the intercepted message to the target device to perform a denial-of-service attack or crash the target device.

>**Exploit Kits**: Exploit kit is a malicious script used by the attackers to exploit poorly patched vulnerabilities in an IoT device. These kits are designed in such a way that whenever there are new vulnerabilities, new ways of exploitation and add on functions will be added to the device automatically.

### Given below are the various steps involved in the Enemybot malware attack. Identify the correct sequence of steps involved in the Enemybot malware attack.
1. Gaining access
2. Disabling other malware on the target
3. Launching attack
4. Persistence
5. Creating exploits


- 5 -> 3 -> 4 -> 1 -> 2
- **5 -> 2 -> 1 -> 3 -> 4**
- 3 -> 4 -> 5 -> 1 -> 2 
- 1 -> 2 -> 3 -> 4 -> 5 

Explanation:

>Enemybot Attack Scenario:
>- Step 1: Creating Exploits
>- Step 2: Disabling Other Malware on the Target
>- Step 3: Gaining Access
>- Step 4: Launching Attack
>- Step 5: Persistence


### Identify the Enemybot malware attack stage in which the malware targets multiple architectures to spread its infection.


- Launching attack
- **Disabling other malware on the target**
- Creating exploits
- Persistence

Explanation:

>**Persistence**: The malware can obfuscate its strings using several techniques such as XOR encoding with several byte keys, single-byte XOR operation with 0x22, encryption of commands with substitution ciphers, and encoding of strings by appending the value three to every character.

>**Disabling Other Malware on the Target**: Enemybot targets multiple architectures to spread its infection. Apart from IoT devices, the malware can also infect desktop architectures such as i586, arm, arm5, arm64, arm7, Darwin, bsd, i686, m68k, mips, mpsl, ppc-440fp, sh4, spc, ppc, x64, and x86.

>**Launching Attack**: Exploiting the vulnerabilities, attackers can launch attacks beyond DDoS, such as crypto-mining attacks.

>**Creating Exploits**: Enemybot borrows some modules such as scanner and bot killer from Mirai’s source code and modifies it to identify vulnerable devices or processes to spread infection.


### Which of the following tools helps attackers find the details and certification granted to IoT devices?


- MultiPing
- RFCrack
- IoTSeeker
- **FCC ID Search**

Explanation:

>**MultiPing**: Attackers can use MultiPing to find the IP address of any IoT device in the target network.

>**RFCrack**: Attackers use the RFCrack tool to obtain the rolling code sent by the victim to unlock a vehicle and later use the same code for unlocking and stealing the vehicle

>**FCC ID Search**: It Search helps in finding the details and granted certification of the devices. FCC ID contains two elements: Grantee ID (initial three or five characters) and Product ID (remaining characters).

>**IoTSeeker**: It will scan a network for specific types of IoT devices to detect if they are using the default, factory set credentials.

### Given below are the steps used by the attackers to perform firmware analysis and reverse engineering.
1. Extract the file system
2. Emulate firmware for dynamic testing
3. Obtain firmware
4. Analyze the file-system content
5. Mount the file system
6. Analyze firmware
### What is the correct sequence of steps used by attackers to perform firmware analysis and reverse engineering?


- **3 -> 6 -> 1 -> 5 -> 4 -> 2**
- 2 -> 1 -> 5 -> 3 -> 4 -> 6
- 3 -> 1 -> 6 -> 5 -> 2 -> 4
- 5 -> 6 -> 3 -> 1 -> 4 -> 2

Explanation:

>Steps used by attackers to perform firmware analysis and reverse engineering:
> 1. Obtain Firmware
> 2. Analyze Firmware
> 3. Extract the Filesystem
> 4. Mount the Filesystem
> 5. Analyze the Filesystem Content
> 6. Emulate Firmware for Dynamic Testing

### Proper communication and storage encryption, no default credentials, strong passwords, and up-to-date components are the security considerations for which of the following component?


- Mobile
- **Edge**
- Gateway
- Cloud platform

Explanation:

>**Mobile**: An ideal framework for the mobile interface should include proper authentication mechanism for the user, account lockout mechanism after a certain number of failed attempts, local storage security, encrypted communication channels and the security of the data transmitted over the channel.

>**Cloud Platform**: A secure framework for the cloud component should include encrypted communications, strong authentication credentials, secure web interface, encrypted storage, automatic updates and so on.

>**Edge**: Framework consideration for edge would be proper communications and storage encryption, no default credentials, strong passwords, use latest up to date components and so on.

>**Gateway**: An ideal framework for the gateway should incorporate strong encryption techniques for secure communications between endpoints. Also, the authentication mechanism for the edge components should be as strong as any other component in the framework. Where ever possible the gateway should be designed in such a way that it authenticates multi-directionally to carry out trusted communication between the edge and the cloud. Automatic updates should also be provided to the device for countering vulnerabilities.


### Which of the following tools offers SaaS technology and assists in operating IoT products in a reliable, scalable, and secure manner?


- beSTORM
- DigiCert IoT security solution
- Firmalyzer Enterprise
- **SeaCat.io**

Explanation:

>**SeaCat.io**: SeaCat.io is a security-first SaaS technology to operate IoT products in a reliable, scalable and secure manner. It provides protection to end users, business, and data.

>**DigiCert IoT Security Solution**: DigiCert Home and Consumer IoT Security Solutions protect private data and home networks while preventing unauthorized access using PKI-based security solutions for consumer IoT devices.

>**Firmalyzer Enterprise**: Firmalyzer enables device vendors and security professionals to perform automated security assessment on software that powers IoT devices (firmware) in order to identify configuration and application vulnerabilities. This tool notifies users about the vulnerabilities discovered and assists to mitigate those in a timely manner.

>**beSTORM**: beSTORM is a smart fuzzer to find buffer overflow vulnerabilities by automating and documenting the process of delivering corrupted input and watching for unexpected response from the application. It supports multi-protocol environment and address breaches by testing over 50 protocols while providing automated binary and textual analysis, advanced debugging and stack tracing.

### In which of the following levels of the Purdue model can the analysis and alteration of the physical process be performed?


- Level 2
- Level 0
- **Level 1**
- Level 3

Explanation:

>**Level 0 (Physical Process)**: In this level, the actual physical process is defined, and the product is manufactured.

>**Level 2 (Control Systems/Area Supervisory Controls)**: Supervising, monitoring, and controlling the physical process is carried out at this level.

>**Level 1 (Basic Controls/Intelligent Devices)**: Analyzation and alteration of the physical process can be done at this level. The operations in basic control include “start motors,” “open valves,” “move actuators,” etc.

>**Level 3 (Operational Systems/Site Operations)**: In this level, the production management, individual plant monitoring, and control functions are defined.

### Which of the following components of an industrial control system contains a centralized supervisory control unit used to control multiple local controllers, thousands of input/output (I/O) points, and various other field devices that are part of the overall production process?


- SCADA
- SIS
- **DCS**
- BPCS

Explanation:

>**Basic Process Control System (BPCS)**: BPCS systems are dynamic in nature and are highly adaptable to changing process conditions. They are applicable to all sorts of control loops, including the temperature, batch, pressure, flow, feedback, and feedforward control loops used in industries such as the chemical, oil and gas, and food and beverages industries.

>**Supervisory Control and Data Acquisition (SCADA)**: SCADA systems provide centralized controlling and monitoring of multiple process inputs and outputs by integrating the data acquisition system with the data transmission system and HMI software.

>**Distributed Control System (DCS)**: It contains a centralized supervisory control unit used to control multiple local controllers, thousands of input/output (I/O) points, and various other field devices that are part of the overall production process.

>**Safety Instrumented Systems (SIS)**: Consists of logic solvers that are helpful in deciding the necessary action to be taken based on the gathered information. They provide actions for both failsafe and fault-tolerant situations. They act as controllers that capture signals from the sensors and execute pre-programmed actions to avoid risk by providing output to the final control elements.

### Which of the following protocols provides a flexible framework for addressing and mitigating current and future security vulnerabilities in industrial automation and control systems? 


- **ISA/IEC 62443**
- HSCP
- IEC 61850
- ICCP (IEC 60870-6)

Explanation:

>**ISA/IEC 62443**: ISA/IEC 62443 provides a flexible framework for addressing and mitigating current and future security vulnerabilities in industrial automation and control systems.

>**ICCP (IEC 60870-6)**: ICCP (Inter-Control Center Communications Protocol) (IEC 60870-6) provides a set of standards and protocols for covering ICS or SCADA communication in power system automation.

>**IEC 61850**: IEC 61850 is a common protocol that enables interoperability and communications between the IEDs at electrical substations.

>**HSCP**: Hybrid SCP (Secure Copy Protocol) is developed for transmitting larger file sizes at high speed on long-distance and wideband infrastructure.

### Which of the following techniques allows an attacker to achieve higher-level access and authorizations to perform further malicious activities on an ICS system or network?


-Obfuscating 
- Network address translation
- **Hooking**
- Activity profiling

Explanation:

>**Obfuscating**: Obfuscation means to make code more difficult to understand or read, generally for privacy or security purposes.

>**Privilege Escalation**: Privilege escalation allows an attacker to achieve higher-level access and authorizations to perform further malicious activities on an ICS system or network. Some of the techniques that can be used by an attacker to escalate privileges are as follows. 
>- **Exploiting software**: Attackers can take advantage of known software vulnerabilities by abusing any programming errors to elevate privileges.
>- **Hooking**: It allows attackers to hook into the APIs of different processes for redirecting and calling them to elevate privileges.

>**Activity Profiling**: Activity profiling is performed based on the average packet rate for network flow, which consists of consecutive packets with similar packet header information. The packet header information includes the IP addresses of the destination and sender, ports, and transport protocols used.

>**Network Address Translation**: Network address translation (NAT) separates IP addresses into two sets and enables the LAN to use these addresses for internal and external traffic. The NAT helps hide an internal network layout and force connections to go through a choke point.

### Identify the technique that allows an attacker to deactivate, control, or exploit the physical control processes within a target ICS environment using command and control.


- Alternative trusted medium
- Anti-disassembly
- **Connection proxy**
- Impersonation 

Explanation:

>**Impersonation**: Impersonation is a common human-based social engineering technique where an attacker pretends to be a legitimate or authorized person. Attackers perform impersonation attacks personally or use a phone or another communication medium to mislead their target and trick them into revealing information.

>**Alternative Trusted Medium**: The alternative trusted medium technique is the most reliable method used for detecting rootkits at the OS level.

>**Connection Proxy**: An attacker attempts to deactivate, control, or exploit the physical control processes within the target ICS environment using command and control. Attackers can control the traffic of the target network across the ICS environment using a connection proxy.

>**Anti-disassembly**: Anti-disassembly is a technique that uses specially crafted code or data in a program to produce an incorrect program listing by disassembly analysis tools.

### Peter, a professional hacker, managed to gain unauthorized access to a target ICS network. He wanted to thwart reactions to any security event such as a hazard or failure. For this purpose, Peter employed a technique to block command messages to stop defense solutions from reacting to any security event.
Identify the technique employed by Peter in the above scenario.


- Command and control
- Persistence
- Evasion 
- **Inhibit response function**

Explanation:

>**Evasion**: Attackers use this tactic to evade conventional defense mechanisms throughout their operations. Some of the techniques used to evade detection are removing the indicators, rootkits, and changing the operator mode.

>**Persistence**: Attackers employ persistence procedures to retain access within the ICS environment, even if the compromised device is restarted or the communication is interrupted. Some of the techniques that can be used by an attacker at this stage are modifying a program, module firmware, and project file infection.

>**Command and Control**: An attacker attempts to deactivate, control, or exploit the physical control processes within the target ICS environment using command and control. Some of the techniques used for command and control are frequently used ports, connection proxy, and standard application-layer protocol.

>**Inhibit Response Function**: The inhibition of response function refers to the different ways an attacker attempts to thwart reactions against any security event such as hazard or failure. Some of the techniques associated with this tactic are activate firmware update mode, block command messages and block reporting messages.

### In which of the following phases of MITRE ATT&CK for ICS does an attacker use various tactics such as I/O brute-forcing and parameter altering to disable, exploit, or control the physical control processes in the target environment?


- **Impair process control** 
- Lateral movement
- Collection 
- Privilege escalation

Explanation:

>**Impair Process Control**: Attackers use this tactic to disable, exploit, or control the physical control processes in the target environment. An attacker can re-program a device by injecting malicious firmware into it and thereby prepare it to perform other malicious tasks.

>**Collection**: Collection refers to various methods that an attacker uses to gather information and gain knowledge regarding the data and domains of the ICS infrastructure.

>**Lateral Movement**: Attackers attempt to make additional movements across the target ICS environment by leveraging the existing access.

>**Privilege Escalation**: Privilege escalation allows an attacker to achieve higher-level access and authorizations to perform further malicious activities on an ICS system or network.

### Which of the following phases of MITRE ATT&CK for ICS involves the use of techniques by an attacker to damage, disrupt, or gain control of the data and systems of the targeted ICS environment and its surroundings?


- Inhibit response function
- Impair process control
- Discovery
- **Impact**

Explanation:

>**Impair Process Control**: Attackers use this tactic to disable, exploit, or control the physical control processes in the target environment.

>**Impact**: Impact refers to the techniques used by an attacker to damage, disrupt, or gain control of the data and systems of the targeted ICS environment and its surroundings. 

>**Inhibit Response Function**: The inhibition of response function refers to the different ways an attacker attempts to thwart reactions against any security event such as hazard or failure.

>**Discovery**: Discovery is the process of gaining information about an ICS environment to assess and identify target assets.

### Which of the following online tools allows attackers to discover the default credentials of a device or product simply by entering the device name or manufacturer name?


- **CRITIFENCE**
- Thingful
- Censys
- Netcraft 

Explanation:

>**Censys**: Censys is a public search engine and data-processing facility backed by data collected from ongoing Internet-wide scans. Censys supports full-text searches on protocol banners and queries a wide range of derived fields. It can identify specific vulnerable devices and networks, and generate statistical reports on broad usage patterns and trends.

>**Thingful**: Thingful is a search engine for finding and using open IoT data from around the world. It helps organizations make better decisions with external IoT data.

>**CRITIFENCE**: CRITIFENCE is an online database that stores default passwords of critical infrastructure, SCADA, ICS, and the IIoT. Attackers can use this online tool to discover the default credentials of a device or product simply by entering the device name or its manufacturer’s name.

>**Netcraft**: Netcraft provides Internet security services, including anti-fraud and anti-phishing services, application testing, and PCI scanning.



### Which of the following tools passively maps and visually displays an ICS/SCADA network topology while safely conducting device discovery, accounting, and reporting on these critical cyber-physical systems?


- **GRASSMARLIN**
- Shodan
- Gqrx
- SCADA Shutdown Tool

Explanation:

>**GRASSMARLIN**: GRASSMARLIN is an open-source tool that passively maps and visually displays an ICS/SCADA network topology, while safely conducting device discovery, accounting, and reporting on these critical cyber-physical systems.

>**SCADA Shutdown Tool**: SCADA Shutdown Tool is an ICS testing and automation tool that allows attackers to fuzz, scan, and run remote commands on ICSs, SCADA networks, and controllers.

>**Shodan**: The Shodan search engine helps attackers to gather information about OT devices connected to the Internet. This online tool can be used to obtain details of SCADA systems that are used in water treatment plants, nuclear power plants, HVAC systems, electrical transmission systems, home heating systems, etc.

>**Gqrx**: Gqrx is an SDR implemented with the help of the GNU Radio and Qt GUI tool. Attackers use hardware devices such as FunCube dongles, Airspy, HackRF, and RTL-SDR along with Gqrx SDR, to analyze the spectrum.

### Which of the following commands helps attackers gather information and identify critical network activities of an ICS network?


- Invoke-Mimikatz -command '"lsadump::dcsync /domain:<Target Domain> /user:<krbtgt>\<Any Domain User>"
- **python -m fuzzowski printer1 631 -f ipp -r get_printer_attribs --restart smartplug**
- msfvenom -p windows/shell_reverse_tcp lhost=<Target IP Address> lport=444 -f exe > /home/attacker/Windows.exe
- run post/windows/gather/arp_scanner RHOSTS <target subnet range>

Explanation:

>**Invoke-Mimikatz -command '"lsadump::dcsync /domain:<Target Domain> /user:<krbtgt>\<Any Domain User>"**: Attackers attempt malicious replication using this command.

>**msfvenom -p windows/shell_reverse_tcp lhost=<Target IP Address> lport=444 -f exe > /home/attacker/Windows.exe**: Attackers run this command to generate a payload using msfvenom.

>**python -m fuzzowski printer1 631 -f ipp -r get_printer_attribs --restart smartplug**: The fuzzing of ICS protocols such as Modbus, BACnet, and Internet Printing Protocol (IPP) is critical for gathering information and identifying critical network activities. Fuzzowski is a network protocol fuzzer that helps attackers perform fuzz tests on ICS protocols. It assists attackers throughout the process of fuzzing a network protocol, as well as configuring communications.

>**run post/windows/gather/arp_scanner RHOSTS <target subnet range>**: Attackers uses this command to detect live hosts in the target network.

### Which of the following tools helps security professionals perform an automated security assessment of software to identify configuration and application vulnerabilities?


- Azure IoT Central
- Gqrx 
- LOIC
- **IoTVAS**

Explanation:

>**Gqrx**: Attackers use Gqrx to observe the frequency bands of temperature/humidity sensors, light switches, car keys, M-bus transmitters, etc. Gqrx can also enable an ttacker to listen to or eavesdrop on radio FM frequencies or any radio conversations.

>**Azure IoT Central**: Azure IoT Central is a hosted, extensible software-as-a-service (SaaS) platform that simplifies the setup of IoT solutions.

>**Low Orbit Ion Cannon (LOIC)**: LOIC is a network stress testing and DoS attack application. LOIC attacks can be called application-based DOS attacks because they primarily target web applications.

>**IoTVAS**: IoTVAS enables device vendors and security professionals to perform an automated security assessment of the software that powers IoT devices (firmware) to identify configuration and application vulnerabilities. This tool notifies users about the vulnerabilities discovered and assists in mitigating those in a timely manner.


### Which of the following Purdue levels is commonly referred to as an industrial demilitarized zone (IDMZ)?


- **Level 3.5**
- Level 2
- Level 4
- Level 3

Explanation:

>- Level 2: Manufacturing zone
>- Level 3: Manufacturing zone
>- Level 3.5: Industrial Demilitarized Zone (IDMZ)
>- Level 4: Enterprise zone

### Given below are the various steps involved in implementing a zero-trust model for an ICS network.
1. Monitoring and maintaining
2. Architecting the network
3. Mapping the traffic
4. Defining the network
5. Developing a ZT policy 

### Identify the correct sequence of steps involved in implementing a zero-trust model.


- 2 -> 1 -> 3 -> 4 -> 5 
- 5 -> 2 -> 4 -> 1 -> 3
- 1 -> 4 -> 3 -> 2 -> 5 
- **4 -> 3 -> 2 -> 5 -> 1**

Explanation:

>Steps to Implement a Zero-Trust Model in an ICS Network
>- Step 1: Defining the Network
>- Step 2: Mapping the Traffic 
>- Step 3: Architecting the Network 
>- Step 4: Developing a ZT Policy
>- Step 5: Monitoring and Maintaining


### Which of the following is a not-for-profit international regulatory authority that aims to assure the effective and efficient reduction of risks to the reliability and security of electric grids?


- Censys
- CVE
- **NERC**
- CSA

Explanation:

>**NERC**: The North American Electric Reliability Corporation (NERC) is a not-for-profit international regulatory authority that aims to assure the effective and efficient reduction of risks to the reliability and security of the electric grid.

>**Common Vulnerabilities and Exposures (CVE)**: CVE® is a publicly available and free-to-use list or dictionary of standardized identifiers for common software vulnerabilities and exposures.

>**Cloud Security Alliance (CSA)**: The CSA is a nonprofit global organization that provides rising awareness and promotes best practices and security policies to help and secure the cloud environment.

>**Censys**: Censys monitors the infrastructure and discovers unknown assets anywhere on the Internet. It provides a full view of every server and device exposed to the Internet.
