Which of the following categories of mobile risk covers binary patching, local resource modification, method hooking, method swizzling, and dynamic memory modification?


Client code quality
Extraneous functionality
**Code tampering**
Reverse engineering

Explanation:
    • M8—Code Tampering: This category covers binary patching, local resource modification, method hooking, method swizzling, and dynamic memory modification. Once an application is delivered to a mobile device, its code and data resources are resident on the device. An attacker can directly modify the code, change the memory contents dynamically, change or replace the system APIs that the application uses, or modify the application’s data and resources.
    • M10—Extraneous Functionality: Often, developers include hidden backdoor functionality or other internal development security controls that are not intended to be released into a production environment. For example, a developer may accidentally include a password as a comment in a hybrid app. Another example involves the disabling of two-factor authentication during testing
    • M9—Reverse Engineering: This category includes the analysis of the final core binary to determine its source code, libraries, algorithms, and other assets. Software such as IDA, Hopper, otool, and other binary inspection tools give the attacker insights into the inner workings of the application. Thus, he/she may exploit other nascent vulnerabilities in the application and uncover information about backend servers, cryptographic constants and ciphers, and intellectual property
    • M7—Client Code Quality: This category covers “Security Decisions via Untrusted Inputs” and is one of the less frequently used categories. It is the catch-all for code-level implementation problems in the mobile client, which are distinct from server-side coding mistakes. It captures buffer overflows, format string vulnerabilities, and various other code-level mistakes where the solution is to rewrite some code that is running on the mobile device. Most exploitations that fall into this category result in foreign code execution or DoS on remote server endpoints (and not the mobile device itself).


If an attacker is able to access the email contact list, text messages, photos, etc. on your mobile device, then what type of attack did the attacker employ?


BlueSniff
Bluebugging
**Bluesnarfing**
Bluesmacking

Explanation:
    • Bluesnarfing is the theft of information from a wireless device through a Bluetooth connection, often between phones, desktops, laptops, PDAs, and others. This technique allows an attacker to access the victim’s contact list, emails, text messages, photos, videos, business data, and so on stored on the device.
    • Any device with its Bluetooth connection enabled and set to “discoverable” or “discovery” mode (allowing other Bluetooth devices within range to view the device) may be susceptible to bluesnarfing if the vendor’s software contains certain vulnerabilities. Bluesnarfing exploits others’ Bluetooth connections without their knowledge.

In which of the following attacks does an attacker bribe or socially engineer telecom providers to obtain ownership of a target user’s SIM?


**OTP hijacking** 
Camfecting attack
Clickjacking
Framing

Explanation:
    • OTP hijacking:The attacker succeeds in OTP hijacking by initially stealing the victim’s PII data by bribing or tricking mobile store sellers or exploiting the reuse of the number for different customers. Attackers perform social engineering on telecom providers to obtain ownership of the target user’s SIM by claiming that their device was lost.
    • Camfecting attack: A camfecting attack is a webcam capturing attack. In this attack, the attacker gains access to the camera of a target’s computer or mobile device. The attacker infects the target device with a remote access Trojan (RAT) and compromises it to access the victim’s camera and microphone.
    • Framing: Framing involves a web page integrated into another web page using the iFrame elements of HTML. An attacker exploits iFrame functionality used in the target website, embeds his/her malicious web page, and uses clickjacking to steal users’ sensitive information.
    • Clickjacking: Clickjacking, also known as a user interface redress attack, is a malicious technique used to trick web users into clicking something different from what they think they are clicking. Consequently, attackers obtain sensitive information or take control of the device.

Which of the following practices is NOT a countermeasure to protect an Android device and the data stored in it from malicious users?


Customize the lock screen with user information
Keep the device updated with Google Android antivirus software
Enable GPS on the Android device to track it when lost or stolen
**Disable two-step verification on the Android mobile device**

Explanation:
Given below are some countermeasures that can help you to protect your Android device and the data stored on it from malicious users:
    • Enable screen lock for your Android phone
    • Never root your Android device
    • Download apps only from official Android markets
    • Keep your device updated with Google Android anti-virus software
    • Do not directly download APKs
    • Update the OS regularly
    • Use free protector Android apps such as Android Protector, where you can assign passwords to text messages, mail accounts, and so on
    • Customize your locked home screen with the user information
    • Enable encryption in your Android device to enhance its security
    • Lock your apps that hold private information to prevent others from viewing it, using apps such as AppLock
    • Enable GPS on your Android device for it to be tracked when lost or stolen
    • Enable two-step verification on your Android mobile device


Which of the following native libraries in the Android OS architecture is meant for Internet security?


SQLite
Open GL | ES
**SSL**
WebKit and Blink

Explanation:
The native libraries are as follows:
    • SQLite—database engine used for data storage purposes
    • SSL—meant for Internet security
    • Open GL | ES—2D and 3D graphics library
    • WebKit and Blink—web browser engine to display HTML content


Which of the following practices is NOT a countermeasure to protect an Android device and the data stored on it from malicious users?


**Enable features such as SmartLock instead of passwords**
Enable the screen pinning option to securely access Android apps
Download apps only from official Android markets 
Never root the Android device 

Explanation:
Given below are some countermeasures that can help you to protect your Android device and the data stored on it from malicious users
    • Never root your Android device
    • Download apps only from official Android markets
    • Uninstall apps that invade your privacy
    • Encrypt all the Internet traffic through VPN services such as ExpressVPN and VyprVPN for Android.
    • Block all the ads displayed by apps
    • Enable two-step verification on your Android mobile device
    • Disable features such as SmartLock instead of passwords, and auto sign-in functionality.
    • Install password manager apps such as LastPass to manage passwords securely
    • Enable the screen pinning option to securely access Android apps

Which of the following applications allows attackers to identify the target devices and block the access of Wi-Fi to the victim devices in a network?


DroidSheep
Network Spoofer
KingoRoot
**NetCut**

Explanation:
    • NetCut is an is a Wi-Fi killing mobile application that quickly detects all network users in the WIFI and allows the attacker to kill Wi-Fi access to any specific user in a network. Attackers use this tool to identify target devices and block the access of Wi-Fi to the victim devices in a network.

Which of the following Jailbreaking techniques will make the mobile device jailbroken after each reboot?


Semi-Tethered Jailbreaking
Tethered Jailbreaking
**Untethered Jailbreaking**
None of the Above

Explanation:
    • An untethered jailbreak has the property that if the user turns the device off and back on, the device will start up completely, and the kernel will be patched without the help of a computer – in other words, it will be jailbroken after each reboot.


By performing which of the following Jailbreaking techniques does a mobile device start up completely, and it will no longer have a patched kernel after a user turns the device off and back on?


Untethered Jailbreaking
Tethered Jailbreaking
**Semi-Tethered Jailbreaking**
None of the Above

Explanation:
    • A semi-tethered jailbreaking has the property that if the user turns the device off and back on, the device will start up completely; it will no longer have a patched kernel, but it will still be usable for normal functions. To use jailbroken addons, the user needs to start the device with the help of the jailbreaking tool.  


