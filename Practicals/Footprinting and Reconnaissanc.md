# Footprinting and Reconnaissance

## Lab 1: Perform Footprinting Through Search Engines

### Task 1: Gather Information using Advanced Google Hacking Techniques

- `cache`: view cached version of a web page. Example: `cache:www.eccouncil.org`
- `allinurl`: restrict results to pages containing all query terms in the URL. Example: `allinurl: EC-Council career`
- `inurl`: restrict results to pages containing the word specified in the URL. Example: `inurl: copy site:www.eccouncil.org`
- `allintitle`: restrict results to pages containing all query terms in the title. Example: `allintitle: detect malware`
- `inanchor`: restrict results to pages containing the query terms in anchor text. Example: `Anti-virus inanchor:Norton`
- `allinanchor`: restrict results to pages containing all query terms in anchor text. Example: `allinanchor: best cloud service provider`
- `link`: search for websites or pages that contain links to the specified website or page. Example: `link:www.eccouncil.org`
- `related`: display websites that are similar or related to the specified URL. Example: `related:www.eccouncil.org`
- `info`: find information for the specified web page. Example: `info:eccouncil.org`
- `location`: find information for a specific location. Example: `location: EC-Council`
- `intitle:login site:eccouncil.org`: extract login pages of the target organization's website.
- `EC-Council filetype:pdf ceh`: search PDF files related to the target organization.

### Task 2: Gather Information from Video Search Engines

- [https://mattw.io/youtube-metadata/](https://mattw.io/youtube-metadata/)
- [https://www.freewareweb.com](https://www.freewareweb.com)

### Task 3: Gather Information from FTP Search Engines

- NAPALM FTP indexer: [https://www.searchftps.net/](https://www.searchftps.net/)
- FreewareWeb FTP File Search: [https://www.freewareweb.com](https://www.freewareweb.com)

### Task 4: Gather Information from IoT Search Engines

- [https://www.shodan.io/](https://www.shodan.io/)
- [https://censys.io](https://censys.io)

## Lab 2: Perform Footprinting Through Web Services

### Task 1: Find the Company's Domains and Sub-domains using Netcraft

- Sublist3r: https://github.com
- Pentest-Tools Find Subdomains: https://pentest-tools.com

### Task 2: Gather Personal Information using PeekYou Online People Search Service

- [https://www.peekyou.com](https://www.peekyou.com)
- [https://www.spokeo.com](https://www.spokeo.com)
- [https://pipl.com](https://pipl.com)
- [https://www.intelius.com](https://www.intelius.com)
- [https://www.beenverified.com](https://www.beenverified.com)

## Lab 3: Perform Footprinting Through Social Networking Sites

### Task 1: Gather Employees' Information from LinkedIn using theHarvester

### Task 2: Gather Personal Information from Various Social Networking Sites using Sherlock

- [https://www.social-searcher.com](https://www.social-searcher.com)
- https://github.com

## Lab 4: Perform Website Footprinting

### Task 1: Gather Information About a Target Website using Ping Command Line Utility

Ping tests reachability, round-trip time, and packet loss. It can obtain domain information and the target website IP address.

- Example: `ping www.certifiedhacker.com -f -l 1500`
- Example: `ping www.certifiedhacker.com -i 3`

### Task 2: Gather Information about a Target Website using Photon

- Example: `python3 photon.py -u http://www.certifiedhacker.com`
- Example: `python3 photon.py -u http://www.certifiedhacker.com -l 3 -t 200 --wayback`

### Task 3: Gather Information About a Target Website using Central Ops

CentralOps is a free online network scanner that investigates domains and IP addresses, DNS records, traceroute, nslookup, and whois searches.

### Other Tools

- [https://website.informer.com](https://website.informer.com)
- [https://portswigger.net](https://portswigger.net)
- [https://www.zaproxy.org](https://www.zaproxy.org)

### Task 4: Extract a Company's Data using Web Data Extractor

Web data extraction extracts data from web pages such as contact details, URLs, meta tags, and directories.

- [https://www.parsehub.com](https://www.parsehub.com)
- [https://www.spiderfoot.net](https://www.spiderfoot.net)

### Task 5: Mirror a Target Website using HTTrack Web Site Copier

- HTTrack Website Copier
- [https://www.cyotek.com](https://www.cyotek.com)

### Task 6: Gather Information About a Target Website using GRecon

### Task 7: Gather a Wordlist from the Target Website using CeWL

CeWL spiders a target site to generate a list of unique words for password cracking.

- Example: `cewl -d 2 -m 5 https://www.certifiedhacker.com`
- `-d` specifies the depth to spider the website.
- `-m` specifies minimum word length.

## Lab 5: Perform Email Footprinting

### Task 1: Gather Information about a Target by Tracing Emails using eMailTrackerPro

## Lab 6: Perform Whois Footprinting

### Task 1: Perform Whois Lookup using DomainTools

- [http://whois.domaintools.com](http://whois.domaintools.com)

## Lab 7: Perform DNS Footprinting

### Task 1: Gather DNS Information using nslookup Command Line Utility and Online Tool

- [http://www.kloth.net/services/nslookup.php](http://www.kloth.net/services/nslookup.php)

### Task 2: Perform Reverse DNS Lookup using Reverse IP Domain Check and DNSRecon

- [https://www.yougetsignal.com](https://www.yougetsignal.com)
- `dnsrecon`

### Task 3: Gather Information of Subdomain and DNS Records using SecurityTrails

SecurityTrails is an advanced DNS enumeration tool that can enumerate current and historical DNS records and subdomains.

- [https://securitytrails.com/](https://securitytrails.com/)
- [https://dnschecker.org](https://dnschecker.org)
- [https://dnsdumpster.com](https://dnsdumpster.com)

## Lab 8: Perform Network Footprinting

Network footprinting gathers network-related information such as network range, traceroute, and TTL values.

### Task 1: Locate the Network Range

Use the ARIN Whois database search tool.

### Task 2: Perform Network Tracerouting in Windows and Linux Machines

- Windows: `tracrt`
- Linux: `traceroute`

Other traceroute tools:

- [http://www.visualroute.com](http://www.visualroute.com)
- [https://www.solarwinds.com](https://www.solarwinds.com)

## Lab 9: Perform Footprinting using Various Footprinting Tools

### Task 1: Footprinting a Target using Recon-ng

Recon-ng is a web reconnaissance framework with modules and database interaction for open-source reconnaissance.

### Task 2: Footprinting a Target using Maltego

### Task 3: Footprinting a Target using OSRFramework

- `domainfy -n eccouncil -t all`
- Use `searchfy -q "target user name or profile name"`
- `usufy` gathers registered accounts with given usernames.
- `mailfy` gathers information about email accounts.
- `phonefy` checks for the existence of a phone series.
- `entify` extracts entities using regular expressions from URLs.

### Task 4: Footprinting a Target using BillCipher

### Task 5: Footprinting a Target using OSINT Framework

OSINT Framework lists OSINT tools by category and provides a web interface for intelligence gathering.

- [https://osintframework.com/](https://osintframework.com/)
