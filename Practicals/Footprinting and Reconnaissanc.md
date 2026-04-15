# Footprinting and Reconnaissance
**Lab 1: Perform Footprinting Through Search Engines**

**Task 1: Gather Information using Advanced Google Hacking Techniques**

*   **cache**: This operator allows you to view cached version of the web page. \[cache:www.eccouncil.org\]- Query returns the cached version of the website www.eccouncil.org
*   **allinurl**: This operator restricts results to pages containing all the query terms specified in the URL. \[allinurl: EC-Council career\]-Query returns only pages containing the words "EC-Council" and "career" in the URL
*   **inurl**: This operator restricts the results to pages containing the word specified in the URL \[inurl: copy site:www.eccouncil.org\]-Query returns only pages in EC-Council site in which the URL has the word "copy"
*   **allintitle**: This operator restricts results to pages containing all the query terms specified in the title. \[allintitle: detect malware\]-Query returns only pages containing the words "detect" and "malware" in the title
*   **inanchor**: This operator restricts results to pages containing the query terms specified in the anchor text on links to the page. \[Anti-virus inanchor:Norton\]-Query returns only pages with anchor text on links to the pages containing the word "Norton" and the page containing the word "Anti-virus"
*   **allinanchor**: This operator restricts results to pages containing all query terms specified in the anchor text on links to the page. \[allinanchor: best cloud service provider\]-Query returns only pages in which the anchor text on links to the pages contain the words "best," "cloud," "service," and "provider"
*   **link**: This operator searches websites or pages that contain links to the specified website or page. \[link:www.eccouncil.org\]-Finds pages that point to EC-Council's home page
*   **related**: This operator displays websites that are similar or related to the URL specified. \[related:www.eccouncil.org\]-Query provides the Google search engine results page with websites similar to eccouncil.org
*   **info**: This operator finds information for the specified web page. \[info:eccouncil.org\]-Query provides information about the www.eccouncil.org home page
*   **location**: This operator finds information for a specific location. \[location: EC-Council\]-Query give you results based around the term EC-Council
*   **intitle:login site:eccouncil.org:** This Advanced Google Search operator can help attackers and pen testers to extract login pages of the target organization's website.
*   **EC-Council filetype:pdf ceh:** The file type pdf is searched for the target organization EC-Council.

**Task 2: Gather Information from Video Search Engines**

