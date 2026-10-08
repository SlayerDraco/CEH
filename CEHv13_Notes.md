# CEHv13 Notes
# 1. CIA + AN
## Information Security Elements
### C → Confidentiality
Prevent unauthorized disclosure.
Examples:
* Encryption
* Access Control
### I → Integrity
Prevent unauthorized modification.
Examples:
* Hashing
* Checksums
### A → Availability
Ensure access when needed.
Examples:
* Backups
* Redundancy
### A → Authenticity
Verify source is genuine.
Examples:
* Certificates
* Biometrics
### N → Non-Repudiation
Prevent denial of actions.
Examples:
* Digital Signatures
### ⚠️ Confidentiality ≠ Authentication
* **Confidentiality** → *who is allowed to see* the data.
* **Authentication** → *whether the source/identity is genuine*.
Both can appear in the same question — decide which one is being asked.
## Security, Functionality & Ease-of-Use Triangle
The three pull against each other:
> As **security** increases, **functionality** and **ease of use** decrease.
More controls = less convenience. Expect scenario questions on this trade-off.
---
# 2. Attack Classifications
### Attacks vs Security Properties
|Attack|Property Affected|
|---|---|
|Interception|Confidentiality|
|Modification|Integrity|
|Interruption|Availability|
|Fabrication|Authenticity|
### CEH Attack Categories (by vector)
|Category|Meaning|
|---|---|
|Passive|Monitor traffic, no modification (sniffing)|
|Active|Alter data or system (MITM, DoS, SQLi)|
|Close-in|Attacker physically near target (shoulder surfing, dumpster diving)|
|Insider|Trusted person misuses access|
|Distribution|Tampering with hardware/software before delivery (supply chain)|
### Attack Terminology
|Term|Meaning|
|---|---|
|Inside Attack|Originates from **inside** the security boundary|
|Outside Attack|Originates from **outside** the network|
|Daisy Chaining|Use one compromised system to reach the next|
|Shrink-Wrap Attack|Exploit default code/config in off-the-shelf software|
|Phreaker|Attacker targeting telephone/telecom systems|
|Bot / Zombie|Compromised machine under remote control|
---
# 3. Active vs Passive Attacks
### Passive
Observe only.
Examples:
* Sniffing
* Eavesdropping
### Active
Modify or disrupt.
Examples:
* DDoS
* Malware
* Spoofing
---
# 4. Information Warfare
|Warfare|Goal|
|---|---|
|Command & Control|Disrupt leadership|
|Intelligence|Gather information|
|Electronic|Jam signals|
|Psychological|Influence minds|
|Hacker|Attack systems|
|Economic|Financial damage|
|Cyber|Nation-state attacks|
---
# 5. Hacker Types
|Type|Motivation|
|---|---|
|White Hat|Security|
|Black Hat|Crime|
|Gray Hat|Curiosity|
|Script Kiddie|Uses Tools|
|Hacktivist|Ideology|
|State-Sponsored|Espionage|
|Cyber Terrorist|Fear|
|Suicide Hacker|Destruction|
---
# 6. CEH Hacking Phases
1. Reconnaissance
1. Scanning & Enumeration
1. Gaining Access
1. Maintaining Access
1. Covering Tracks
### "Really Smart Guys Make Cash"
## Testing Knowledge Levels (Box Types)
|Type|Knowledge|Models|
|---|---|---|
|Black Box|No prior knowledge|External attacker|
|White Box|Full knowledge|Internal / knowledgeable threat|
|Gray Box|Partial knowledge|Trusted user / partially informed|
#### ⚠️ Box type ≠ hat colour. A **white-hat** ethical hacker can perform a **black-box** test.
## Rules of Engagement (RoE) / Authorization
What makes hacking *ethical* is **explicit written permission** + defined limits:
* Signed authorization / scope agreement
* NDA
* Allowed targets & boundaries
* Timing window
* Agreed test type
Same technical action = legal with authorization, illegal without it.
---
# 7. Cyber Kill Chain
1. Reconnaissance
1. Weaponization
1. Delivery
1. Exploitation
1. Installation
1. Command & Control
1. Actions on Objectives
### "Really Weird Dogs Eat Ice Cream Always"
## Memory Map
Weaponization
→ Create malware
Delivery
→ Send malware
Exploitation
→ Trigger vulnerability
Installation
→ Install malware
C2
→ Control victim
Actions
→ Steal data
---
# 8. MITRE ATT&CK, Diamond Model & Security Controls
## MITRE ATT&CK
**A**dversarial **T**actics, **T**echniques and **C**ommon **K**nowledge.
A knowledge base of real-world attacker behavior, organized as:
* **Tactics** → The attacker's goal (the "why"). Enterprise matrix has **14 tactics**: Reconnaissance, Resource Development, Initial Access, Execution, Persistence, Privilege Escalation, Defense Evasion, Credential Access, Discovery, Lateral Movement, Collection, Command & Control, Exfiltration, Impact.
* **Techniques** → How the goal is achieved (the "how").
* **Procedures** → Specific implementation by an adversary.
Together these are called **TTPs** (Tactics, Techniques, and Procedures).
## Diamond Model of Intrusion Analysis
Four core linked features of any intrusion:
* **Adversary** → Who is attacking
* **Capability** → Tools / malware used
* **Infrastructure** → C2, domains, IPs
* **Victim** → Target
## Security Control Types (by function)
|Control Example|Type|
|---|---|
|Firewall|Preventive|
|IDS|Detective|
|IPS|Preventive|
|Patch|Corrective|
|Backup|Recovery|
|Warning Banner|Deterrent|
|Hot/Cold Site|Compensating|
### Control Categories (by nature)
* **Physical** → Locks, guards, CCTV
* **Technical / Logical** → Firewall, encryption, IDS
* **Administrative** → Policies, training, procedures
---
# 9. Risk Management
|Term|Meaning|
|---|---|
|Asset|Valuable Resource|
|Threat|Danger|
|Vulnerability|Weakness|
|Exploit|Attack Method|
|Risk|Potential Loss|
---
# 10. STRIDE Threat Model
|Letter|Meaning|
|---|---|
|S|Spoofing|
|T|Tampering|
|R|Repudiation|
|I|Information Disclosure|
|D|Denial of Service|
|E|Elevation of Privilege|
---
# 11. Incident Response Lifecycle
1. Preparation
1. Detection & Analysis
1. Containment
1. Eradication
1. Recovery
1. Lessons Learned
### "Please Don't Contain Evil Ransomware Lazily"
---
# 12. CTI (Cyber Threat Intelligence)
|Type|Audience|
|---|---|
|Strategic|Executives|
|Operational|Managers|
|Tactical|Defenders|
|Technical|Analysts|
---
# 13. Laws & Standards
|Framework|Purpose|
|---|---|
|GDPR|Privacy|
|HIPAA|Healthcare|
|SOX|Financial Reporting|
|PCI DSS|Payment Cards|
|ISO 27001|ISMS|
|NIST|Cybersecurity Framework|
---
# 14. Governance Documents
|Document|Meaning|
|---|---|
|Policy|What|
|Standard|Mandatory Rule|
|Procedure|How|
|Guideline|Recommendation|
---
---
# 15. Footprinting & Reconnaissance
### Definition
The process of gathering information about a target before launching an attack.
### Goals
* Reduce uncertainty
* Identify attack surface
* Gather public and technical information
### Types
**Passive Footprinting**
* No direct interaction
* Hard to detect
**Active Footprinting**
* Direct interaction
* Can be detected
---
# 16. OSINT (Open-Source Intelligence)
## Definition
Information collected from **publicly available sources**.
### Common Sources
* Google
* LinkedIn
* GitHub
* WHOIS
* Shodan
---
# 17. Information Categories (OENSF)
|Category|Information|
|---|---|
|Organization|Company Structure|
|Employees|Names, Emails|
|Network|IPs, Domains|
|Security|Firewalls, IDS|
|Financial|Revenue, Investors|
---
# 18. Google Dorking
## Definition
Using advanced Google search operators to discover exposed information.
### Important Operators
|Operator|Purpose|
|---|---|
|site:|Search one domain|
|filetype:|Search specific files|
|intitle:|Search page titles|
|inurl:|Search URLs|
|intext:|Search page contents|
#### Google Hacking Database (GHDB) is a Collection of known Google Dorks.
### Search-Engine Footprinting Beyond Google
Footprinting uses many sources, not just Google:
* Other engines (Bing, DuckDuckGo), cached/indexed pages
* Job portals (reveal tech stack), social platforms
* Public documents & metadata, people-search and public databases
* **Shodan / Censys** → Internet-connected devices
---
# 19. WHOIS Footprinting
## Definition
Protocol/database used to obtain **domain registration information**.
### Important Information
* Registrant (Owner)
* Registrar (Seller)
* Creation Date
* Expiration Date
* Name Servers
* Contact Details
### WHOIS Privacy
Hides ownership details. It does **NOT** hide the domain itself.
---
# 20. DNS Footprinting
## DNS Records
|Record|Purpose|
|---|---|
|A|Hostname → IPv4|
|AAAA|Hostname → IPv6|
|MX|Mail Server|
|NS|Name Server|
|CNAME|Alias|
|PTR|IP → Hostname|
|TXT|Text Information|
|SOA|Start of Authority|
#### "**An** **A**ngry **M**ailman **N**amed **C**arl **P**refers **T**extbooks **S**ometimes”
## DNS Lookup Tools
|Tool|Use|
|---|---|
|`nslookup`|Query records; has **interactive mode** (`set type=MX`)|
|`dig`|Linux query tool; `dig MX example.com`, `dig axfr`|
|`host`|Quick record lookup|
Know you can query a **specific record type** and read the output.
## DNS Zone Transfer (AXFR)
Copies the **entire DNS zone** (all hosts + records) — a big info leak if allowed to anyone.
* Test: `dig axfr @nameserver domain` / `nslookup` → `ls -d`
* **Countermeasure:** restrict AXFR to authorized secondary servers only.
---
# 21. Network Footprinting
## Main Techniques
* Ping
* Ping Sweep
* Traceroute
* ARP
* Route Mapping
### ICMP
Used for:
* Echo Request
* Echo Reply
* Destination Unreachable
* Time Exceeded
### ARP
IP → MAC
### RARP
MAC → IP
### Traceroute
Uses TTL and ICMP Time Exceeded.
* **Windows:** `tracert` (uses ICMP by default)
* **Linux/Unix:** `traceroute` (uses UDP by default; `-I` for ICMP)
* Output/behavior differs because the probe protocol differs.
### ICMP Firewall Clue — Type 3, Code 13
**ICMP Type 3 = Destination Unreachable.**
**Code 13 = Communication Administratively Prohibited** → a **firewall/ACL is filtering** the traffic (not that the host is down). High-yield exam fact.
### War Dialing / Modem Discovery
Scanning phone lines for dial-in modems (recognition-level tools):
ToneLoc, THC-Scan, WarVox (VoIP), PAWS, TeleSweep.
---
# 22. Email Foot printing
## Email Protocols
|Protocol|Purpose|Port|
|---|---|---|
|SMTP|Send Mail|25, 465, 587|
|POP3|Download Mail|110, 995|
|IMAP|Synchronize Mail|143, 993|
### Email Security
|Technology|Purpose|
|---|---|
|SPF|Authorized Senders|
|DKIM|Integrity + Authenticity|
|DMARC|Authentication Policy|
### Email Headers as a Recon Source
Full headers reveal more than the visible From/To:
* Originating IP & mail-server hops (`Received:`)
* Mail software/infrastructure
* Timestamps & routing path
Useful for mapping infrastructure and spotting spoofing.
---
# 23. Website Foot printing
### Important Files
|File|Purpose|
|---|---|
|robots.txt|Search Engine Instructions|
|sitemap.xml|Website Map|
### Important Techniques
* Banner Grabbing
* Web Fingerprinting
* CMS Detection
* Directory Enumeration
* Website Mirroring
* Web Crawling
---
# 24. Social Engineering Foot printing
### Main Sources
* LinkedIn
* Facebook
* GitHub
* Job Portals
* PDFs
* Office Documents
### Metadata
Hidden information inside files.
Examples:
* Author
* Username
---
# 25. Countermeasures Against Footprinting
|Threat|Countermeasure|
|---|---|
|WHOIS Exposure|WHOIS Privacy|
|DNS Leakage|Restrict AXFR|
|Email Spoofing|SPF + DKIM + DMARC|
|Metadata Leakage|Metadata Sanitization|
|Social Media Leakage|Social Media Policy|
|Banner Disclosure|Banner Hiding|
|Search Engine Exposure|Access Controls|
|Human Leakage|Security Awareness|
---
# 26. Top 30 Ports for CEH v13
|Port|Protocol|Service|Purpose|
|---|---|---|---|
|20|TCP|FTP Data|Transfers FTP data|
|21|TCP|FTP Control|File transfer commands and authentication|
|22|TCP|SSH|Secure remote login and administration|
|23|TCP|Telnet|Unencrypted remote login|
|25|TCP|SMTP|Sending email|
|53|TCP/UDP|DNS|Domain name resolution|
|69|UDP|TFTP|Simple file transfer (no authentication)|
|67/68|UDP|DHCP|Server (67) / Client (68) IP assignment|
|80|TCP|HTTP|Unencrypted web traffic|
|88|TCP/UDP|Kerberos|AD authentication (ticket-based)|
|110|TCP|POP3|Download emails|
|111|TCP/UDP|RPCbind (Portmapper)|Maps RPC services|
|123|UDP|NTP|Time synchronization|
|135|TCP|MSRPC / EPMAP|Microsoft RPC endpoint mapper|
|137|UDP|NetBIOS Name Service|Name resolution|
|138|UDP|NetBIOS Datagram|Connectionless NetBIOS|
|139|TCP|NetBIOS Session|SMB over NetBIOS|
|143|TCP|IMAP|Synchronize emails|
|161/162|UDP|SNMP|Queries (161) / Traps (162)|
|389|TCP/UDP|LDAP|Directory services (e.g., Active Directory)|
|443|TCP|HTTPS|Encrypted web traffic|
|445|TCP|SMB|Windows file and printer sharing|
|500|UDP|IKE / IPsec|VPN key exchange|
|514|UDP|Syslog|Centralized logging|
|636|TCP|LDAPS|LDAP over SSL/TLS|
|993|TCP|IMAPS|Secure IMAP|
|995|TCP|POP3S|Secure POP3|
|1433|TCP|Microsoft SQL Server|SQL database service|
|1521|TCP|Oracle Database|Oracle DB listener|
|2049|TCP/UDP|NFS|Linux/Unix file sharing|
|3268|TCP|Global Catalog (LDAP)|AD forest-wide search|
|3306|TCP|MySQL|MySQL database|
|3389|TCP|RDP|Windows Remote Desktop|
|5432|TCP|PostgreSQL|PostgreSQL Database|
|5900|TCP|VNC|Remote desktop/screen sharing|
---
---
# 27. Host Discovery
## Definition
The process of identifying **live hosts** before performing port scanning.
### Techniques
|Technique|Purpose|
|---|---|
|ICMP Ping|Discover live hosts|
|ARP Scan|Discover hosts on LAN|
|TCP SYN Ping|Discover hosts when ICMP is blocked|
|TCP ACK Ping|Test firewall filtering|
|UDP Ping|Discover UDP hosts|
### Important Nmap Flags
|Flag|Purpose|
|---|---|
|`-sn`|Host Discovery Only|
|`-PE`|ICMP Echo|
|`-PR`|ARP Scan|
|`-PS`|SYN Ping|
|`-PA`|ACK Ping|
|`-PU`|UDP Ping|
### Important Facts
* ICMP uses Echo Request/Echo Reply.
* ARP works **only on Local Networks (LAN)**.
* ARP is more reliable than ICMP inside LAN.
* ICMP may be blocked by firewalls.
## Nmap Options Cheat-Sheet (High-Yield)
|Option|Purpose|
|---|---|
|`-sn`|Host discovery only (no port scan)|
|`-Pn`|Skip host discovery; treat all as online (bypass ICMP block)|
|`-sT`|TCP connect scan|
|`-sS`|SYN / half-open scan|
|`-sU`|UDP scan|
|`-sA`|ACK scan (firewall filtering map)|
|`-sF` / `-sN` / `-sX`|FIN / NULL / XMAS|
|`-sV`|Service/version detection|
|`-O`|OS detection|
|`-A`|Aggressive (OS + version + scripts + traceroute)|
|`-p` / `-p-`|Specific ports / all 65535 TCP ports|
|`-T0`–`-T5`|Timing (0 = slowest/stealthy, 5 = fastest)|
|`-D`|Decoy scan|
|`-f`|Fragment packets|
|`-oN/-oX/-oG`|Output normal / XML / grepable|
---
# 28. Port Scanning Fundamentals
## Definition
Process of identifying **open services** running on a host.
### Port States
|State|Meaning|
|---|---|
|Open|Service Running|
|Closed|Host Alive, No Service|
|Filtered|Firewall Blocking|
### TCP 3-Way Handshake
SYN ——————————> SYN/ACK ——————————> ACK
### TCP Flags (know these for scan questions)
|Flag|Meaning|
|---|---|
|SYN|Start/synchronize a connection|
|ACK|Acknowledge received data|
|SYN/ACK|Server agrees + proposes sequence number|
|RST|Reset / refuse connection|
|FIN|Graceful termination|
|PSH|Push buffered data to the application now|
|URG|Urgent data present (urgent pointer)|
Mnemonic for the 6 control flags: **"Unskilled Attackers Pester Real Security Folks"** (URG, ACK, PSH, RST, SYN, FIN).
---
# 29. TCP Connect Scan (-sT)
## Definition
Performs a **complete TCP 3-Way Handshake**.
### Characteristics
* Full Connection
* Reliable
* Easy to Detect
* No Root/Admin Required
### Responses
|Response|Meaning|
|---|---|
|SYN/ACK|Open|
|RST|Closed|
---
# 30. SYN Scan (-sS)
## Definition
Performs a **Half-Open Scan**.
### Process
SYN ——————————> SYN/ACK ——————————> RST
### Characteristics
* Stealth Scan
* Faster
* Less Logging
* Requires Root/Admin
### Responses
|Response|Meaning|
|---|---|
|SYN/ACK|Open|
|RST|Closed|
|No Response / ICMP Unreachable|Filtered|
---
# 31. FIN, NULL & XMAS Scans
These are **stealth scans** that send packets a normal handshake never would, so no full connection is logged.
### FIN Scan (-sF)
Sends only the FIN flag. Normally used to terminate a session.
### NULL Scan (-sN)
NULL means: **No TCP flags set**.
### XMAS Scan (-sX)
FIN + PSH + URG flags (packet "lit up like a Christmas tree").
### Response Rule
|Response|Meaning|
|---|---|
|No Response|Open \| Filtered|
|RST|Closed|
|ICMP Unreachable (type 3)|Filtered|
#### ⚠️ Important Exception
These scans rely on **RFC 793** behavior and only work reliably on **Linux/UNIX** systems.
**Windows** (and many devices) reply with **RST for both open and closed ports**, so every port falsely appears "Closed." Firewalls that block these flags are also bypassed because the packets look incomplete.
---
# 32. ACK Scan (-sA)
## Definition
Determines **firewall filtering**, not open ports.
### Results
|Response|Meaning|
|---|---|
|RST|Unfiltered|
|No Response|Filtered|
### Uses
* Firewall Mapping
* Stateful Firewall Detection
### Stateful vs Stateless
|Stateful|Stateless|
|---|---|
|Tracks Connections|No Connection Memory|
---
# 33. UDP Scan (-sU)
## Definition
Scans UDP services.
### Responses
|Response|Meaning|
|---|---|
|ICMP Port Unreachable|Closed|
|UDP Response|Open|
|No Response|Open or Filtered|
### Characteristics
* No Handshake
* Slower
* Less Reliable
---
# 34. Service Version Detection & Banner Grabbing
## Banner Grabbing
Obtains:
* Service Name
* Software Version
* Server Information
### Types
|Type|Description|
|---|---|
|Active|Direct Connection|
|Passive|No Direct Contact|
---
# 35. Operating System Detection
## Purpose
Identify target operating system.
### TCP/IP Stack Fingerprinting
Uses:
* TCP Behavior
* ICMP Responses
* Window Size
* TTL
### Default TTL Values
|OS|TTL|
|---|---|
|Linux/Unix|64|
|Windows|128|
|Cisco/Network gear|255|
#### ⚠️ TTL is a **clue, not proof**
Default TTL values are *starting points*. Routing hops decrement TTL, and config/device type can change it, so OS detection combines TTL **with** window size, TCP flag behavior, and ICMP responses — never TTL alone.
---
# 36. Nmap Scripting Engine (NSE)
## Definition
Nmap feature that automates scanning using scripts.
### Categories
|Category|Purpose|
|---|---|
|safe|Information Gathering|
|default|Default Scripts|
|discovery|Enumeration|
|version|Version Detection|
|vuln|Vulnerability Detection|
|auth|Authentication|
|brute|Password Guessing|
|malware|Malware Detection|
|exploit|Limited Exploitation|
---
# 37. Firewall, IDS/IPS Evasion
## Important Techniques
|Technique|Purpose|
|---|---|
|Decoy Scan|Hide Real IP|
|Fragmentation|Split Packets|
|Source Port Spoofing|Use Trusted Source Port|
|MAC Spoofing|Hide Device Identity|
|Timing Templates|Reduce Detection|
### Nmap Options
|Option|Purpose|
|---|---|
|`-D`|Decoy|
|`-f`|Fragment|
|`--source-port`|Source Port Spoof|
|`--spoof-mac`|MAC Spoof|
|`-T0` to `-T5`|Timing|
### ⚠️ IP Spoofing Has a Big Limitation
If you spoof the **source IP**, replies go to the **spoofed address, not to you**. So spoofing hides identity but breaks normal two-way interaction — it is **not** invisibility in a real session. (It's useful for decoys, reflection, blind attacks.)
---
# 38. Scanning Countermeasures
## Defensive Controls
|Threat|Countermeasure|
|---|---|
|Port Scanning|Firewall|
|Reconnaissance|IDS|
|Active Attack|IPS|
|Service Discovery|Port Knocking|
|Attackers|Honeypot|
|Lateral Movement|Network Segmentation|
|Known Vulnerabilities|Patch Management|
|Banner Disclosure|Banner Hiding|
|Fast Scanning|Rate Limiting|
|Suspicious Activity|Logging & Monitoring|
### ⚠️ Legal Note
Port scanning can be detected and, depending on jurisdiction/impact, is a legal gray area. CEH rule: **only scan systems you are authorized to scan.**
---
---
# 39. Enumeration
## Definition
Active process of extracting detailed information from a target after discovering hosts and open ports.
### Objectives
* Usernames
* Groups
* Shared Resources
* Password Policies
* Domain Information
* Network Services
* Operating System Details
* Active Directory Information
### Important Protocols
|Protocol|Port|
|---|---|
|NetBIOS|137–139|
|SMB|445|
|SNMP|161|
|LDAP|389|
|DNS|53|
|SMTP|25|
|RPC|111 / 135|
|NFS|2049|
---
# 40. NetBIOS Enumeration
## Purpose
Enumerate Windows network information.
### Ports
|Port|Service|
|---|---|
|137|Name Service|
|138|Datagram Service|
|139|Session Service|
### Important Tools
|Tool|Purpose|
|---|---|
|nbtstat|Windows Enumeration|
|nbtscan|Linux Enumeration|
|enum4linux|Advanced Enumeration|
|Nmap NSE|NetBIOS Information|
### Important NetBIOS Suffixes (Name Codes)
|Suffix|Meaning|
|---|---|
|<00>|Workstation Service|
|<03>|Messenger Service (logged-on user)|
|<20>|File Server Service|
|<1B>|Domain Master Browser|
|<1C>|Domain Controllers (group)|
|<1D>|Master Browser|
|<1E>|Browser Service Elections|
### `nbtstat` Operations
|Command|Purpose|
|---|---|
|`nbtstat -a <name>`|Remote machine's NetBIOS name table (by name)|
|`nbtstat -A <IP>`|Same, but by IP address|
|`nbtstat -c`|Local NetBIOS name cache|
|`nbtstat -n`|Local NetBIOS names|
|`nbtstat -r`|Names resolved via broadcast/WINS|
|`nbtstat -S`|Active NetBIOS sessions|
---
# 41. SMB Enumeration
## Purpose
Enumerate Windows file sharing and domain information.
### Ports
|Port|Service|
|---|---|
|139|SMB over NetBIOS|
|445|SMB over TCP/IP|
### Important Tools
|Tool|Purpose|
|---|---|
|enum4linux|Full Enumeration|
|smbclient|List/Browse Shares|
|rpcclient|RPC Enumeration|
|Nmap NSE|SMB Enumeration|
### Common Administrative Shares
|Share|Purpose|
|---|---|
|C$|System Drive|
|ADMIN$|Windows Directory|
|IPC$|Inter-Process Communication (null-session target)|
### `net view` Enumeration
|Command|Purpose|
|---|---|
|`net view \\<computer>`|List shared resources on a host|
|`net view \\<computer> /ALL`|Include hidden shares where supported|
|`net view /domain`|Domains/workgroups visible|
|`net view /domain:<name>`|Hosts/shares in a specific domain|
---
# 42. SNMP Enumeration
## Purpose
Enumerate network devices.
### Ports
|Port|Purpose|
|---|---|
|161|Queries|
|162|Traps|
### Versions
|Version|Security|
|---|---|
|v1|Weak|
|v2c|Weak|
|v3|Secure|
### Community Strings
|String|Permission|
|---|---|
|public|Read Only|
|private|Read/Write|
### MIB & OID
* MIB = Database
* OID = Individual Object
---
# 43. LDAP & Active Directory Enumeration
## LDAP
Protocol used to access directory services.
### Ports
|Port|Service|
|---|---|
|389|LDAP|
|636|LDAPS|
### Important Tools
|Tool|Purpose|
|---|---|
|ldapsearch|LDAP Enumeration|
|ldapdomaindump|AD Enumeration|
|enum4linux|Domain Enumeration|
|Nmap NSE|LDAP Search|
---
# 44. DNS Enumeration
## Purpose
Discover DNS infrastructure.
### Port
53 TCP/UDP
### Lookup Types
|Lookup|Record|
|---|---|
|Forward|A / AAAA|
|Reverse|PTR|
Zone Transfer ( AXFR ) Copies entire DNS database.
### Information Retrieved
* Subdomains
* Name Servers
* Mail Servers
* Internal Hosts
* IP Addresses
### Security
DNSSEC
Provides:
* Authentication
* Integrity
(Not Encryption)
---
# 45. SMTP Enumeration
## Purpose
Enumerate valid email users.
### Ports and commands
|Port|Purpose|
|---|---|
|25|SMTP|
|465|SMTPS|
|587|Mail Submission|
|Command|Purpose|
|---|---|
|HELO|Start Session|
|EHLO|Extended HELO|
|VRFY|Verify a user/mailbox exists|
|EXPN|Expand a mailing list / alias|
|RCPT TO|Reveal whether a recipient is accepted|
#### Modern servers usually disable/restrict VRFY and EXPN.
### What Each Service Reveals (don't lump "enumeration" together)
|Service|Exposes|
|---|---|
|LDAP/AD|Users, groups, directory objects|
|NTP|Time, server list, connected hosts|
|DNS|Hosts, records, possibly zone data|
|NFS|Exported/shared file systems|
|SNMP|Device config, interfaces, routes|
---
# 46. RPC & NFS Enumeration
### RPC
|Port|Service|
|---|---|
|111|RPCbind (Linux)|
|135|Microsoft RPC|
**Tool : rpcinfo**
Lists registered RPC services.
## NFS
Port : 2049
Purpose: Linux File Sharing
### Important Tools
|Tool|Purpose|
|---|---|
|showmount -e|List Exports|
|rpcinfo|RPC Services|
|mount|Mount NFS Share|
---
# 47. Enumeration Countermeasures
## Defense Strategy
Reduce Information
↓
Restrict Access
↓
Monitor Activity
↓
Respond
### Security Controls
|Threat|Defense|
|---|---|
|NetBIOS|Disable NetBIOS, Block 137–139|
|SMB|Disable SMBv1, SMB Signing|
|SNMP|SNMPv3, Change Community Strings|
|LDAP|LDAPS, Disable Anonymous Bind|
|DNS|Disable AXFR, DNSSEC|
|SMTP|Disable VRFY & EXPN|
|RPC|Restrict 111/135|
|NFS|Restrict Exports|
|Password Attacks|Strong Passwords + MFA|
|Enumeration|Firewall + IDS/IPS|
### Important Concepts
* Principle of Least Privilege (PoLP)
* Disable Unused Services
* Strong Authentication
* Patch Management
* Banner Hiding
* Logging & Monitoring
* Network Segmentation
**"FIM"**
* **F**irewall → Block
* **I**DS/IPS → Identify
* **M**onitor → Log Everything
---
---
# 48. Introduction to Vulnerability Analysis
## Definition
Systematic process of identifying, classifying, prioritizing, and validating security weaknesses before attackers exploit them.
### Purpose
* Identify weaknesses
* Measure severity
* Prioritize fixes
* Reduce attack surface
* Improve security posture
* Support compliance
### Types of Vulnerabilities
* Software
* Configuration
* Network
* Human
* Physical
### Common Sources
* Software Bugs
* Missing Patches
* Misconfiguration
* Weak Authentication
* Human Error
* Legacy Software
* Third-party Libraries
### Vulnerability Classification (major classes)
|Class|Examples|
|---|---|
|Misconfiguration|Default settings, open ports, verbose errors|
|Application Flaws|Injection, poor input validation|
|Poor Patch Management|Outdated/unpatched systems|
|Default Credentials|Vendor default user/pass left enabled|
|Design Flaws|Insecure logic/architecture|
|Third-Party Risks|Vulnerable libraries/vendor integrations|
---
# 49. Vulnerability Management Lifecycle
## Purpose
Continuous process of identifying, assessing, prioritizing, fixing and monitoring vulnerabilities.
### Risk Treatment Options
|Option|Meaning|
|---|---|
|Remediation|Fix Completely|
|Mitigation|Reduce Risk|
|Acceptance|Accept Risk|
|Transfer|Transfer Risk|
### Vulnerability Severity
* Critical
* High
* Medium
* Low
* Informational
**"Discover → Find → Assess → Prioritize → Fix → Verify → Repeat."**
**RMAT:**
* **R**emediate
* **M**itigate
* **A**ccept
* **T**ransfer
---
# 50. Vulnerability Classification Standard
## CVE
Common Vulnerabilities and Exposures
Purpose: Unique Vulnerability Identifier
Maintained By: MITRE
## CVSS
Common Vulnerability Scoring System
Purpose: Severity Score
Maintained By: FIRST
### CVSS Scores
|Score|Severity|
|---|---|
|0.0|None|
|0.1–3.9|Low|
|4.0–6.9|Medium|
|7.0–8.9|High|
|9.0–10|Critical|
### Metrics
* Base
* Temporal
* Environmental
## CWE
Common Weakness Enumeration
Purpose: Software Weakness Classification
Maintained By: MITRE
## CPE
Common Platform Enumeration
Purpose: Standardized Product Identification
Maintained By: NIST
**"ID → Score → Weakness → Product."**
* CVE → ID
* CVSS → Score
* CWE → Weakness
* CPE → Product
---
# 51. Vulnerability Databases & Security Advisories
## Major Databases
|Database|Purpose|
|---|---|
|NVD|National Vulnerability Database|
|CVE|Vulnerability IDs|
|CVSS|Severity|
|CWE|Weaknesses|
|CPE|Products|
|CAPEC|Attack Patterns|
|Exploit-DB|Public Exploits|
## NVD
Maintained By: NIST
Contains:
* CVE
* CVSS
* CWE
* CPE
* References
* Patch Information
## CAPEC
Common Attack Pattern Enumeration and Classification
Purpose: Attack Techniques
Maintained By: MITRE
## Exploit Database
Maintained By: Offensive Security
Search Tool: searchsploit
Contains:
* Proof-of-Concept Exploits
* Exploit Code
* Local & Remote Exploits
#### Zero-Day is a vulnerability for which **no patch is available**.
### ⚠️ Don't Confuse CVE / CVSS / Advisory
|Item|Role|
|---|---|
|**CVE**|Standard **ID** for one vulnerability (MITRE)|
|**CVSS**|**Severity score** 0–10 (FIRST)|
|**Security Advisory**|Vendor/researcher write-up + remediation|
CVE = *which* vulnerability. CVSS = *how bad*. They are not the same thing.
---
# 52. Vulnerability Assessment Types
## Assessment Types
|Assessment|Target|
|---|---|
|Network|Network Devices|
|Host|Operating Systems|
|Web|Web Applications|
|Database|Databases|
|Wireless|Wi-Fi|
|Cloud|Cloud Infrastructure|
|Container|Docker/Kubernetes|
## Credentialed vs Non-Credentialed
|Credentialed|Non-Credentialed|
|---|---|
|Login Required|No Login|
|Internal View|External View|
|More Accurate|Less Accurate|
## Internal vs External
|Internal|External|
|---|---|
|Inside Network|Internet|
|Insider View|Attacker View|
## Active vs Passive
|Active|Passive|
|---|---|
|Sends Packets|Observes Traffic|
## Agent-Based vs Agentless
|Agent-Based|Agentless|
|---|---|
|Software Installed|No Installation|
---
# 53. Vulnerability Assessment Tools
## Major Tools
|Tool|Purpose|
|---|---|
|Nessus|General Vulnerability Scanner|
|OpenVAS|Open-Source Vulnerability Scanner|
|Qualys VMDR|Enterprise Vulnerability Management|
|InsightVM|Risk-Based Assessment|
|Nikto|Web Server Scanner|
|Burp Suite|Web Application Testing|
|OWASP ZAP|Open-Source Web Testing|
|Nmap NSE|Basic Vulnerability Detection|
|Lynis|Linux Security Auditing|
|Trivy|Container Scanning|
|Scout Suite|Cloud Assessment|
---
# 54. Vulnerability Scanning Techniques
## Scanning Workflow
Discover Assets —> Detect Services —> Identify Versions —> Match CVEs —> Generate Report
## Compliance Scan
Checks:
* PCI-DSS
* HIPAA
* ISO 27001
* CIS
* NIST
---
# 55. Patch Management & Remediation
## Patch Types
|Type|Purpose|
|---|---|
|Security Patch|Security Fix|
|Bug Fix|Software Error|
|Feature Update|New Features|
|Hotfix|Emergency Fix|
|Service Pack|Collection of Updates|
## Remediation vs Mitigation
|Remediation|Mitigation|
|---|---|
|Removes Vulnerability|Reduces Risk|
---
# 56. Risk Assessment & Risk Management
## Risk Formula
```
Risk = Threat × Vulnerability × Impact
```
|Term|Meaning|
|---|---|
|Asset|Valuable Resource|
|Threat|Potential Danger|
|Vulnerability|Weakness|
|Risk|Chance of Loss|
## Risk Matrix
|Likelihood|Impact|Risk|
|---|---|---|
|High|High|Critical|
|High|Medium|High|
|Medium|Medium|Medium|
|Low|Low|Low|
## Risk Analysis Approaches
### Qualitative
* Rates risk by label: High / Medium / Low
* Subjective, fast, no dollar values
### Quantitative
* Uses numerical / monetary values
* **SLE** = Asset Value × Exposure Factor (loss per single incident)
* **ARO** = Annualized Rate of Occurrence (times per year)
* **ALE** = SLE × ARO (expected yearly loss — used to justify control spend)
## Risk Treatment “AMTA”
* **A**void (eliminate the activity)
* **M**itigate / Reduce (apply controls)
* **T**ransfer (insurance, outsource)
* **A**ccept (tolerate residual risk)
## Risk Types
|Type|Meaning|
|---|---|
|Inherent|Before Controls|
|Residual|After Controls|
---
# 57. Vulnerability Reporting
## Report Structure
Executive Summary —> Scope —> Methodology —> Findings —> Risk Rating —> Evidence —> Remediation —> References —> Appendix
## Findings Include
* CVE
* CVSS
* Severity
* Description
* Business Impact
* Remediation
* References
## Metrics
* MTTD
* MTTR
* Patch Compliance
* Critical Findings
* False Positive Rate
## False Positive vs False Negative
|Term|Meaning|
|---|---|
|False Positive|Tool reports a vuln that isn't really there (wasted effort)|
|False Negative|Real vuln is **missed** (dangerous — false sense of security)|
## Report Quality
A good finding connects **technical issue → business impact → specific remediation**, with evidence that makes it reproducible/defensible.
---
# 58. Vulnerability Validation & Penetration Testing
## Vulnerability Assessment vs Penetration Testing
|Vulnerability Assessment|Penetration Testing|
|---|---|
|Finds Weaknesses|Exploits Weaknesses|
|Low Risk|Higher Risk|
|Automated|Mostly Manual|
|Broad Coverage|Deep Testing|
|Regular|Periodic|
|Detects Vulnerabilities|Demonstrates Impact|
## Penetration Testing Lifecycle
```
Planning
      ↓
Recon
      ↓
Scanning
      ↓
Enumeration
      ↓
Exploitation
      ↓
Privilege Escalation
      ↓
Post Exploitation
      ↓
Reporting
```
## Vulnerability Assessment Limitations
* False Positives
* False Negatives
* Zero-Day Vulnerabilities
* Credential Issues
* Limited Context
* Dynamic Environments
---
## Best Practices
* Regular Scanning
* Validate Findings
* Prioritize Risk
* Patch Critical Issues
* Verify Fixes
* Maintain Asset Inventory
* Continuous Monitoring
* Combine VA + PT
---
---
# 59. System Hacking Methodology
## Definition
System Hacking is the phase after gaining initial access where the attacker attempts to obtain higher privileges, maintain access, and avoid detection.
### Methodology
Gain Access
↓
Password Cracking
↓
Privilege Escalation
↓
Execute Applications
↓
Hide Files
↓
Maintain Persistence
↓
Cover Tracks
### Goals
* Gain Access
* Escalate Privileges
* Execute Applications
* Maintain Access
* Cover Tracks
## Steganography vs Cryptography vs Steganalysis
|Term|What it does|
|---|---|
|**Steganography**|Hides the **existence** of data inside another medium (image, audio, file)|
|**Cryptography**|Hides the **meaning** of data (reversible with a key)|
|**Steganalysis**|Attempts to **detect** hidden data|
Used in "Hide Files" step. Can be combined (encrypt *then* hide). Whitespace/ADS/image-LSB are common carriers.
---
# 60. Password Attacks
## Password Storage
Passwords are stored as:
* NTLM
* LM (Legacy)
* SHA
* MD5 (General Hashing)
## Authentication vs Authorization
|Authentication|Authorization|
|---|---|
|Who are you?|What can you access?|
## Password Attack Categories (CEH's four)
|Category|Meaning|Examples|
|---|---|---|
|Non-Electronic|No tech needed|Shoulder surfing, dumpster diving, social engineering|
|Active Online|Interact with target directly|Brute force, password spraying, phishing|
|Passive Online|Observe without interacting|Sniffing, MITM, replay|
|Offline|Attack captured hashes|Dictionary, rainbow tables, rule-based|
#### Online = slower & noisier (lockouts/logs). Offline = much faster once hashes are stolen.
## Attack Types
|Attack|Description|
|---|---|
|Dictionary|Wordlist|
|Brute Force|Every Combination|
|Hybrid|Dictionary + Mutation|
|Rule-Based|Apply Rules|
|Rainbow Table|Precomputed Hashes|
|Offline|Crack Stolen Hashes|
|Online|Attack Login Service|
## Rainbow Tables
Fast lookup tables. Defeated by:  Salt
## Salt
Random value added before hashing.
Purpose:
* Prevent Rainbow Tables
* Prevent identical hashes
* Slow cracking
---
# 61. Windows & Linux Password Storage
## SAM
Stores:
* Local Accounts
* NTLM Hashes
Location
```
C:\Windows\System32\config\SAM
```
## Credential Storage Locations (know these)
|Location|Holds|
|---|---|
|`C:\Windows\System32\config\SAM`|Local account NTLM hashes|
|Registry SYSTEM hive|Boot key to decrypt SAM|
|**LSASS** (memory)|Hashes, Kerberos tickets, sometimes plaintext|
|**NTDS.dit**|Active Directory domain account hashes (DC)|
## Linux Password Storage
|File|Contents|
|---|---|
|`/etc/passwd`|Account info (username, UID, shell) — **world-readable, no hashes normally**|
|`/etc/shadow`|Actual password **hashes** — root-only|
#### Exam trap: hashes live in **`/etc/shadow`**, not `/etc/passwd`.
## LM vs NTLM
|LM|NTLM|
|---|---|
|Legacy|Modern|
|Uppercase only|Case Sensitive|
|Max 14 Characters|Long Passwords|
|Weak|Stronger|
#### Why LM is broken
* Password is converted to **uppercase** (kills case complexity).
* Split into **two 7-character halves**, each hashed separately → effectively two weak 7-char passwords, cracked independently and fast.
* No salt → identical passwords produce identical hashes.
* A password ≤ 7 chars leaves the second half as a known constant (`AAD3B435B51404EE`), instantly revealing the length.
## Active Directory
#### Kerberos : Ticket-based authentication.
Components:
* Client
* KDC
* TGT
* Service Ticket
## NTLM vs Kerberos
|NTLM|Kerberos|
|---|---|
|Challenge-Response|Ticket-Based|
|Older|Modern|
---
# 62. Password Cracking Tools
|Tool|Purpose|
|---|---|
|John the Ripper|Offline Cracking|
|Hashcat|GPU Password Cracking|
|Hydra|Online Login Cracking|
|Medusa|Online Cracking|
|Ophcrack|Rainbow Tables|
|Cain & Abel|Windows Password Recovery|
## Password Spraying
One Password —> Many Users
## Credential Stuffing
Previously leaked credentials —> Multiple websites
## Offline vs Online
|Offline|Online|
|---|---|
|Hashes|Login Services|
|Faster|Slower|
|Hard to Detect|Easy to Detect|
---
# 63. Credential Dumping
## Credential Storage
Windows
│
├── SAM
├── LSASS
├── NTDS.dit
├── Credential Manager
└── Kerberos Tickets
## LSASS
Local Security Authority Subsystem Service
Stores:
* NTLM Hashes
* Plaintext Passwords
* Kerberos Tickets
* Cached Credentials
## NTDS.dit
Stores:
* Domain Accounts
* Active Directory Objects
## Mimikatz
Purpose:
* Dump Credentials
* Pass-the-Hash
* Pass-the-Ticket
* Golden Ticket
## Pass-the-Hash vs Pass-the-Ticket
|PtH|PtT|
|---|---|
|NTLM Hash|Kerberos Ticket|
|Older|Modern AD|
## Golden vs Silver Ticket
|Golden|Silver|
|---|---|
|Fake TGT|Fake Service Ticket|
|Entire Domain|One Service|
|Forged with krbtgt hash|Forged with service account hash|
## Keyloggers: Software vs Hardware
|Software Keylogger|Hardware Keylogger|
|---|---|
|Program on the system|Physical device in keyboard/USB path|
|Can be detected by AV/EDR|**Not** seen by AV (not software)|
|Remotely installable|Needs physical access|
---
# 64. Privilege Escalation
## Types
|Vertical|Horizontal|
|---|---|
|User → Admin|User → User|
|Higher Privileges|Same Privilege|
## Common Techniques
* Weak Services
* DLL Hijacking
* Kernel Exploits
* Weak Registry Permissions
* Weak File Permissions
* PATH Hijacking
* Weak sudo
* SUID
#### DLL Hijacking —> Abuses DLL Search Order.
#### Linux —> Runs executable with owner's privileges.
#### PATH Hijacking —> Malicious executed before legitimate one.
**"SUID = Someone Else's ID."**
**"DLL = Windows, PATH = Linux."**
#### ⚠️ Mnemonic, not a rule
"DLL = Windows, PATH = Linux" is a memory aid. Windows **also** has PATH/search-order hijacking; the association is just *strongest* on each side. Privilege escalation abuses both **software vulnerabilities** and **misconfiguration** (weak service/file/registry permissions, unquoted service paths, misconfigured `sudo`, UAC bypass).
---
# 65. Executing Applications
## Common Execution Methods
* PowerShell
* CMD
* WMI
* Scheduled Tasks
* Services
* DLL Loading
## Process Injection
Inject malicious code inside another process.
## DLL Injection
Inject DLL into running process.
## Reflective DLL Injection
Loads DLL directly into memory.
## Process Hollowing
Replace legitimate process code with malicious code.
## Fileless Malware
Runs in memory.
Uses:
* PowerShell
* WMI
* LOLBins
## LOLBins
|Tool|Purpose|
|---|---|
|PowerShell|Scripts|
|cmd|Commands|
|certutil|Download Files|
|rundll32|DLL Execution|
|regsvr32|Register DLL|
|mshta|HTA Execution|
|wmic|Remote Management|
|bitsadmin|Downloads|
---
# 66. Persistence
## Common Persistence Techniques
|Technique|Platform|
|---|---|
|Registry Run Keys|Windows|
|Startup Folder|Windows|
|Scheduled Tasks|Both|
|Windows Services|Windows|
|Cron Jobs|Linux|
|RAT|Both|
|Backdoor|Both|
|Rootkit|Both|
|Web Shell|Web|
## Registry Run Keys
Automatically execute at login.
## Startup Folder
Automatically executes applications after login.
## Windows Services
Start during boot.
## Cron Jobs
Linux process scheduler.
## RAT
#### “Remote Access Trojan”
It provides complete remote control.
## Web Shell
Remote command execution through browser.
## Rootkits
Hide:
* Files
* Processes
* Drivers
* Registry
* Network Connections
---
# 67. Covering Tracks & Anti-Forensics
## Goal
Hide evidence after compromise.
## Techniques
* Clear Logs
* Time-stomping
* ADS
* Secure Delete
* Rootkits
* Encryption
* Artifact Removal
## Windows Logs
* Security
* Application
* System
#### Linux logs exist at `/var/log` (e.g. `/var/log/auth.log`, `/var/log/syslog`)
Common log-clearing commands attackers abuse: `wevtutil cl` (Windows), `Clear-EventLog` (PowerShell), `echo > /var/log/...` or editing `/var/log/wtmp`, `utmp`, `btmp` (Linux).
## Time-stomping (MAC times)
Changes:
* Modified
* Accessed
* Created
## ADS
Alternate Data Streams. NTFS only. Hide data inside files.
## Secure Delete
Overwrite data before deleting.
## Anti-Forensics
* Hide Evidence
* Destroy Evidence
* Modify Evidence
* Prevent Analysis
---
---
# 68. Malware Lifecycle
## Malware Infection Process
**D → Delivery**
Malware reaches the victim.
Examples:
* Phishing Email
* USB
* Drive-by Download
**E → Execution**
Victim executes malware.
Examples:
* Double-click EXE
* Office Macro
* PowerShell
**I → Installation**
Malware copies itself onto the system.
Examples:
* AppData
* Startup Folder
* Registry
**P → Persistence**
Survives reboot.
Examples:
* Registry Run Keys
* Scheduled Tasks
* Services
**C → Command & Control (C2)**
Contacts attacker.
Examples:
* HTTP/HTTPS
* DNS
* IRC
**A → Actions on Objectives**
Performs attack.
Examples:
* Encrypt Files
* Steal Passwords
* Install RAT
* DDoS
### Mnemonic
## **"DEIPCA"**
* **D**elivery
* **E**xecution
* **I**nstallation
* **P**ersistence
* **C**ommand & Control
* **A**ctions on Objectives
---
# 69. Malware Types
|Malware|Purpose|
|---|---|
|Virus|Infect Files|
|Worm|Self Spread|
|Trojan|Disguise|
|Spyware|Spy|
|Keylogger|Record Keys|
|Adware|Ads|
|Rootkit|Hide Malware|
|RAT|Remote Control|
|Bot|Controlled Device|
|Botnet|Group of Bots|
|Ransomware|Encrypt Files|
|Logic Bomb|Trigger-Based|
|Fileless|Memory Execution|
|Wiper|Destroy Data|
|Cryptojacker|Mine Cryptocurrency|
### Virus vs Worm vs Trojan
|Virus|Worm|Trojan|
|---|---|---|
|Needs Host/File|Standalone|Disguised|
|Usually user-triggered|Automatic Spread|User Installs|
|Self-Replicates|Self-Replicates|No Replication|
#### ⚠️ A virus is defined by **replicating into a host/file**, not strictly by "must need user action." User interaction is often *part of* the chain but is not the defining trait. Worm = autonomous spread; Trojan = disguise (no self-replication).
## Components of Malware (building blocks)
|Component|Role|
|---|---|
|Crypter|Conceal/encrypt malware to evade AV|
|Packer|Compress/obscure the executable|
|Obfuscator|Make code hard to read/analyze|
|Downloader|Pulls additional malicious code|
|Dropper|Carries/installs the malware|
|Injector|Injects code into running processes|
|Exploit|Code that triggers the vulnerability|
|Payload|Code that performs the malicious action|
|Malicious Code|The core harmful logic|
## PUA / PUP (Potentially Unwanted Applications)
Not confirmed malware, but a security/privacy risk:
* Adware, Dialers
* Torrent/bundled software
* Marketing/behavior-tracking software
* Cryptomining/cryptojacking software
#### PUA ≠ malware, but still unwanted.
---
# 70. Malware Delivery Methods
|Method|Description|
|---|---|
|Phishing|Generic Email|
|Spear Phishing|Targeted Email|
|Whaling|Executive Target|
|Office Macro|VBA Code|
|USB|Removable Media|
|Drive-by Download|Browser Exploit|
|Watering Hole|Trusted Website Compromised|
|Malvertising|Malicious Ads|
|Fake Software|Trojan Delivery|
|Fake Updates|Fake Patch|
|Supply Chain|Compromised Vendor|
## Web-Based Distribution Techniques (named)
* Black-hat SEO (poison search rankings)
* Social-engineered clickjacking
* Spear-phishing sites
* Malvertising & compromised legitimate sites
* Drive-by downloads
* Spam emails & malicious attachments
* RTF / document injection
#### Also enters via: IM, removable media, browser/email bugs, poor patching, fake apps, network propagation. Attackers social-engineer the **delivery**, not just the exploit.
---
# 71.0 Trojan Types
|Trojan|Purpose|
|---|---|
|Backdoor|Hidden Access|
|RAT|Remote Control|
|Banking|Steal Banking Data|
|Downloader|Download Malware|
|Dropper|Carry Malware|
|Spy|Spy|
|Keylogger|Record Keys|
|DDoS|Attack Targets|
|Proxy|Anonymous Relay|
|FTP|File Transfer|
|Security Disabler|Disable AV|
|Rootkit|Hide Malware|
|Scareware|Fake Antivirus|
# 71.1  Virus Types
|Virus|Target|
|---|---|
|Boot Sector|MBR|
|File Infector|Executables|
|Macro|Office Documents|
|Resident|RAM|
|Direct Action|One-Time|
|Multipartite|Boot + Files|
|Polymorphic|Changes Signature|
|Metamorphic|Rewrites Code|
|Stealth|Hides|
|Overwriting|Destroys Files|
# 71.2 Famous Worms
|Worm|Target|
|---|---|
|Morris|Internet|
|Code Red|IIS|
|SQL Slammer|SQL Server|
|Conficker|Windows|
|WannaCry|SMB|
# 71.3 Ransomware
|Type|Description|
|---|---|
|Crypto|Encrypt Files|
|Locker|Lock Device|
|Double Extortion|Steal + Encrypt|
|Triple Extortion|Steal + Encrypt + Pressure|
|RaaS|Ransomware Rental|
### Encryption
* **AES** → Encrypt Files (fast symmetric)
* **RSA/ECC** → Encrypt the AES key (so only attacker can recover it)
#### This is the **hybrid encryption** pattern. It's the *common* ransomware design, not a universal rule — implementations vary.
# 71.4 Rootkits
|Rootkit|Purpose|
|---|---|
|User Mode|User Applications|
|Kernel Mode|Kernel|
|Bootkit|Boot Loader|
|Firmware|BIOS/UEFI|
|Hypervisor|Below OS|
### Special Technique
**DKOM**
Direct Kernel Object Manipulation
# 71.5 Botnets & Command-and-Control
## Botnet Architecture
Attacker —> C2 Server —> Bots —> Victims
### C2 Types
* IRC
* HTTP/HTTPS
* DNS
* Peer-to-Peer
---
# 72. Malware Evasion
|Technique|Purpose|
|---|---|
|Obfuscation|Hide Code|
|Packing|Hide Executable|
|Encryption|Hide Strings|
|Polymorphism|Change Signature|
|Metamorphism|Rewrite Code|
|Anti-Debug|Detect Debugger|
|Anti-VM|Detect VM|
|Anti-Sandbox|Detect Sandbox|
|Delayed Execution|Wait|
|LOLBins|Use Trusted Tools|
### Mnemonic
## **"Old Programmers Eat Pizza After Very Stressful Days Lazily."**
* **O**bfuscation
* **P**acking
* **E**ncryption
* **P**olymorphism
* **M**etamorphism
* **A**nti-Debug
* **V**M Detection
* **A**nti-Sandbox
* **D**elayed Execution
* **L**OLBins
---
# 73. Indicators of Compromise (IoCs) and Indicators of Attack (IoA)
## IoC vs IoA
|IoC|IoA|
|---|---|
|Evidence After Attack|Suspicious Behavior|
|Reactive|Proactive|
### Types of IoC’s
* File
* Host
* Network
* Behavioral
### Common IoC’s
* SHA256 Hash
* IP Address
* Domain
* URL
* Registry Key
* Process
* Service
* DNS Query
* Mutex
### Threat Intelligence
* MITRE ATT&CK → TTP Mapping
* STIX → Threat Intelligence Format
* TAXII → Threat Intelligence Sharing
---
# 74. Malware Analysis
## Definition
The process of examining malware to understand its behavior, origin, and impact.
## Sheep Dip
A **dedicated, isolated computer** used to test suspicious files/media before they touch the production network. Runs AV, port monitors, and analysis tools.
## Static vs Dynamic Analysis
|Static (Code Analysis)|Dynamic (Behavioral)|
|---|---|
|Does NOT run the malware|Runs malware in a sandbox|
|Inspect file, strings, hashes, headers|Observe runtime behavior|
|Safer|Riskier (contained)|
|Disassembly, PE header, packing|Registry, file, network, process changes|
## Static Analysis Includes
* File fingerprinting (hashes)
* Malware disassembly (IDA, Ghidra)
* String search
* Packing/obfuscation detection
* PE/ELF header analysis
* Identifying file dependencies
## Dynamic Analysis Monitors
|Area|Tool Examples|
|---|---|
|Process|Process Monitor, Process Explorer|
|Registry|Regshot|
|Network|Wireshark, TCPView|
|Files|Process Monitor|
|API calls|API Monitor|
---
# 75. Malware Analysis Environment & Tools
## Safe Lab Setup
* Isolated VM / sandbox (no bridged network)
* Snapshots for rollback
* Host-only or simulated internet (INetSim)
## Common Sandboxes / Services
* Cuckoo Sandbox
* Any.Run
* Hybrid Analysis
* VirusTotal (multi-engine hash/file lookup)
* Joe Sandbox
## Key Tools
|Tool|Purpose|
|---|---|
|PEiD / Detect It Easy|Detect packers|
|Dependency Walker|DLL dependencies|
|Strings|Extract readable text|
|IDA / Ghidra|Disassembly / reverse engineering|
|OllyDbg / x64dbg|Debugging|
---
# 76. Advanced Persistent Threat (APT)
## Definition
A **stealthy, long-term, targeted** attack (often nation-state) that maintains undetected access to steal data over time.
## Characteristics
* Highly skilled & well-funded
* Specific target (not opportunistic)
* Long dwell time
* Uses zero-days and custom malware
* Low and slow / evades detection
## APT Lifecycle
Preparation → Initial Intrusion → Expansion (lateral movement) → Persistence → Data Exfiltration → Cleanup
---
# 77. Fileless Malware (Deep Dive)
## Definition
Malware that runs **in memory** using legitimate, trusted system tools — leaving little or no file on disk (hard for signature AV to catch).
## Living-off-the-Land (LOLBins)
Uses built-in tools: PowerShell, WMI, `mshta`, `rundll32`, `regsvr32`, `certutil`.
## Why It Evades
* No executable file to scan
* Trusted/signed binaries
* Resides in RAM, registry, or WMI repository
## Detection
* Behavioral / EDR monitoring
* Script-block & PowerShell logging
* Memory forensics
## Overt vs Covert Channels
|Overt Channel|Covert Channel|
|---|---|
|Legitimate, intended communication|Hidden, unintended path|
|Normal app traffic|Smuggles data (e.g. via ICMP, DNS, timing)|
RATs/Trojans often use **covert channels** to exfiltrate data unnoticed.
---
# 78. Malware Countermeasures
|Countermeasure|Purpose|
|---|---|
|Antivirus|Known Malware Detection|
|EDR|Endpoint Behavior|
|XDR|Enterprise-wide Detection|
|Patch Management|Fix Vulnerabilities|
|Least Privilege|Limit Damage|
|Application Whitelisting|Allow Only Trusted Apps|
|Network Segmentation|Stop Lateral Movement|
|Secure Boot|Prevent Bootkits|
|MFA|Prevent Account Abuse|
|Offline Backups|Ransomware Recovery|
|User Awareness|Prevent Phishing|
|Email Security|Block Malware Delivery|
|Incident Response|Respond & Recover|
## 3-2-1 Backup Rule
* **3** Copies
* **2** Different Media
* **1** Offline (or Immutable) Copy
---
---
# 79. Network Sniffing Fundamentals
## What is Sniffing?
Capturing and analyzing packets traveling across a network.
Can capture:
* Usernames
* Passwords
* Cookies
* Emails
* DNS Queries
* Files
* Session Tokens
## Types of Sniffing
|Type|Description|
|---|---|
|Passive|Listen Only|
|Active|Manipulate Network|
## Hub vs Switch
|Hub|Switch|
|---|---|
|Broadcasts All Traffic|Sends to Destination Only|
|Easy to Sniff|Difficult to Sniff|
## Promiscuous Mode
NIC accepts **all Ethernet frames**.
## Monitor Mode
Wireless NIC captures **all Wi-Fi frames**.
---
# 80. Packet Flow and OSI layers
## Packet Flow
Application —> TCP Header —> IP Header —> Ethernet Header —> Bits
## OSI Layers
![](https://beta.appflowy.cloud/api/file_storage/adefbea7-8428-4793-9c94-60a521191aed/v1/blob/20323db1-7670-410e-a775-d1aa47513dc2/NKGJDryDNgMNWtmCVVE1txJ4iyLDn7jFebSa8W06K78=.png)
|Layer|Contains|
|---|---|
|L7|HTTP, FTP, DNS|
|L6|SSL/TLS|
|L5|Sessions|
|L4|TCP/UDP Ports|
|L3|IP Addresses|
|L2|MAC Addresses|
|L1|Bits|
## Traffic Types
* Unicast → One Device
* Broadcast → Everyone
* Multicast → Group
---
# 81. Active vs Passive Sniffing
|Passive|Active|
|---|---|
|Listen Only|Modify Network|
|No Injection|Packet Injection|
|Hub|Switch|
|Hard to Detect|Easier to Detect|
## Active Sniffing Techniques
* ARP Spoofing
* MAC Flooding
* DHCP Starvation
* STP Attack
* Switch Port Stealing
## Defenses
* Dynamic ARP Inspection
* DHCP Snooping
* Port Security
* Root Guard
---
# 82. ARP Protocol & ARP Spoofing
## ARP
Maps **IPv4 → MAC** on the **local Layer-2 network only**.
#### ⚠️ ARP is **not** routable across the Internet and does **not** handle IPv6 — IPv6 uses **NDP (Neighbor Discovery Protocol)** instead.
## ARP Process
Broadcast ARP Request —> Unicast ARP Reply —> ARP Cache Update
## ARP Spoofing
Fake ARP Replies —> Victim Updates Cache —>Traffic Goes to Attacker —> MITM
## Best Defense
* Dynamic ARP Inspection
* Static ARP Entries
* DHCP Snooping
---
# 83. MAC Flooding & CAM Table
## CAM Table
Stores **MAC → Port**
## MAC Learning
Switch learns the Source MAC which then updates CAM table
## MAC Flooding
Thousands of Fake MACs
↓
CAM Overflow
↓
Unknown Unicast Flooding
↓
Traffic Captured
## CAM vs ARP
|CAM|ARP|
|---|---|
|Switch|Host|
|MAC → Port|IP → MAC|
## Prevention
* Port Security
* Sticky MAC
* VLANs
* 802.1X
---
# 84. DHCP Starvation & Rogue DHCP
## DHCP
Automatically assigns:
* IP Address
* Gateway
* DNS
* Subnet Mask
## DHCP Ports
* UDP 67 → Server
* UDP 68 → Client
## DORA Process
* **D**iscover
* **O**ffer
* **R**equest
* **A**cknowledge
## DHCP Starvation
Fake MAC Addresses —> Exhaust DHCP Pool —> No IPs Left
## Rogue DHCP
Fake DHCP Server
↓
Victim Receives
* Fake Gateway
* Fake DNS
* Fake Routes
↓
MITM
## Best Defense
* DHCP Snooping
* Port Security
* IDS/IPS
---
# 85. DNS Spoofing & DNS Cache Poisoning
## DNS
Maps **Domain → IP**
## DNS Resolution
Browser Cache —> OS Cache —> Router —> Resolver —> Root —> TLD —> Authoritative DNS
## Important DNS Records
|Record|Purpose|
|---|---|
|A|IPv4|
|AAAA|IPv6|
|MX|Mail|
|NS|Name Server|
|CNAME|Alias|
|PTR|Reverse Lookup|
|TXT|Verification|
|SOA|Zone Info|
## DNS Spoofing
Fake DNS Reply —> Wrong IP
## DNS Cache Poisoning
Fake Record Stored —> Future Users Redirected
## Pharming
Correct URL goes to a Fake Website
## Hosts File
Windows
```
C:\Windows\System32\drivers\etc\hosts
```
Linux
```
/etc/hosts
```
## Best Defense
* DNSSEC
* HTTPS
* DoH / DoT
* Flush DNS Cache
---
# 86. Sniffing Tools
|Tool|Purpose|
|---|---|
|Wireshark|GUI Packet Analyzer|
|Tshark|CLI Wireshark|
|tcpdump|CLI Capture|
|Bettercap|Modern MITM|
|Ettercap|MITM Framework|
|Scapy|Packet Crafting|
|NetworkMiner|Network Forensics|
## Wireshark
Three Panes
* Packet List
* Packet Details
* Packet Bytes
### Wireshark Display Filters (know these)
|Filter|Shows|
|---|---|
|`ip.addr == 10.0.0.5`|Traffic to/from a host|
|`tcp.port == 80`|Traffic on a port|
|`http` / `dns` / `arp`|By protocol|
|`tcp.flags.syn == 1`|SYN packets (scan detection)|
|`ip.src == x && ip.dst == y`|Directional filter|
#### Capture filter (BPF) vs display filter: capture filters limit what's recorded; display filters just hide/show captured packets.
## SPAN Port / Port Mirroring
Switch feature that **copies traffic** from selected ports/VLANs to a monitor port so an analyzer can see it (switches normally isolate traffic). A legitimate way to sniff a switched network.
## Hardware Protocol Analyzers
Dedicated appliances that capture/decode traffic (incl. high-speed Ethernet/Fibre Channel) — more capable than software sniffers for heavy environments.
## Wiretapping
* **Active wiretapping** → inject/alter traffic.
* **Passive wiretapping** → only monitor/record.
* **Lawful interception** → authorized, legal monitoring by agencies. Unauthorized wiretapping is illegal — not "admin sniffing."
## Snort (IDS) Basics
Open-source IDS/IPS using rule signatures.
* Rule format: `action proto src_ip src_port -> dst_ip dst_port (options)`
* Example: `alert tcp any any -> 10.0.0.0/24 80 (msg:"HTTP"; sid:1000001;)`
* Recognize the action, protocol, ports, and direction (`->`) in output.
---
# 87. Detecting & Preventing Sniffing
## Detect
* Promiscuous Mode
* Duplicate MACs
* ARP Changes
* Rogue DHCP
* Wrong DNS
* SSL Warnings
* IDS Alerts
## Layer 2 Defenses
* Dynamic ARP Inspection
* DHCP Snooping
* Port Security
* Sticky MAC
* VLAN Segmentation
## Encryption
|Insecure|Secure|
|---|---|
|HTTP|HTTPS|
|Telnet|SSH|
|FTP|SFTP|
|POP3|POP3S|
|IMAP|IMAPS|
|SMTP|SMTPS|
## IDS vs IPS
|IDS|IPS|
|---|---|
|Detect|Detect + Block|
## Best Practices
* HTTPS
* VPN
* SSH
* SFTP
* DAI
* DHCP Snooping
* Port Security
* VLANs
* IDS/IPS
---
---
# 88. Introduction to Social Engineering
## What is Social Engineering?
Manipulating **people**, rather than computers, into revealing sensitive information or performing insecure actions.
Targets:
* Passwords
* OTPs
* Financial Information
* Physical Access
* Confidential Data
## Why It Works — Psychological Triggers
Scenario questions describe the behavior without naming it:
|Trigger|Lever|
|---|---|
|Authority|"I'm from IT/the CEO"|
|Intimidation|Threats/pressure|
|Consensus / Social Proof|"Everyone else did it"|
|Scarcity|"Only a few left"|
|Urgency|"Act now or lose access"|
|Familiarity / Liking|Builds rapport first|
|Trust|Poses as a trusted party|
|Greed|Promise of reward/money|
## Social Engineering Lifecycle
Reconnaissance —> Information Analysis —> Build Trust —> Exploitation —> Execution —> Exit
## Main Goals
* Credential Theft
* Financial Fraud
* Malware Installation
* Physical Access
* Information Gathering
---
# 89. Human-Based Social Engineering
## Common Human-Based Attacks
|Attack|Purpose|
|---|---|
|Impersonation|Fake Identity|
|Pretexting|Fake Story|
|Tailgating|Secret Entry|
|Piggybacking|Allowed Entry|
|Shoulder Surfing|Observe Credentials|
|Eavesdropping|Listen Secretly|
|Dumpster Diving|Search Trash|
|Reverse Social Engineering|Victim Contacts Attacker|
|Vishing|Voice/phone pretext call|
|Diversion Theft|Trick delivery to wrong place|
|Honey Trap|Fake romantic/online lure|
|Baiting|Leave infected media/USB|
|Quid Pro Quo|"Service" in exchange for info|
|Elicitation|Casual conversation to extract info|
## Tailgating vs Piggybacking
|Tailgating|Piggybacking|
|---|---|
|No Permission|Permission Given|
|Victim Unaware|Victim Aware|
## Impersonation vs Pretexting
|Impersonation|Pretexting|
|---|---|
|Fake Identity|Fake Story|
---
# 90. Computer-Based Social Engineering
## Phishing Family
|Attack|Medium|
|---|---|
|Phishing|Email|
|Spear Phishing|Targeted Email|
|Whaling|Executive Email|
|Clone Phishing|Copied Email|
|BEC|Business Email|
|Smishing|SMS|
|Vishing|Voice|
|Angler|Social Media|
|Quishing|QR Code|
|Search Engine Phishing|Search Results|
## Email Authentication
|Technology|Purpose|
|---|---|
|SPF|Verify Sender|
|DKIM|Verify Integrity|
|DMARC|Enforce Policy|
## Common Indicators
* Urgent Language
* Misspelled Domains
* Suspicious Links
* Unexpected Attachments
* Requests for OTPs
* Poor or Unexpected Context
## Other Computer-Based Techniques
Phishing, Spam, Instant-messaging abuse, Pop-up window attacks, Scareware, Deepfake videos, Voice cloning.
## Mobile-Based Social Engineering
Malicious apps, Fake apps, Repackaged apps, QR-code attacks (quishing), SMS phishing (smishing).
---
# 91. Physical Social Engineering
## Physical Attacks
|Attack|Purpose|
|---|---|
|USB Drop|Malware Installation|
|Baiting|Exploit Curiosity|
|Juice Jacking|Data Theft|
|Evil Maid|Device Tampering|
|Badge Cloning|Physical Access|
|Rogue Device|Network Access|
|Hardware Keylogger|Capture Keystrokes|
|Shoulder Surfing|Observe Passwords|
## Physical Security Controls
* CCTV
* Security Guards
* Biometrics
* Smart Cards
* Turnstiles
* Visitor Logs
* Locked Server Rooms
---
# 92. Social Engineering Lifecycle & OSINT
## OSINT
Open Source Intelligence means collecting publicly available information.
## Phases of a Social Engineering Attack
1. Research the target company
2. Select a target (individual)
3. Develop a relationship
4. Exploit the relationship
## Passive vs Active Recon
|Passive|Active|
|---|---|
|No Interaction|Direct Interaction|
|Hard to Detect|Easier to Detect|
## Common OSINT Sources
* Google
* LinkedIn
* Facebook
* Instagram
* GitHub
* WHOIS
* Shodan
* Company Websites
* Data Breaches
## Popular OSINT Tools
|Tool|Purpose|
|---|---|
|Google Dorks|Advanced Search|
|Maltego|Relationship Mapping|
|theHarvester|Emails|
|SpiderFoot|Automated OSINT|
|Recon-ng|OSINT Framework|
|Shodan|Internet Devices|
|WHOIS|Domain Information|
|Have I Been Pwned|Breach Lookup|
---
# 93. AI-Powered Social Engineering
## AI Attacks
* Deepfakes
* Voice Cloning
* Face Swapping
* AI Phishing
* AI Spear Phishing
* Chatbot Impersonation
* Fake Video Meetings
## Deepfake vs Voice Cloning
|Deepfake|Voice Cloning|
|---|---|
|Video/Image|Audio|
|Fake Face|Fake Voice|
## Defenses
* MFA
* Zero Trust
* Human Verification
* Security Awareness
* Multi-Channel Verification
---
# 94. Social Engineering Tools
|Tool|Purpose|
|---|---|
|SET|Social Engineering Framework|
|Gophish|Phishing Simulation|
|King Phisher|Phishing Campaign|
|Evilginx|Reverse Proxy Phishing|
|Modlishka|Reverse Proxy Phishing|
|BeEF|Browser Exploitation|
|HiddenEye|Phishing Templates|
SET supports:
* Website Cloning
* Credential Harvesting
* USB Payloads
* Email Attacks
* QR Phishing
---
# 95. Detection, Prevention & Countermeasures
## Best Defenses
* Security Awareness Training
* MFA
* Zero Trust
* Least Privilege
* Incident Reporting
* Verification Procedures
## Email Protection
|Technology|Purpose|
|---|---|
|SPF|Verify Sender|
|DKIM|Verify Integrity|
|DMARC|Enforce Policy|
## Authentication Factors
|Factor|Example|
|---|---|
|Something You Know|Password|
|Something You Have|Phone, Smart Card|
|Something You Are|Fingerprint|
## Organizational Controls
* Password Managers
* HTTPS
* SSH
* VPN
* Security Policies
* Clean Desk Policy
* USB Policies
* Social Media Policy
---
---
# 96. Introduction to Denial-of-Service (DoS)
## What is DoS?
A **Denial-of-Service (DoS)** attack attempts to make a system, network, or service **unavailable** to legitimate users by exhausting its resources.
Unlike attacks that steal data, the primary objective is **availability disruption**.
## CIA Triad Impact
|Security Principle|Impact|
|---|---|
|Confidentiality|❌ Usually unaffected|
|Integrity|❌ Usually unaffected|
|Availability|✅ Primary Target|
---
# 97. Objectives of DoS
* Consume bandwidth
* Exhaust CPU
* Exhaust RAM
* Exhaust connection tables
* Crash applications
* Prevent legitimate access
## What DoS Attacks Consume/Disrupt
Bandwidth · CPU · Memory · Connection/session resources · Disk space & data structures · Physical/network components · Programs/files.
## Characteristics
* Single source (DoS) vs many sources (DDoS)
* Targets one or more services
* Resource exhaustion
* Service disruption
#### ⚠️ DoS is defined by **disrupting availability**, and DDoS by **distributed sources** — not strictly by "exactly one machine." The key DoS-vs-DDoS difference is the **distribution of attack sources**.
---
# 98. Distributed Denial-of-Service (DDoS)
## What is DDoS?
A **Distributed Denial-of-Service (DDoS)** attack uses **multiple compromised systems** (bots) to attack one victim simultaneously.
## Components
Bot : An infected computer controlled remotely.
Botmaster: Controls the botnet.
Command & Control (C2): Server used to send attack commands.
Zombie: Another name for an infected bot.
## Common Botnet Examples
* Mirai
* Zeus
* Mozi
* Cutwail
* Emotet
---
# 99. Types of DoS Attacks
DoS attacks are classified into three major categories.
## Volume-Based Attacks
Goal:
Consume bandwidth.
Examples:
* UDP Flood
* ICMP Flood
* DNS Amplification
* NTP Amplification
* SSDP Amplification
## Protocol Attacks
Exploit weaknesses in protocols.
Examples:
* SYN Flood
* Ping of Death
* Smurf Attack
* Fraggle Attack
* LAND Attack
* Teardrop Attack
## Application Layer Attacks
Target applications instead of networks.
Examples:
* HTTP GET Flood
* HTTP POST Flood
* Slowloris
* Slow POST
* DNS Query Flood
|Attack Type|Target|
|---|---|
|Volume|Bandwidth|
|Protocol|Network Stack|
|Application|Web Server/Application|
---
# 100. Common DoS Attacks
## SYN Flood
Abuses TCP three-way handshake.
Attacker sends:
SYN —> Server replies —> No ACK
Half-open connections accumulate. Hence, The Server resources are exhausted.
## UDP Flood
Attacker sends huge numbers of UDP packets.
Victim repeatedly checks for applications listening. CPU usage increases.
## ICMP Flood
Massive number of ICMP Echo Requests. It Consumes bandwidth.
## Ping of Death
Oversized malformed ICMP packets.
Historically crashed older operating systems.
Modern systems are generally patched.
## Smurf Attack
Attacker Spoofs victim IP —> Sends ICMP request —> Broadcast network replies —> Victim flooded
## Teardrop Attack
Uses overlapping IP fragments. Causes fragmentation issues.
## Slowloris
Keeps HTTP connections open. Never completes requests.
Server eventually runs out of connections.
## HTTP Flood
Legitimate-looking HTTP requests.
Hard to distinguish from real traffic.
## Phlashing (Permanent DoS / PDoS)
Attack that **permanently damages** hardware — e.g. pushing malicious firmware that "bricks" a device. Recovery needs reinstall/replacement, not just a reboot.
---
# 101. Reflection & Amplification Attacks
Amplification attacks increase attack traffic using protocols with responses larger than requests.
## Reflection vs Amplification
|Reflection|Amplification|
|---|---|
|Send request to 3rd-party servers with **spoofed victim IP** → replies flood victim|Response is **much larger** than the request → multiplies volume|
#### A single attack can be **both** reflective and amplifying (e.g. DNS/NTP amplification).
## Reflection Process
Attacker —> Spoofs Victim IP —> Reflection Server —> Victim
## Amplification Protocols
* DNS
* NTP
* SSDP
* Memcached
* CLDAP
## Common Reflection Attacks
### DNS Amplification
Small DNS request —> Large DNS response.
### SSDP Amplification
Uses UPnP devices.
---
# 102. DDoS Tools & Detection
## Popular DDoS Tools
* LOIC
* HOIC
* Trinoo
* TFN
* TFN2K
* Stacheldraht
## Detection Indicators
* High CPU usage
* Network congestion
* Huge spike in requests
* Large number of SYN packets
* Numerous half-open TCP connections
* High bandwidth utilization
* Slow application response
## Monitoring Tools
* Wireshark
* tcpdump
* NetFlow
* SIEM
* IDS/IPS
## Common Metrics
* Packets Per Second (PPS)
* Bits Per Second (bps)
* Requests Per Second (RPS)
* Concurrent Connections
---
# 103. DoS Prevention & Mitigation
## Best Mitigations
### Network Layer
* Firewalls
* ACLs
* Rate Limiting
* Geo-blocking
* Ingress/Egress Filtering
### Application Layer
* CAPTCHA
* Web Application Firewall (WAF)
* CDN
* Reverse Proxy
* Load Balancer
### Infrastructure
* Redundant Servers
* Auto Scaling
* High Availability
* Anycast Routing
* Cloud DDoS Protection
## Rate Limiting
Limit requests per client.
## Blackholing vs Sinkholing
|Blackholing|Sinkholing|
|---|---|
|Drops all traffic|Redirects traffic for analysis|
|Fast protection|Useful for investigation|
## Defense strategy
Firewall —> IPS —> WAF —> CDN —> Load Balancer —> Application
---
---
# 104. Introduction to Session Hijacking
## What is a Session?
A session allows a web server to **remember a user** across multiple HTTP requests.
Without sessions:
* Login on every page
* No shopping carts
* No Gmail persistence
* No authenticated state
## Why Sessions Exist
HTTP is **stateless**. Every request is independent. Sessions maintain user state.
## Session Flow
```
User Login

↓

Server Authenticates

↓

Server Creates Session ID

↓

Browser Stores Cookie

↓

Every Request Sends Cookie

↓

Server Identifies User
```
## Components
|Component|Stored Where|
|---|---|
|Session|Server|
|Session ID|Browser Cookie|
---
# 105. Session Tokens & Cookies
## Session Token Requirements
* Random
* Unique
* Long
* Temporary
* Cryptographically Secure
## Cookie Attributes
|Attribute|Purpose|
|---|---|
|Secure|HTTPS Only|
|HttpOnly|Blocks JavaScript Access|
|SameSite|Helps Prevent CSRF|
## Cookie Types
|Type|Lifetime|
|---|---|
|Session Cookie|Browser Session|
|Persistent Cookie|Fixed Expiration|
---
# 106. Types of Session Hijacking
## Main Types
|Attack|Description|
|---|---|
|Session Sniffing|Capture Cookie from Network|
|Session Sidejacking|Reuse Stolen Cookie|
|Session Fixation|Victim Uses Attacker's Session ID|
|Session Prediction|Guess Weak Session IDs|
## Passive vs Active
|Passive|Active|
|---|---|
|Observe Traffic|Take over / participate in the session|
|Sniffing|Fixation / MITM / command injection|
## Network-Level vs Application-Level
|Network-Level|Application-Level|
|---|---|
|Hijack TCP/UDP session|Steal/use app session IDs|
|Sequence numbers, IP/port|HTTP cookies/tokens|
---
# 107. TCP Session Hijacking
## Definition
Taking over an **existing TCP connection** by injecting packets with valid sequence numbers.
## Session Hijacking Process (3 steps)
1. **Track** the connection (find an active session, IPs, ports)
2. **Desynchronize** the connection (disrupt sequence numbers)
3. **Inject** attacker's packets/commands into the session
## Sequence Numbers (exam focus)
* Each ACK **advances** the expected sequence number.
* The **TCP window size** sets the range of sequence numbers the host will accept.
* To inject successfully, the attacker's packet must carry a sequence number **inside that window**.
## Requirements
* Active TCP Session
* Correct Sequence Numbers
* IP Addresses
* TCP Ports
## Blind vs Non-Blind
|Blind|Non-Blind|
|---|---|
|Guess Sequence Numbers|Observe Traffic|
|Difficult|Easier|
## ⚠️ Spoofing vs Hijacking
|Spoofing|Hijacking|
|---|---|
|Pretend to be another source/identity|Take over an **already-established** session|
Spoofing can *help* a hijack, but they are **not** synonyms.
---
# 108. Session Hijacking Tools
## Common Tools
|Tool|Purpose|
|---|---|
|Wireshark|Packet Analysis|
|Burp Suite|Web Security Testing|
|Ettercap|MITM Testing|
|Bettercap|Modern MITM Framework|
|SSLStrip|Historical HTTPS Downgrade Demonstration|
## Cookie Theft Sources
* XSS
* Malware
* MITM
* Browser Compromise
* Physical Access
* Insecure HTTP
---
# 109. Detection & Countermeasures
## Detection Methods
* Impossible Travel
* Device Fingerprinting
* IP Changes
* Concurrent Sessions
* Behavioral Analytics
## Best Defenses
* HTTPS
* Secure Cookies
* HttpOnly
* SameSite
* Session Regeneration
* MFA
* Session Timeout
* Token Rotation
* Zero Trust
## Session Lifecycle
Login —> Authenticate —> Create Session —> Use Session —> Expire —> Destroy Session
## Secure Session Management
* Generate Random Tokens
* Regenerate After Login
* Short Session Lifetime
* Logout Properly
* Destroy Expired Sessions
* Reauthenticate Sensitive Actions
* Device Binding
* Continuous Authentication
---
---
# 110. IDS (Intrusion Detection System)
### Definition
A security device that **monitors network or host activity** and **generates alerts** when suspicious behavior is detected.
### Key Points
* Detects attacks
* Generates alerts
* Passive device
* Does **not** block traffic
### CEH Keywords
* Passive
* Monitoring
* Alert Generation
### NIDS vs HIDS
|NIDS (Network)|HIDS (Host)|
|---|---|
|Monitors network traffic|Monitors one host's activity|
|Placed at choke points / SPAN port|Installed on the endpoint|
|Sees traffic, not host internals|Sees files, logs, processes, registry|
---
# 111. IPS (Intrusion Prevention System)
### Definition
An inline security device that **detects and actively blocks malicious traffic**.
### Key Points
* Prevents attacks
* Drops malicious packets
* Inline deployment
* Stops threats before reaching the target
### CEH Keywords
* Inline
* Prevention
* Blocking
---
# 112. IDS Detection Methods
### Signature Detection
* Detects **known attacks**
* Fast
* Low false positives
* Cannot detect zero-days
### Anomaly Detection
* Detects **unknown attacks**
* Learns normal behavior
* Higher false positives
### Protocol Anomaly Detection
* Detects protocol violations
* Invalid headers
* Malformed packets
### 🧠 Mnemonic
**SAP**
**S** → Signature
**A** → Anomaly
**P** → Protocol
---
# 113. IDS Alert Types
|Actual Attack|Alert|Result|
|---|---|---|
|Yes|Yes|True Positive|
|No|Yes|False Positive|
|Yes|No|False Negative|
|No|No|True Negative|
---
# 114. Firewall Architecture
### Bastion Host
* Hardened public-facing system
### Screened Subnet
* Uses a **DMZ** between two security boundaries
### Multi-Homed Firewall
* Firewall with multiple network interfaces
### DMZ
* Hosts public servers
* Separates Internet from internal LAN
---
# 115. Firewall Technologies
### Types
* Packet Filtering Firewall
* Circuit-Level Gateway
* Application-Level Firewall
* Stateful Inspection Firewall
* Proxy Firewall
* NAT Firewall
* VPN Firewall
* Next-Generation Firewall (NGFW)
---
# 116. Firewall & IDS Identification Techniques
### Techniques
* Port Scanning
* Firewalking
* Banner Grabbing
### Purpose
Reconnaissance
Learn:
* Open ports
* Firewall rules
* Service versions
---
# 117. Evasion Techniques
### Methods
* IP Address Spoofing
* Source Routing
* Tiny Fragments
* Using IP instead of URL
* Anonymous Browsing
* Proxy Servers
### Goal
Avoid
* Detection
* Filtering
* Monitoring
---
# 118. Tunneling Techniques
Tunneling is the process of encapsulating one network protocol inside another protocol to bypass security controls such as firewalls, IDS/IPS, proxy servers, and network filtering devices.
**ICMP Tunneling uses Ping packets**
**ACK Tunneling uses TCP ACK packets**
**HTTP Tunneling uses HTTP/HTTPS traffic**
**Purpose: Hide one type of traffic inside another protocol.**
---
# 119. Honeypots
A honeypot is a deliberately deployed decoy system or service designed to attract attackers, monitor their activities, and collect intelligence without exposing production systems.
Organizations use honeypots to:
* Detect attackers early
* Study attack techniques
* Gather malware samples
* Delay attackers
* Divert attacks from production systems
|Type|Purpose|
|---|---|
|Production Honeypot|Detect attacks in operational environments|
|Research Honeypot|Collect attack intelligence|
|Low-Interaction Honeypot|Simulates limited services|
|High-Interaction Honeypot|Real operating system with extensive attacker interaction|
**Honeypot ≠ IDS**
* IDS monitors production traffic.
* Honeypot attracts attackers intentionally.
### Mnemonic
**"DRAMA"**
* **D**etect
* **R**esearch
* **A**nalyze
* **M**onitor
* **A**ttract
---
# 120. Countermeasures
### Best Practices
* Keep IDS/IPS signatures updated
* Apply security patches regularly
* Implement firewall rule reviews
* Disable unnecessary services
* Use encrypted protocols securely
* Monitor logs continuously
* Enable anomaly detection
* Restrict administrative privileges
* Implement Network Access Control (NAC)
* Use endpoint protection
* Apply network segmentation
* Perform regular vulnerability assessments
* Enforce least privilege
* Monitor DNS activity
* Detect tunneling attempts
### Mnemonic
**"PATCH"**
* **P**atch
* **A**udit
* **T**rain
* **C**onfigure securely
* **H**arden
---
# 121. Modern Enterprise Security
### Definition
Modern Enterprise Security is a layered security architecture that combines preventive, detective, and responsive security technologies to protect enterprise assets against modern cyber threats.
### Enterprise Stack
```
Internet

↓

NGFW (Next gen Firewall)

↓

IPS

↓

IDS

↓

Proxy

↓

SIEM

↓

Endpoint Protection

↓

Users
```
### Zero Trust Principles
* Never trust
* Always verify
* Least privilege
* Continuous authentication
* Continuous monitoring
### Goals
* Reduce attack surface
* Prevent lateral movement
* Improve visibility
* Detect attacks rapidly
* Respond quickly
* Protect cloud and on-premises resources
---
---
# 122. Web Server Concepts
## Definition
A **Web Server** is software (or hardware running it) that receives **HTTP/HTTPS** requests from clients and delivers web content such as web pages, images, APIs, and downloadable files.
## Components
|Component|Purpose|
|---|---|
|Document Root|Stores website files (HTML, CSS, JS, Images)|
|Server Root|Stores configuration files and executables|
|Virtual Document Tree|Maps URLs to physical directories|
|Virtual Hosting|Hosts multiple websites on one server|
|Web Proxy|Intermediary between client and server|
## Workflow
Browser —> HTTP/HTTPS Request —> Web Server —> Static Content —> Application Server —> Database —> HTTP Response
**“DSVP”**
* Document Root
* Server Root
* Virtual Hosting
* Proxy
---
# 123. Web Server Security Issues
## Definition
Weaknesses or misconfigurations allowing attackers to compromise a web server.
## Common Security Issues
* Weak passwords
* Default credentials
* Unpatched software
* Improper permissions
* Directory listing
* SSL/TLS misconfiguration
* Information disclosure
* Weak authentication
---
# 124. Web Server Architecture
## Definition
The structure showing how web servers, application servers, and databases interact.
### Three-Tier Architecture
Client —> Web Server —> Application Server —> Database
## Architecture Types
|Type|Description|
|---|---|
|Single Tier|Rare|
|Two Tier|Client ↔ Database|
|Three Tier|Most common|
|Multi Tier|Enterprise architecture|
## Goals
* Scalability
* Security
* Performance
* Separation of duties
## Apache Architecture (modular)
Apache = HTTP core + loadable **modules**. Common modules:
* Authentication (`mod_auth*`)
* SSL/TLS (`mod_ssl`)
* URL rewriting (`mod_rewrite`)
* Proxy (`mod_proxy`)
#### Key idea: web-server functionality is **modular** — disable unneeded modules to shrink the attack surface. (IIS is the Windows counterpart.)
---
# 125. Web Server Attacks
## Definition
Attempts to compromise web servers through vulnerabilities or misconfigurations.
## Common Attacks
* Information Disclosure
* Directory Traversal
* Misconfiguration Exploitation
* Password Attacks
* DoS/DDoS
* Buffer Overflow
* Web Shell Upload
* Malware
## Methodology
```
Reconnaissance

↓

Footprinting

↓

Scanning

↓

Vulnerability Assessment

↓

Exploitation

↓

Privilege Escalation

↓

Maintaining Access

↓

Covering Tracks
```
## Goals
* Gain access
* Execute commands
* Install malware
* Steal data
* Deface website
---
# 126. Web Server Vulnerability Assessment
## Definition
Identifying vulnerabilities before exploitation.
## Assessment Areas
* Server Software
* Operating System
* SSL/TLS
* Configuration
* Authentication
* File Permissions
* Known CVEs
## Workflow
```
Identify Software

↓

Version

↓

Known CVEs

↓

Configuration Review

↓

Risk Rating

↓

Mitigation
```
---
# 127. Specific Web Server Attacks
|Attack|Description|
|---|---|
|DNS Server Hijacking|Alter DNS so users are sent to a malicious server|
|DNS Amplification|Use recursive DNS to flood a victim (DDoS)|
|Directory Traversal|`../../` to read files outside web root|
|Website Defacement|Change visible site content|
|Web Cache Poisoning|Inject malicious content into a shared cache|
|HTTP Response Splitting|Inject CR/LF to craft extra responses|
|SSH Brute Force|Guess SSH creds to open a tunnel|
|Server Misconfiguration|Exploit default/weak settings|
|Web Server Password Cracking|Recover admin creds|
## Server-Side Request Forgery (SSRF)
Trick the server into making requests to internal/unintended resources (e.g., cloud metadata `169.254.169.254`).
---
# 128. Web Server Attack Tools
|Tool|Purpose|
|---|---|
|Metasploit|Exploitation framework|
|Nikto|Web server vulnerability scanner|
|Nmap NSE (http-*)|Service/vuln detection|
|THC Hydra|Online password cracking|
|Wfuzz / DirBuster / Gobuster|Directory & file brute forcing|
|Burp Suite|Intercept / manipulate requests|
---
# 129. Web Server Footprinting / Banner Grabbing
## Goal
Identify server software, version, OS, and modules before attacking.
## Techniques & Tools
* `telnet <host> 80` then `HEAD / HTTP/1.0`
* `curl -I <url>` (dump headers)
* Netcat (`nc`)
* Nmap: `-sV`, `--script=http-server-header`
* **Whatweb / Wappalyzer** → tech fingerprinting
## Key Response Headers
* `Server:` → web server + version
* `X-Powered-By:` → backend (PHP, ASP.NET)
* `Set-Cookie:` → session tech (JSESSIONID, PHPSESSID)
---
# 130. Web Server Password Cracking
## Definition
Recovering valid credentials using password attack techniques.
## Password Attacks
|Attack|Description|
|---|---|
|Brute Force|Every combination|
|Dictionary|Wordlist|
|Hybrid|Dictionary + modifications|
|Credential Stuffing|Leaked credentials|
|Password Spraying|One password, many users|
## Countermeasures
* Strong passwords
* MFA
* Rate limiting
* Account lockout
* Monitoring
---
# 131. Web Server Misconfiguration
## Definition
Insecure server settings that expose the server without requiring software vulnerabilities.
## Common Misconfigurations
* Default settings
* Directory Listing
* Improper Permissions
* Backup Files
* Server Banner Disclosure
* Verbose Error Pages
* Unnecessary Services
* Weak SSL/TLS
---
# 132. Web Server Hardening
## Definition
Strengthening server security by reducing the attack surface and applying secure configurations.
## Hardening Checklist
* Patch software
* Remove unnecessary services
* Disable directory listing
* Secure permissions
* Hide server information
* Configure SSL/TLS
* Strong authentication
* Logging
* WAF
* IDS/IPS
---
# 133. Web Server Attack Countermeasures
## Definition
Security controls implemented to prevent, detect, and respond to web server attacks.
## Major Countermeasures
* Patch Management
* Secure Configuration
* Strong Authentication
* Web Application Firewall (WAF)
* IDS/IPS
* SSL/TLS
* Logging & Monitoring
* Network Segmentation (DMZ)
* Regular Security Assessments
---
---
# **134. Web Application Concepts**
## Definition
A **web application** is software hosted on a web server and accessed through a browser using HTTP/HTTPS.
Web Server.
### Components
|Component|Function|
|---|---|
|Client|Sends requests / displays responses|
|Web Server|Handles HTTP/HTTPS and static content|
|Application Server|Executes business logic|
|Database|Stores persistent information|
### Three-Tier Architecture
|Layer|Function|
|---|---|
|Presentation|User interface (client)|
|Application|Business logic|
|Data|Database/data storage|
## Vulnerability Stack (layers of attack surface)
A web app sits on a stack; a weakness in **any** layer can be the entry point:
```
Custom Web App / Business Logic   (top)
Third-Party Components
Web Server
Database
Operating System
Network (router/switch)
Security Controls
```
## ⚠️ Client-Side vs Server-Side Validation
Client-side checks (JavaScript, hidden fields, disabled buttons) run in the **user's browser** and can be bypassed with a proxy. **Security-critical validation and authorization must be enforced server-side.**
---
# **135. Web Services**
## Definition
A **web service** allows applications to communicate over a network, even when they use different platforms or programming languages. 
## Three Roles
1. **Service Provider**
1. **Service Requester**
1. **Service Registry**
## Three Operations
* **Publish** → Provider publishes service information.
* **Find** → Requester discovers the service.
* **Bind** → Requester connects to/invokes the service.
## SOAP
* XML-based
* Protocol
* Structured messaging
* Common in enterprise environments
## REST
* Architectural style
* Uses HTTP concepts
* Commonly uses JSON
* Uses methods such as GET, POST, PUT, DELETE
## Important Components
### UDDI
Service discovery/registry.
### WSDL
Describes the web service.
### WS-Security
Provides security mechanisms for SOAP messaging.
---
# **136. Broken Access Control**
## Definition
Occurs when an application fails to correctly enforce what authenticated users are allowed to access or modify.
### Parameter Tampering
Manipulating parameters to access another object.
### Force Browsing
Directly requesting restricted resources such as administrative pages.
### Privilege Escalation
Normal user → administrative functionality.
### Hidden Field Manipulation
Manipulating security-sensitive values stored in hidden form fields.
### JWT / Cookie Manipulation
Manipulating client-held authentication/session information.
### API Authorization Failures
Sensitive APIs must enforce authorization on **every operation**, not just the login endpoint.
## CORS
Improper CORS configuration may allow APIs to be accessed from unauthorized origins.
## Least Privilege
Users should have only the permissions required for their legitimate activities.
---
# **137. Cryptographic Failures / Sensitive Data Exposure**
## Definition
Occurs when sensitive information is inadequately protected due to weak or improper cryptographic mechanisms.
## Major Weaknesses
* Weak cryptography
* Poor key protection
* Weak/poor IV handling
* Deprecated algorithms
* Insecure storage
* Information leakage
## Important Algorithms
The material specifically identifies:
* **MD5**
* **SHA-1**
as deprecated for secure cryptographic use. 
It also identifies **PKCS #1 v1.5 padding** as deprecated.
### Hashing ≠ Encryption
|Hashing|Encryption|
|---|---|
|One-way|Reversible with key|
|Integrity / password use|Confidentiality|
|SHA-256 etc.|AES/RSA etc.|
---
# **138. Security Misconfiguration**
## Definition
Security Misconfiguration occurs when application components are improperly configured, exposing weaknesses.
## Major Causes
* Missing hardening
* Default credentials
* Unnecessary services
* Unpatched software
* Poor error handling
* Weak TLS configuration
* Unvalidated input
* Parameter tampering
* XXE
* Legacy software
---
# **139. Identification and Authentication Failures / Broken Authentication**
## Definition
Weaknesses in identification, authentication, password management, and session management that allow user impersonation or session compromise.
## Major Attack Areas
* Session IDs
* Password management
* Logout
* Session timeout
* Remember Me
* Secret questions
* Account updates
* Exposed accounts
## Session ID in URL
Exposing session IDs in URLs can enable session-related attacks. 
## Password Exploitation
Weak hashing or insecure password storage can expose credentials.
## Timeout Exploitation
Excessively long sessions can allow attackers to reuse active sessions.
---
---

# **140. Injection**
## Definition
Untrusted input is sent to an interpreter as part of a command or query, letting an attacker alter the intended logic.
## Common Types
|Injection|Interpreter|
|---|---|
|SQL Injection|Database|
|Command Injection|OS Shell|
|LDAP Injection|Directory Service|
|XPath Injection|XML Query|
|CRLF Injection|Headers/Logs|
|Server-Side Template Injection (SSTI)|Template Engine|
## Command Injection Example
`127.0.0.1; cat /etc/passwd` → chains an OS command onto expected input.
## Defense
* Parameterized queries / prepared statements
* Input validation (allow-list)
* Least-privilege DB accounts
* Escape special characters / use safe APIs
---
# **141. Cross-Site Scripting (XSS)**
## Definition
Injecting malicious **JavaScript** into a web page so it runs in another user's browser.
## Types
|Type|Where Payload Lives|
|---|---|
|Stored (Persistent)|Saved on server (DB, comment)|
|Reflected (Non-persistent)|In the request/URL, echoed back|
|DOM-Based|Client-side JS modifies the DOM|
## Impact
* Session/cookie theft
* Keylogging
* Defacement
* Redirect / phishing
* Browser exploitation (BeEF)
## Defense
* Output encoding (context-aware)
* Input validation
* `HttpOnly` cookies
* **Content Security Policy (CSP)**
---
# **142. CSRF, SSRF, IDOR & Other Web App Attacks**
## CSRF (Cross-Site Request Forgery)
Tricks a **logged-in victim's browser** into sending an unwanted authenticated request.
* Exploits trust the **site has in the user**.
* Defense: CSRF tokens, `SameSite` cookies, re-authentication.
## SSRF (Server-Side Request Forgery)
Force the **server** to make requests to internal systems or cloud metadata (`169.254.169.254`).
* Defense: allow-list outbound hosts, block internal ranges, disable unused URL schemes.
## IDOR (Insecure Direct Object Reference)
Change a reference (`id=123` → `id=124`) to access another user's data. A form of broken access control.
## File Inclusion
|Type|Meaning|
|---|---|
|LFI|Local File Inclusion — include server files (`../../etc/passwd`)|
|RFI|Remote File Inclusion — include attacker-hosted code|
## Directory / Path Traversal
`../` sequences to escape the web root and read arbitrary files.
## XXE (XML External Entity)
Malicious XML entity reads local files or triggers SSRF. Defense: disable external entity (DTD) processing.
## Insecure Deserialization
Attacker-controlled serialized objects → remote code execution / privilege abuse.
## Clickjacking
Invisible iframe over a legit button. Defense: `X-Frame-Options`, CSP `frame-ancestors`.
## CSRF vs XSS
|CSRF|XSS|
|---|---|
|Abuses site's trust in user|Abuses user's trust in site|
|No script injection needed|Injects script|
|Forces a request|Runs code in browser|
---
# **143. Remaining OWASP Top 10 (2021) Categories**
## Insecure Design
Missing/ineffective security controls by design (not just a bug). Fix with threat modeling & secure design patterns.
## Vulnerable and Outdated Components
Using libraries/frameworks with known CVEs. Fix with SCA tools, patching, inventory (SBOM).
## Software and Data Integrity Failures
Trusting unverified updates, plugins, or CI/CD pipelines (supply chain). Fix with signing & integrity checks.
## Security Logging and Monitoring Failures
Attacks go undetected due to missing logs/alerts. Fix with centralized logging, SIEM, alerting.
## SSRF
(See section 142.) Listed as its own Top 10 item (A10).
---
# **144. OWASP Top 10 (2021) — Quick Reference**
|ID|Category|
|---|---|
|A01|Broken Access Control|
|A02|Cryptographic Failures|
|A03|Injection (incl. XSS)|
|A04|Insecure Design|
|A05|Security Misconfiguration|
|A06|Vulnerable & Outdated Components|
|A07|Identification & Authentication Failures|
|A08|Software & Data Integrity Failures|
|A09|Security Logging & Monitoring Failures|
|A10|Server-Side Request Forgery (SSRF)|
---
# **145. Web Application Hacking Methodology & Tools**
## Methodology
Footprint Web Infrastructure → Analyze Web Apps → Bypass Client-Side Controls → Attack Authentication → Attack Authorization → Attack Session Management → Attack Input Validation (Injection/XSS) → Attack Logic Flaws → Attack Database/Shared Environment
## WAF Detection & Evasion
* Detect: WAFW00F
* Evade: encoding, case variation, comments, HTTP parameter pollution
## Key Tools
|Tool|Purpose|
|---|---|
|Burp Suite|Intercepting proxy / all-in-one|
|OWASP ZAP|Open-source proxy & scanner|
|Nikto|Web server scanning|
|Wfuzz / ffuf / Gobuster|Fuzzing & dir brute force|
|sqlmap|Automated SQL injection|
|BeEF|Browser exploitation (XSS)|
## Countermeasures (Summary)
* Input validation + output encoding
* Parameterized queries
* Strong auth + MFA + secure sessions
* WAF, security headers (CSP, HSTS, X-Frame-Options)
* Patch components, least privilege, logging & monitoring
#### ⚠️ A WAF inspects HTTP(S) and blocks known patterns, but it is **not** a substitute for secure code — weak rules can be evaded. Treat it as a supplemental control.
---
---
# 146. SQL Injection — Concepts (Module 15)
## Definition
SQL injection happens when attacker-controlled input is interpreted as part of the **SQL query structure** because the app fails to separate **data from executable query logic** — letting the attacker read, modify, or destroy data or bypass authentication.
## Why It Happens
String concatenation of user input into SQL is the classic cause, but the core weakness is **data being treated as code** (fixed by parameterization, not just filtering).
## Classic Auth Bypass
`' OR '1'='1' -- ` → makes the WHERE clause always true.
## Impact
* Authentication bypass
* Data theft / modification / deletion
* Read/write files, command execution (if DB allows)
* Full DB (and sometimes host) compromise
---
# 147. Types of SQL Injection
## Main Categories
|Type|Description|
|---|---|
|In-Band|Results returned in the same channel|
|Error-Based|Forces DB errors that leak data|
|UNION-Based|`UNION SELECT` to append attacker data|
|Blind (Inferential)|No data returned; infer from behavior|
|Boolean-Based Blind|True/false page differences|
|Time-Based Blind|`SLEEP()`/`WAITFOR DELAY` timing|
|Out-of-Band|Data exfil via DNS/HTTP (separate channel)|
## Second-Order SQLi
Payload stored first, executes later when used by another query.
---
# 148. SQL Injection Methodology & Tools
## Methodology
Identify Input → Detect SQLi → Determine DB Type → Extract Schema (DBs → Tables → Columns) → Extract Data → Escalate (file/OS access)
## Fingerprinting Tricks
* MySQL comment: `-- `, `#`, `/* */`
* `@@version`, `version()`, `information_schema`
## Key Tool — sqlmap
`sqlmap -u "http://site/page?id=1" --dbs` (enumerate databases)
`--tables -D <db>` → `--dump -T <table>`
## Other Tools
* Burp Suite (manual + scanner)
* Havij (legacy GUI)
## Evasion
* Inline comments `/**/`
* Case toggling, URL/hex encoding
* `OR 1=1` variants, whitespace alternatives
---
# 149. SQL Injection Countermeasures
|Defense|Why|
|---|---|
|Prepared Statements / Parameterized Queries|**Best defense** — data never treated as code|
|Stored Procedures (safely written)|Separates query logic|
|Input Validation (allow-list)|Reject bad input|
|Least Privilege DB account|Limit damage|
|WAF|Filter known payloads|
|Error Handling|Hide DB errors from users|
|Disable dangerous features|e.g. `xp_cmdshell`|
---
---
# 150. Wireless Concepts & Standards (Module 16)
## Terminology
|Term|Meaning|
|---|---|
|SSID|Network name|
|BSSID|AP's MAC address|
|Access Point (AP)|Connects wireless clients to LAN|
|Association|Client joins an AP|
|Hotspot|Public Wi-Fi area|
|GHz Bands|2.4 GHz (range) / 5 GHz (speed)|
## 802.11 Standards
|Standard|Band|Max Speed|
|---|---|---|
|802.11a|5 GHz|54 Mbps|
|802.11b|2.4 GHz|11 Mbps|
|802.11g|2.4 GHz|54 Mbps|
|802.11n (Wi-Fi 4)|2.4/5 GHz|600 Mbps|
|802.11ac (Wi-Fi 5)|5 GHz|~1.3+ Gbps|
|802.11ax (Wi-Fi 6)|2.4/5/6 GHz|~9.6 Gbps|
## Antenna Types
Omnidirectional, Directional, Yagi, Parabolic Grid, Dipole.
## Other 802.15/802.16 Standards
|Standard|Technology|
|---|---|
|802.15.1|Bluetooth|
|802.15.4|Low-rate PAN (Zigbee)|
|802.15.5|Wireless mesh|
|802.16|WiMAX|
## ⚠️ Association vs Authentication
|Association|Authentication|
|---|---|
|Client **connects/associates** with an AP|AP/network **verifies** the client before granting access|
Not synonyms — association is the link; authentication is identity proof.
## WPA/WPA2 Authentication Modes
|Mode|How|
|---|---|
|Personal (PSK)|Shared pre-shared key|
|Enterprise (802.1X)|Central auth via RADIUS/EAP, per-user credentials|
---
# 151. Wireless Encryption
|Protocol|Encryption|Weakness|
|---|---|---|
|WEP|RC4 + 24-bit IV + CRC-32 ICV|Broken — IV reuse, crackable in minutes|
|WPA|TKIP + RC4|Better, still weak (TKIP)|
|WPA2|AES-CCMP|Strong **if** strong PSK/config; KRACK, weak-PSK risk|
|WPA3|SAE (Dragonfly)|Modern; resists offline password cracking|
## WEP Structure (high-yield)
* **RC4** stream cipher
* **24-bit IV** (too small → reuse)
* **CRC-32 ICV** integrity check (weak)
* Poor key management / IV reuse = core flaw
## Know the Security Mechanism, Not Just "Strong/Weak"
* **WPA** → TKIP/RC4
* **WPA2** → AES-CCMP
* **WPA3-Personal** → **SAE**, resists offline dictionary attacks
* **WPA3-Enterprise** → stronger 192-bit enterprise suite
#### ⚠️ "WPA2 = strong" and "WPA3 = forward secrecy" are incomplete. WPA2 security still depends on PSK strength/config; WPA3's headline is **SAE + offline-attack resistance** (forward secrecy is one part).
## Key Facts
* **WEP** uses a weak **24-bit IV** → the core flaw.
* **WPA2-PSK** handshakes can be captured and brute-forced offline.
* **WPA3** replaces the PSK handshake with **SAE**, resisting offline cracking.
---
# 152. Wireless Threats & Attacks
|Attack|Description|
|---|---|
|Rogue AP|Unauthorized AP on the network|
|Evil Twin|Fake AP mimicking a legit SSID|
|Honeyspot / MITM|Lure clients to attacker AP|
|Jamming|RF denial of service|
|Deauthentication|Forged deauth frames kick clients off|
|KRACK|Key reinstallation attack on WPA2|
|WPS PIN Attack|Brute-force 8-digit WPS PIN (Reaver)|
|aLTEr / Karma|Target client probe behavior|
## Wireless Threat Categories (scenario grouping)
|Category|Example attacks|
|---|---|
|Access-Control|Rogue AP, MAC spoofing, unauthorized association|
|Integrity|Frame injection, data tampering|
|Confidentiality|Eavesdropping, traffic analysis, evil twin|
|Availability|Jamming, deauth flood, beacon flood|
|Authentication|PSK cracking, identity theft, shared-key guessing|
## More Attack Names (recognition)
Misconfigured AP · SSID broadcast abuse · ad-hoc connection attack · promiscuous/mis-association client · unauthorized association · beacon flood · AP theft · EAP-failure · authentication flood · ARP poisoning · power-saving attack · TKIP MIC exploit.
## Authentication Attacks
WPA-PSK cracking · LEAP cracking · VPN/domain login cracking · key reinstallation (KRACK) · identity theft · shared-key guessing · application-login theft.
## Deauth → Handshake Capture
Deauth client → client reconnects → capture 4-way handshake → crack PSK offline.
---
# 153. Wireless Hacking Methodology & Tools
## Methodology
Wi-Fi Discovery → GPS Mapping (wardriving) → Traffic Analysis → Launch Attack (deauth) → Capture Handshake → Crack Key → Compromise
## Aircrack-ng Suite
|Tool|Purpose|
|---|---|
|airmon-ng|Enable monitor mode|
|airodump-ng|Capture packets / handshakes|
|aireplay-ng|Inject / deauth|
|aircrack-ng|Crack WEP/WPA keys|
## Other Tools
* Kismet (detection)
* Wifite (automation)
* Reaver / Bully (WPS)
* Wireshark (analysis)
* Fern / Wifiphisher (evil twin)
## WPS Discovery
`wash -i <mon-iface>` lists **WPS-enabled APs** (channel, output options, survey mode) → candidates for Reaver/Bully PIN attacks.
## War Driving / War Chalking
* **War driving** → moving around mapping Wi-Fi (often with GPS).
* **War chalking** → marking symbols (in chalk) to advertise a discovered network's SSID/type/security. Know the concept + symbols.
## Bluetooth Attacks
|Attack|Meaning|
|---|---|
|Bluesmacking|Bluetooth DoS (oversized ping)|
|Bluejacking|Send unsolicited messages|
|Bluesniffing|Discovery/sniffing of devices|
|Bluesnarfing / Bluescarfing|Steal data from the device|
|Bluebugging|Take control of device|
|BlueBorne|RCE over Bluetooth|
---
# 154. Wireless Countermeasures
* Use **WPA3** (or WPA2-AES with strong, long PSK)
* Disable **WPS**
* Disable SSID-based trust; use **802.1X / EAP** (enterprise)
* Wireless IDS/IPS (detect rogue/evil twin)
* MAC filtering (weak, supplemental only — **MACs are easily sniffed and spoofed**, so it is an administrative control, not real security)
* Reduce signal leakage / AP placement
* Change default admin creds & firmware updates
* VPN over untrusted Wi-Fi
---
---
# 155. Mobile Platform Attack Vectors (Module 17)
## OWASP Mobile Top 10 (themes)
Improper Credential Usage, Inadequate Supply Chain Security, Insecure Auth/Authorization, Insufficient Input/Output Validation, Insecure Communication, Inadequate Privacy, Insufficient Binary Protection, Security Misconfiguration, Insecure Data Storage, Insufficient Cryptography.
## Anatomy of a Mobile Attack — 3 Points
1. **The device** (OS, apps, storage)
2. **The network** (Wi-Fi, carrier, MITM)
3. **The data center / cloud** (backend, APIs)
A compromise can chain across all three.
## Common Vectors
* Malicious apps / repackaged apps
* SMS phishing (smishing)
* Insecure data storage
* Insecure communication (no TLS / weak pinning)
* Excessive permissions
* Jailbreak / root exposure
## App-Store Security Risks
Insufficient vetting · malicious/repackaged apps · third-party app stores · apps requesting excessive permissions · malicious updates / supply-chain issues.
## App Sandboxing
Each app is isolated from others' data/resources. A **vulnerable sandbox or sandbox escape** greatly increases a malicious app's impact.
## Network-Based Mobile Attacks
Open/weak Wi-Fi · rogue AP · sniffing · MITM · session hijacking · DNS poisoning · SSLStrip · fake SSL certificates.
## SMS Phishing (Smishing) — why it works
High open/read rates, short messages, urgency, shortened URLs, few security cues, easy to impersonate trusted brands. (**Mobile spam** = unsolicited SMS/MMS/IM with malicious links/attachments.)
---
# 156. Android Hacking
## Architecture (top→bottom)
Applications → Application Framework → Libraries + Android Runtime (ART) → Linux Kernel
## Key Points
* Apps are **APK** files; code often in **DEX** (Dalvik/ART).
* **Rooting** = gaining superuser (su) on Android.
* Sideloading unknown APKs is a major risk.
## Android Attack Concepts (recognition)
Weak/no passcode · rooting · data caching · insecure password/data access · carrier-loaded (bloatware) apps · untrusted code · weak update/security controls · excessive permissions.
## Tools
|Tool|Purpose|
|---|---|
|ADB|Android Debug Bridge (device control)|
|Drozer|Attack surface analysis|
|apktool|Decompile/rebuild APK|
|MobSF|Static & dynamic app analysis|
|zANTI / Metasploit (msfvenom)|Payloads|
---
# 157. iOS Hacking
## Key Points
* **Jailbreaking** removes Apple's restrictions (adds root/sideloading).
* Sandboxed apps; signed via App Store.
## iOS Attack Concepts (recognition)
Jailbreaking · data caching · weak protected credential/data storage · carrier/preinstalled apps · untrusted user-generated code · device-management weaknesses.
## Jailbreak Types
|Type|Persists Reboot?|Notes|
|---|---|---|
|Tethered|No|Needs PC each boot|
|Semi-Tethered|Partial|Boots, but jailbreak needs re-run|
|Untethered|Yes|Survives reboot fully|
|Semi-Untethered|Partial|Re-run via on-device app|
## Tools
checkra1n, unc0ver, palera1n, Cydia.
---
# 158. Mobile Management & Countermeasures
## MDM / BYOD
* **MDM** (Mobile Device Management) → enforce policy, remote wipe, encryption.
* **BYOD** risks → data leakage, mixing personal/corporate data.
* **Containerization** → separate work data from personal.
## Countermeasures
* No jailbreak/root; keep OS & apps patched
* Install apps only from official stores
* Strong screen lock + device encryption
* Remote wipe / find my device
* VPN + certificate pinning
* Least-privilege app permissions
* App vetting / MAM
---
---
# 159. IoT Concepts (Module 18)
## Definition
Network of physical "smart" devices with sensors/software that collect and exchange data.
## IoT Architecture Layers
Edge/Device → Communication/Network → Middleware/Cloud → Application
## Communication Protocols
|Protocol|Use|
|---|---|
|MQTT|Lightweight pub/sub messaging|
|CoAP|Constrained REST-like|
|Zigbee / Z-Wave|Low-power mesh|
|BLE|Bluetooth Low Energy|
|LoRaWAN|Long range, low power|
### More IoT Protocols (recognition)
NFC · Wi-Fi / Wi-Fi Direct · Thread · ANT · 6LoWPAN · Sigfox · NB-IoT · VSAT · Cellular · LWM2M · XMPP · Ethernet · PLC.
## IoT Operating Systems (recognition)
Windows 10 IoT · Amazon FreeRTOS · Fuchsia · RIOT · Ubuntu Core · ARM mbed OS · Zephyr · Embedded Linux · NuttX · Integrity RTOS · Apache Mynewt · Tizen.
## IoT Communication Models
|Model|Flow|
|---|---|
|Device-to-Device|Devices talk directly|
|Device-to-Cloud|Device → cloud service|
|Device-to-Gateway|Device → local gateway → cloud|
|Back-End Data-Sharing|Cloud data shared with 3rd parties|
## IoT Challenges
Interoperability · weak vendor support · hard-to-update firmware · poor physical security · resource/scalability limits · power constraints · compliance · legacy integration · huge unstructured data.
---
# 160. IoT Threats & OWASP IoT Top 10
## OWASP IoT Top 10 (exact module wording)
1. Weak, Guessable, or Hardcoded Passwords
2. Insecure Network Services
3. Insecure Ecosystem Interfaces
4. Lack of Secure Update Mechanisms
5. Use of Insecure or Outdated Components
6. Insufficient Privacy Protection
7. Insecure Data Transfer and Storage
8. Lack of Device Management
9. Insecure Default Settings
10. Lack of Physical Hardening
## IoT Attack Surface Areas
Ecosystem · device memory · firmware · network services · device interfaces · cloud web interface · local data storage · mobile app · authentication/authorization · third-party/vendor interfaces · hardware/sensors · network traffic/privacy.
## Security Problems by Layer
Application, network, mobile, cloud, and device layers all show recurring issues: weak auth, no auto-updates, poor encryption, insecure storage, weak comms controls, poor device management.
## Notable
* **Mirai botnet** → infected IoT via default creds, launched massive DDoS.
## IoT Hacking Methodology
Information Gathering → Vulnerability Scanning → Launch Attacks → Gain Access → Maintain Access
## Tools
Shodan (find exposed devices), Nmap, Firmware analysis (Firmwalker, Binwalk), Multiping, RFCrack.
---
# 161. OT (Operational Technology) Hacking
## Definition
Hardware/software that controls **physical industrial processes** (power, water, manufacturing).
## Key Terms
|Term|Meaning|
|---|---|
|ICS|Industrial Control Systems|
|SCADA|Supervisory Control and Data Acquisition|
|PLC|Programmable Logic Controller|
|HMI|Human-Machine Interface|
|RTU|Remote Terminal Unit|
|DCS|Distributed Control System|
## Purdue Model
Levels 0–5: Physical Process → Control → Supervisory → Site Operations (MES) → Enterprise/IT → Internet.
## Common Protocols
Modbus, DNP3, PROFINET, OPC — often **no authentication/encryption**.
## Notable Attack
**Stuxnet** → worm that sabotaged PLCs (centrifuges).
## Countermeasures
* **Network segmentation / air-gap**, IT/OT separation (zones & conduits, IEC 62443)
* Disable unused services, strong auth
* Monitor with OT-aware IDS
* Patch carefully (change control), physical security
---
---
# 162. Cloud Computing Concepts (Module 19)
## Service Models
|Model|You Manage|Example|
|---|---|---|
|IaaS|OS, apps, data|AWS EC2|
|PaaS|Apps, data|App Engine, Heroku|
|SaaS|Just use it|Gmail, Office 365|
## Deployment Models
Public · Private · Hybrid · Community · **Multi-Cloud** · Distributed cloud · Poly cloud.
## Cloud Actors / Roles (NIST)
|Role|Does|
|---|---|
|Cloud Consumer|Uses the service|
|Cloud Provider|Delivers the service|
|Cloud Carrier|Connectivity/transport between them|
|Cloud Auditor|Independent assessment/audit|
|Cloud Broker|Manages use/performance/delivery between consumer & provider|
## Expanded Service Models
Beyond IaaS/PaaS/SaaS: **IDaaS** (identity), **SECaaS** (security), **CaaS** (container), **FaaS** (function/serverless), **FWaaS** (firewall), **DaaS** (desktop/data), **MBaaS** (mobile backend), **XaaS** (anything). Core exam idea: **how much the provider manages vs the customer.**
## Key Characteristics (NIST)
On-demand self-service, broad network access, resource pooling, rapid elasticity, measured service.
## Responsibility
**Shared Responsibility Model** → provider secures "of the cloud" (infrastructure); customer secures "in the cloud" (data, config, access).
#### ⚠️ The split **shifts by service model**: customer carries most in **IaaS**, progressively less infra in **PaaS/SaaS** — but always owns its own **data, identities, and configuration**.
---
# 163. Cloud Technologies & Containers
## Virtualization vs Containers
|VM|Container|
|---|---|
|Full OS per VM|Shares host kernel|
|Hypervisor|Container engine (Docker)|
|Heavier|Lightweight/fast|
## Orchestration
* **Kubernetes** → manage containers at scale (pods, nodes, API server, etcd).
## Serverless
Run code without managing servers (AWS Lambda) — attack surface shifts to functions/permissions.
## Cloud-Native Concepts
Microservices, CI/CD, IaC (Terraform), API-driven.
## OWASP Kubernetes Top 10 (themes)
Insecure workload configs · supply-chain vulns · overly permissive RBAC · no centralized policy · poor logging/monitoring · broken auth · missing network segmentation · secrets-management failures · misconfigured cluster components · outdated K8s components.
## OWASP Serverless Top 10 (themes)
Injection · broken auth · sensitive data exposure · XXE · broken access control · security misconfiguration · XSS · insecure deserialization · vulnerable components · insufficient logging/monitoring.
---
# 164. Cloud Threats & Attacks
|Threat/Attack|Description|
|---|---|
|Misconfiguration|Public S3 buckets, open ports (top cause)|
|Account Hijacking|Stolen cloud credentials|
|Insecure APIs|Weak auth on cloud APIs|
|Data Breach|Exposed storage/DB|
|Side-Channel|Shared tenancy leakage|
|Cryptojacking|Abuse cloud compute to mine crypto|
|Container Escape|Break out of container to host|
|SSRF → Metadata|Steal cloud IAM creds via `169.254.169.254`|
|Privilege Escalation|Over-permissive IAM roles|
|Service Hijacking|Via social engineering or network sniffing|
|Wrapping Attack|Tamper with a SOAP message so a malicious request is processed as legitimate|
|Man-in-the-Cloud (MITC)|Steal sync tokens → hijack cloud account without a password|
|Side-Channel / Cross-Guest|Malicious VM exploits **shared physical resources** to infer another tenant's data (timing/cache)|
## OWASP Top 10 Cloud Risks (themes)
Accountability/data ownership · identity federation · compliance · business continuity · user privacy/secondary use · service & data integration · multi-tenancy/physical security · incident/forensic support · infrastructure security · non-production environment exposure.
## Cloud Attack Tools
Nimbostratus, Trufflehog (secrets), ScoutSuite, Prowler, Pacu (AWS exploitation), S3Scanner.
---
# 165. Cloud Security & Countermeasures
* **Harden IAM** → least privilege, MFA, no root keys, rotate credentials
* Fix misconfigurations → CSPM tools, block public storage by default
* Encrypt data at rest & in transit; manage keys (KMS/HSM)
* Secure APIs → auth, rate limiting, logging
* **CASB** → visibility/control over cloud use
* Monitoring/logging → CloudTrail, GuardDuty, SIEM
* Container security → image scanning, runtime protection, no privileged containers
* Zero Trust + network segmentation
---
---
# 166. Cryptography Concepts (Module 20)
## Goals
Confidentiality, Integrity, Authentication, Non-Repudiation.
## Symmetric vs Asymmetric
|Symmetric|Asymmetric|
|---|---|
|One shared key|Public + Private key pair|
|Fast|Slow|
|Key distribution problem|Solves key distribution|
|AES, DES, 3DES, RC4, Blowfish|RSA, ECC, DSA, Diffie-Hellman|
## Hybrid Approach
Asymmetric exchanges a symmetric **session key**; symmetric encrypts the bulk data (e.g., TLS).
---
# 167. Symmetric & Asymmetric Algorithms
#### 🎯 Exam gold: for any algorithm know **(1) key length** and **(2) block vs stream**.
## Symmetric Algorithms (key + type)
|Algorithm|Type|Key / Block facts|
|---|---|---|
|DES|Block|56-bit key — obsolete/weak|
|3DES|Block|168-bit (classic) — slow, legacy|
|AES|Block|128/192/256-bit key; 128-bit block (Rijndael)|
|IDEA|Block|128-bit key|
|Blowfish|Block|64-bit block; 32–448-bit key|
|Twofish|Block|up to 256-bit key|
|RC2|Block|variable key|
|RC4|**Stream**|variable key — legacy/insecure|
|RC5|Block|variable block (32/64/128)|
|RC6|Block|128-bit block|
|CAST-128|Block|64-bit block; ≤128-bit key|
|CAST-256|Block|128-bit block; ≤256-bit key|
|GOST|Block|64-bit block; 256-bit key|
|Serpent / Camellia / TEA / Threefish|Block|CEHv13-listed block ciphers|
|ChaCha20 / Salsa20|**Stream**|256-bit key|
## Asymmetric Algorithms
|Algorithm|Based On / Use|
|---|---|
|RSA|Integer factorization — encrypt + sign|
|Diffie-Hellman|Key exchange (discrete log)|
|ECC|Elliptic curves — small keys, strong|
|DSA|Digital signatures|
|ElGamal|Discrete-log public-key|
## Block vs Stream
Block = fixed-size blocks (AES 128-bit); Stream = bit/byte at a time (RC4, ChaCha20).
---
# 168. Hashing & Integrity
## Definition
One-way function producing a fixed-length digest; used for integrity & password storage.
## Algorithms
|Hash|Output / Status|
|---|---|
|MD5|128-bit — broken (collisions)|
|SHA-1|160-bit — deprecated|
|SHA-2|SHA-256/512 — secure|
|SHA-3|Keccak — modern|
## Related Concepts
* **Salt** → random value added before hashing (defeats rainbow tables).
* **HMAC** → hash + **shared secret key** → integrity + **message authentication** (proves the sender holds the shared key). ⚠️ It does **not** give public-key identity or non-repudiation.
* **Collision** → two inputs, same hash (MD5/SHA-1 weakness).
---
# 169. PKI & Digital Certificates
## PKI Components
|Component|Role|
|---|---|
|CA (Certification Authority)|Issues/signs certificates|
|RA (Registration Authority)|Verifies identity before issuance|
|VA (Validation Authority)|Confirms a cert's validity (revocation status)|
|Certificate|Binds public key to identity (X.509)|
|Certificate Management System|Stores/manages/distributes certs|
|End User|Uses/holds the certificate|
|CRL|Certificate Revocation List|
|OCSP|Online revocation checking|
## Digital Certificate Contents (X.509)
Subject (identity) · Issuer (CA) · Validity period · Serial number · Public key · Signature algorithm · CA's digital signature · Key-usage fields.
## CA-Signed vs Self-Signed
|CA-Signed|Self-Signed|
|---|---|
|Trust via a trusted CA chain|Signed by itself|
|Browsers trust it|No automatic third-party trust (warnings)|
## Digital Signature
Created with the **signer's private key**, verified with the **public key** → integrity + authentication + non-repudiation.
#### ⚠️ "Encrypt the hash with the private key" is a **teaching simplification**. It's true for RSA-style signatures but not a literal description of every scheme (e.g. DSA/ECDSA). Memorize: **private key → sign, public key → verify.**
## Encryption vs Signature (asymmetric)
|Goal|Key Used|
|---|---|
|Confidentiality|Encrypt with recipient's **public** key|
|Signature|Sign with sender's **private** key|
## SSL/TLS
TLS handshake authenticates server (cert) and negotiates a session key. HTTPS = HTTP over TLS → **confidentiality + integrity + server authentication** (not just "encryption"). Use **TLS 1.2/1.3**; SSL and TLS 1.0/1.1 are deprecated.
## Applications of Cryptography
Digital signatures · SSL/TLS · PGP · email encryption · disk encryption · blockchain.
---
# 170. Cryptanalysis & Crypto Attacks
|Attack|Description|
|---|---|
|Brute Force|Try all keys|
|Dictionary|Common values/passwords|
|Known-Plaintext|Have plaintext + ciphertext|
|Chosen-Plaintext|Choose plaintext to encrypt|
|Chosen-Ciphertext|Choose ciphertext to decrypt|
|Birthday Attack|Exploit hash collisions (probability)|
|Side-Channel|Timing, power, EM leakage|
|Meet-in-the-Middle|Against double encryption|
|Rainbow Table|Precomputed hashes (defeated by salt)|
|Padding Oracle|Exploit padding error responses|
|DUHK / FREAK / POODLE / DROWN|Known TLS/SSL downgrade & RNG attacks|
## Cryptanalysis Methods
|Method|Goal|
|---|---|
|Linear|Find linear approximations of the cipher|
|Differential|Study how input differences affect output|
|Integral|Exploit sums over sets of inputs (block ciphers)|
|Quantum|Use quantum algorithms (Shor/Grover) to break keys|
## Quantum Note
Quantum computing threatens classical public-key crypto (RSA/ECC via **Shor's algorithm**; halves symmetric strength via **Grover's**) → move to **Post-Quantum / quantum-resistant Cryptography (PQC)**.
---
# 171. Cryptography Tools & Countermeasures
## Tools
|Tool|Purpose|
|---|---|
|VeraCrypt / BitLocker|Disk encryption|
|GPG / PGP|Email/file encryption|
|OpenSSL|Crypto toolkit / certs|
|Hashcat / John|Hash cracking (audit)|
|CrypTool|Learning/analysis|
## Countermeasures
* Use strong, current algorithms (AES-256, SHA-256+, RSA-2048+/ECC)
* Never roll your own crypto
* Proper key management (rotation, HSM/KMS)
* Salt + slow hashes (bcrypt, scrypt, Argon2, PBKDF2) for passwords
* Enforce TLS 1.2/1.3, disable weak ciphers
* Perfect Forward Secrecy (PFS)
---
# 172. Blockchain Fundamentals
## What is Blockchain?
A **distributed ledger**: a chain of **blocks** linked with cryptographic hashes.
* Each block stores data + its own hash + the **previous block's hash**.
* Changing any block breaks the hash link in every later block → **tamper-evident**.
* Decentralized & consensus-driven (no single trusted authority).
## Core Properties
Decentralization · Immutability · Transparency · Consensus (PoW / PoS).
---
# 173. Blockchain Types & Attacks
## Types of Blockchain
|Type|Access|
|---|---|
|Public|Open to anyone (Bitcoin, Ethereum)|
|Private|Single org, permissioned|
|Federated / Consortium|Shared by a group of orgs|
|Hybrid|Mix of public + private|
## Blockchain Attacks
|Attack|Meaning|
|---|---|
|51% Attack|One party controls majority mining/hash power → rewrite transactions|
|Finney Attack|Pre-mine a block with a hidden transaction to double-spend|
|Eclipse Attack|Isolate a node from honest peers (feed it a fake view)|
|Race Attack|Exploit confirmation timing to double-spend|
|DeFi Sandwich Attack|Front-run + back-run a victim trade to profit from price movement|
---
# 174. Quantum Computing Attacks
## Why It Matters
Quantum algorithms threaten classical cryptography — especially **public-key** schemes.
* **Shor's algorithm** → breaks RSA/ECC (factoring / discrete log).
* **Grover's algorithm** → halves effective symmetric key strength (AES-128 → ~64-bit security).
* Defense direction: **Post-Quantum Cryptography (PQC)**.
## Quantum Attack Vocabulary (recognition)
Quantum cryptanalysis · quantum side-channel · classical-to-quantum transition · **harvest-now-decrypt-later** · quantum Trojan horse · quantum supply-chain · quantum-computer sabotage · fault-injection on quantum hardware · quantum DoS · quantum data eavesdropping · quantum bit-flipping · quantum error-correction exploitation · quantum replay.
#### High-yield: **harvest-now, decrypt-later** = capture encrypted data today, decrypt once quantum computers mature.
---
---
# 175. "Don't Confuse These" — High-Value Pairs
|Pair|Correct Distinction|
|---|---|
|Authentication vs Authorization|Who are you? vs What can you do?|
|Confidentiality vs Authentication|Prevent disclosure vs verify identity/source|
|Reconnaissance vs Scanning|Broad info gathering vs active host/service discovery|
|Scanning vs Enumeration|Find hosts/ports/services vs extract users/shares/details|
|Vulnerability Assessment vs Pen Test|Find weaknesses vs validate/exploit impact|
|IDS vs IPS|Detect/alert vs detect + actively block|
|NIDS vs HIDS|Network visibility vs host visibility|
|DoS vs DDoS|Single-source vs distributed availability attack|
|Reflection vs Amplification|3rd-party responder vs 3rd-party responder + traffic multiplication|
|Spoofing vs Hijacking|Impersonation vs taking over an existing session|
|Passive vs Active Sniffing|Observe vs manipulate/inject|
|Tailgating vs Piggybacking|Unauthorized following vs following with awareness/permission|
|Virus vs Worm vs Trojan|Host-based replication vs autonomous spread vs disguised delivery|
|Hashing vs Encryption|One-way digest vs reversible with key|
|Digital Certificate vs Digital Signature|Identity/public-key binding vs proof made with a private key|
|WEP vs WPA vs WPA2 vs WPA3|RC4/IV weakness vs TKIP vs AES-CCMP vs SAE|
|Black vs White vs Gray box|No knowledge vs full knowledge vs limited knowledge|
|LFI vs RFI|Include local file vs remote file|
|XSS vs CSRF|Script runs in victim's browser vs victim's browser forced to act|
|SSRF vs CSRF|**Server** makes attacker's request vs **victim browser** makes it|
|IDOR vs Auth Failure|Access another object's data vs failure to establish identity/session|
|Steganography vs Cryptography|Hide existence vs hide meaning|
|IaaS vs PaaS vs SaaS|Customer manages most (IaaS) → least infra (SaaS)|
|Association vs Authentication (Wi-Fi)|Connect to AP vs verify client identity|
---
# 176. Final Exam Priority Pass
## Tier 1 — Must Know 🔴
* Black/white/gray-box testing
* Nmap options + TCP flags + port states
* `nslookup` / `dig` / DNS zone transfer (AXFR)
* Enumeration commands (nbtstat, net view, SMTP VRFY/EXPN)
* CVE vs CVSS vs advisory
* SAM / `/etc/shadow` / LSASS / NTDS.dit
* Password attack categories (non-electronic / active / passive / offline)
* Malware components + delivery techniques
* Wireshark filters + Snort basics
* Social engineering techniques + psychological triggers
* Phlashing
* Session hijacking: track → desync → inject; sequence numbers
* IDS signature/anomaly/protocol + four alert types; NIDS vs HIDS
* Firewall types + evasion categories
* Web-server architecture/misconfiguration
* OWASP Top 10 (2021)
* SQLi types: error / UNION / Boolean / time / out-of-band
* Wireless auth modes + WEP/WPA/WPA2/WPA3 mechanisms
* Wireless threat categories + attack names
* Mobile attack surface + app store + sandbox + Android/iOS concepts
* Exact OWASP IoT Top 10
* Cloud actors + deployment/service models
* Cloud attacks: side-channel, wrapping, MITC
* Crypto: key size + block/stream classification
* PKI / CA / RA / VA / certificates / signatures
* Blockchain basics + 51% / Finney / Eclipse / Race / sandwich
* Cryptanalysis: linear / differential / integral / quantum
* Quantum attack vocabulary
## Tier 2 — Important 🟠
War dialing · ICMP Type 3/Code 13 · NetBIOS name codes · NTP/NFS/RPC/SMTP enumeration differences · steganography/steganalysis · overt/covert channels · SPAN / hardware analyzers · smishing details · IoT protocol/OS recognition · expanded cloud services (FaaS, IDaaS, SECaaS, FWaaS) · certificate fields / self-signed certs.
## Tier 3 — Recognition Only 🟢
Historical tools, long vendor/tool lists, niche wireless/IoT protocols, product-specific names — learn after Tier 1 & 2.
---