Tool Link: [https://mattw.io/youtube-metadata/](https://mattw.io/youtube-metadata/)

Tool Link: [https://www.freewareweb.com](https://www.freewareweb.com)

**Task 3: Gather Information from FTP Search Engines**

**NAPALM FTP indexer:** [https://www.searchftps.net/](https://www.searchftps.net/)

**FreewareWeb FTP File Search:** [https://www.freewareweb.com](https://www.freewareweb.com)

**Task 4: Gather Information from IoT Search Engines**

**Shodan:** [**https://www.shodan.io/**](https://www.shodan.io/)

**Censys:** [https://censys.io](https://censys.io)

**Lab 2: Perform Footprinting Through Web Services**

**Task 1: Find the Company's Domains and Sub-domains using Netcraft**

**Sublist3r** (https://github.com)

**Pentest-Tools Find Subdomains** (https://pentest-tools.com)

**Task 2: Gather Personal Information using PeekYou Online People Search Service**

**PeekYou:** [https://www.peekyou.com](https://www.peekyou.com)

**Spokeo:** [https://www.spokeo.com](https://www.spokeo.com)

**pipl:** [https://pipl.com](https://pipl.com)

**Intelius:** [https://www.intelius.com](https://www.intelius.com)

**BeenVerified:** [https://www.beenverified.com](https://www.beenverified.com)

**Lab 3: Perform Footprinting Through Social Networking Sites**

**Task 1: Gather Employees' Information from LinkedIn using theHarvester**

**Task 2: Gather Personal Information from Various Social Networking Sites using Sherlock**

**Social Searcher** (https://www.social-searcher.com)

**UserRecon** (https://github.com)

**Lab 4: Perform Website Footprinting**

**Task 1: Gather Information About a Target Website using Ping Command Line Utility**

Ping is a network administration utility used to test the reachability of a host on an IP network and measure the round-trip time for messages sent from the originating host to a destination computer. The ping command sends an ICMP echo request to the target host and waits for an ICMP response. During this request-response process, ping measures the time from transmission to reception, known as round-trip time, and records any loss of packets. The ping command assists in obtaining domain information and the IP address of the target website.

Gathering information about a target website using Ping command-line utility such as the IP address of the target website, hop count to the target, and value of maximum frame size allowed on the target network.

**Example:**

**Value of maximum frame size:** ping www.certifiedhacker.com -f -l 1500

**Hop Count:** ping www.certifiedhacker.com -i 3

**Task 2: Gather Information about a Target Website using Photon**

**Ex: python3 photon.py -u http://www.certifiedhacker.com** and press **Enter** to crawl the target website for internal, external and scripts URLs.

**Ex: python3 photon.py -u http://www.certifiedhacker.com -l 3 -t 200 --wayback**

We can perform various other functionalities such as the cloning of the target website, extracting secret keys and cookies, obtaining strings by specifying regex pattern, etc. Using this information, the attackers can perform various attacks on the target website such as brute-force attacks, denial-of-service attacks, injection attacks, phishing attacks and social engineering attacks.

**Task 3: Gather Information About a Target Website using Central Ops**

CentralOps (centralops.net) is a free online network scanner that investigates domains and IP addresses, DNS records, traceroute, nslookup, whois searches, etc.

**Other Tools:**

**Website Informer** (https://website.informer.com)

**Burp Suite** (https://portswigger.net)

**Zaproxy** (https://www.zaproxy.org)

**Task 4: Extract a Company's Data using Web Data Extractor**

Web data extraction is the process of extracting data from web pages available on the company's website. A company's data such as contact details (email, phone, and fax), URLs, meta tags (title, description, keyword) for website promotion, directories, web research, etc. are important sources of information for an ethical hacker. Web spiders (also known as a web crawler or web robot) such as Web Data Extractor perform automated searches on the target website and extract specified information from the target website.

**Web Data Extractor Pro**

**ParseHub** (https://www.parsehub.com)

**SpiderFoot** (https://www.spiderfoot.net)

**Task 5: Mirror a Target Website using HTTrack Web Site Copier**

**HTTrack Website Copier**

**Cyotek WebCopy** (https://www.cyotek.com)

**Task 6: Gather Information About a Target Website using GRecon**

**Task 7: Gather a Wordlist from the Target Website using CeWL**

The words available on the target website may reveal critical information that can assist in performing further exploitation. CeWL is a ruby app that is used to spider a given target URL to a specified depth, optionally following external links, and returns a list of unique words that can be used for cracking passwords.

**cewl -d 2 -m 5 https://www.certifiedhacker.com** and press **Enter**.

> **\-d** represents the depth to spider the website (here, **2**) and **\-m** represents minimum word length (here, **5**).

**Lab 5: Perform Email Footprinting**

**Task 1: Gather Information about a Target by Tracing Emails using eMailTrackerPro**  


**Lab 6: Perform Whois Footprinting**

**Task 1: Perform Whois Lookup using DomainTools**

Link: [http://whois.domaintools.com](http://whois.domaintools.com)

**Lab 7: Perform DNS Footprinting**

**Task 1: Gather DNS Information using nslookup Command Line Utility and Online Tool**

**Link:** [http://www.kloth.net/services/nslookup.php](http://www.kloth.net/services/nslookup.php)

**Task 2: Perform Reverse DNS Lookup using Reverse IP Domain Check and DNSRecon**

Tool Link: [**https://www.yougetsignal.com**](https://www.yougetsignal.com)

**Python Tool: dnsrecon**

**Task 3: Gather Information of Subdomain and DNS Records using SecurityTrails**

SecurityTrails is an advanced DNS enumeration tool that is capable of creating a DNS map of the target domain network. It can enumerate both current and historical DNS records such as A, AAAA, NS, MX, SOA, and TXT, which helps in building the DNS structure. It also enumerates all the existing subdomains of the target domain using brute-force techniques.

**Tool Link:** [**https://securitytrails.com/**](https://securitytrails.com/)

**DNSChecker** (https://dnschecker.org)

**DNSdumpster** (https://dnsdumpster.com)

**Lab 8: Perform Network Footprinting**

With the IP address, hostname, and domain obtained in the previous information gathering steps, as a professional ethical hacker, your next task is to perform network footprinting to gather the network-related information of a target organization such as network range, traceroute, TTL values, etc. This information will help you to create a map of the target network and perform a man-in-the-middle attack.

**Task 1: Locate the Network Range**

Here, we will locate the network range using the ARIN Whois database search tool.

**Task 2: Perform Network Tracerouting in Windows and Linux Machines**

**Windows:** tracrt

**Linux:** traceroute

**Other Traceroute tools :**

**VisualRoute:** [http://www.visualroute.com](http://www.visualroute.com)

**Traceroute NG:** [https://www.solarwinds.com](https://www.solarwinds.com)

**Lab 9: Perform Footprinting using Various Footprinting Tools**

**Task 1: Footprinting a Target using Recon-ng**

Recon-ng is a web reconnaissance framework with independent modules and database interaction that provides an environment in which open-source web-based reconnaissance can be conducted. Here, we will use Recon-ng to perform network reconnaissance, gather personnel information, and gather target information from social networking sites.

**Task 2: Footprinting a Target using Maltego**

**Task 3: Footprinting a Target using OSRFramework**

OSRFramework is a set of libraries that are used to perform Open Source Intelligence tasks. They include references to many different applications related to username checking, DNS lookups, information leaks research, deep web search, regular expressions extraction, and many others. It also provides a way of making these queries graphically as well as several interfaces to interact with such as OSRFConsole or a Web interface.

**Command:** domainfy -n eccouncil -t all

**\-n**: specifies a nickname or a list of nicknames to be checked. **\-t**: specifies a list of top-level domains where nickname will be searched. The tool will retrieve all the domains along with their IP addresses related to the target domain.

Use **searchfy** to check for the existence of a given user details on different social networking platforms such as Github, Instagram and Keyserverubuntu. Type **searchfy -q “target user name or profile name”**

Similarly, you can use following OSRFramework packages to gather more information about the target:

*   **usufy** - Gathers registered accounts with given usernames.
*   **mailfy** - Gathers information about email accounts
*   **phonefy** - Checks for the existence of a given series of phones
*   **entify** - Extracts entities using regular expressions from provided URLs

**Task 4: Footprinting a Target using BillCipher**

**Task 5: Footprinting a Target using OSINT Framework**

OSINT Framework is an open source intelligence gathering framework that helps security professionals for performing automated footprinting and reconnaissance, OSINT research, and intelligence gathering. It is focused on gathering information from free tools or resources. This framework includes a simple web interface that lists various OSINT tools arranged by category and is shown as an OSINT tree structure on the web interface.

The OSINT Framework includes the following indicators with the available tools:

*   (T) - Indicates a link to a tool that must be installed and run locally
*   (D) - Google Dork
*   (R) - Requires registration
*   (M) - Indicates a URL that contains the search term and the URL itself must be edited manually

Tool Link: [**https://osintframework.com/**](https://osintframework.com/)