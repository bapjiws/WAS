# Best practices
- [OWASP ASVS(Application Security Verification Standard)](https://www.owasp.org/index.php/Category:OWASP_Application_Security_Verification_Standard_Project)

# Nomenclature
- [Common Weakness Enumeration](https://cwe.mitre.org/)
- [OWASP Top Ten Project](https://www.owasp.org/index.php/Category:OWASP_Top_Ten_Project)

# Courses
- [ ] [Ethical Hacking Path](https://app.pluralsight.com/paths/skills/ethical-hacking-fundamentals)
  - [x] [Ethical Hacking: Hacking Web Applications](https://app.pluralsight.com/library/courses/ethical-hacking-web-applications)
  - [x] [Ethical Hacking: Hacking Web Servers](https://app.pluralsight.com/library/courses/ethical-hacking-web-servers)
  - [x] [Ethical Hacking: Reconnaissance/Footprinting](https://app.pluralsight.com/library/courses/ethical-hacking-reconnaissance-footprinting)
  - [x] [Ethical Hacking: Scanning Networks](https://app.pluralsight.com/library/courses/ethical-hacking-scanning-networks)
  - [x] [Ethical Hacking: Enumeration](https://app.pluralsight.com/library/courses/ethical-hacking-enumeration)
  - [x] [Ethical Hacking: Sniffing](https://app.pluralsight.com/library/courses/ethical-hacking-sniffing)
  - [ ] [Ethical Hacking: Denial of Service](https://app.pluralsight.com/library/courses/ethical-hacking-denial-service)
  - [x] [Ethical Hacking: Evading IDS, Firewalls, and Honeypots](https://app.pluralsight.com/library/courses/ethical-hacking-evading-ids-firewalls-honeypots)
  - [x] [Ethical Hacking: SQL Injection](https://app.pluralsight.com/library/courses/ethical-hacking-sql-injection)
  - [x] [Ethical Hacking: Session Hijacking](https://app.pluralsight.com/library/courses/ethical-hacking-session-hijacking/table-of-contents)
  - [x] [Ethical Hacking: Hacking Wireless Networks](https://app.pluralsight.com/library/courses/ethical-hacking-wireless-networks)
  - [x] [Ethical Hacking: Cryptography](https://app.pluralsight.com/library/courses/ethical-hacking-cryptography-ceh)
  - [ ] [Ethical Hacking: Penetration Testing](https://app.pluralsight.com/library/courses/ethical-hacking-penetration-testing) [WIP]

- [x] [Software Security, selected](https://www.coursera.org/learn/software-security/)
  - [x] [Week 3, Web Security](https://www.coursera.org/learn/software-security/home/week/3)
  - [x] [Week 6, Pen Testing](https://www.coursera.org/learn/software-security/home/week/6)

- [ ] [Bugcrowd University](https://www.bugcrowd.com/hackers/bugcrowd-university/)
  - [ ] [Bugcrowd University - Introduction + Become a Bug Bounty Hunter](https://www.youtube.com/watch?v=EZzAl-bfu7Q) [WIP]

- [ ] [Web Security Academy](https://portswigger.net/web-security)

- [ ] [Hacker101](https://www.hacker101.com/)
  - [ ] [Videos](https://www.hacker101.com/videos)
  - [ ] [Resources](https://www.hacker101.com/resources)
  
- [ ] [Penetration Testing and Ethical Hacking with Kali Linux](https://www.pluralsight.com/courses/kali-linux-penetration-testing-ethical-hacking) [WIP]

- [ ] [Full Ethical Hacking Course - Network Penetration Testing for Beginners (2019)](https://www.youtube.com/watch?v=3Kq1MIfTWCE)
  
# Sources
- [Bugcrowd forums](https://forum.bugcrowd.com/c/ask-a-hacker)
  
# Tools

## Reconnaissance
- Discovering IP space
  - [Hurricane Electric BGP Toolkit](https://bgp.he.net/) -- autonomous system number
  - [RIPE Database Text Search](https://apps.db.ripe.net/db-web-ui/#/fulltextsearch)
  - [American Registry for Internet Numbers](https://whois.arin.net/ui/query.do)
  - [Shodan](https://www.shodan.io/), search engine for Internet-connected devices

- Discovering New Targets (Brands & TLDs)
  - Acquisition
    - Wikipedia
    - [Crunchbase](https://www.crunchbase.com/) -- discover innovative companies and the people behind them
  - Linked discovery
    - Burp
  - Weighted link and reverse tracker analysis
    - BuiltWith (also below)
    - [DomLink](https://github.com/vysecurity/DomLink) -- a tool to link a domain with registered organisation names and emails, to other domains

- Subdomain enumeration (scraping)
  - [Amass](https://github.com/OWASP/Amass) -- in-depth attack surface mapping and asset discovery
  - [subfinder](https://github.com/subfinder/subfinder) --  a subdomain discovery tool that discovers valid subdomains for websites. Designed as a passive framework to be useful for bug bounties and safe for penetration testing

- Subdomain bruteforcing
  - [massdns](https://github.com/blechschmidt/massdns) -- a high-performance DNS stub resolver for bulk lookups and reconnaissance (subdomain enumeration)
  - [gobuster](https://github.com/OJ/gobuster) -- directory/file, DNS and VHost busting tool
  - [Commonspeak2 wordlists](https://github.com/assetnote/commonspeak2-wordlists) -- leverages publicly available datasets from Google BigQuery to generate content discovery and subdomain wordlists
  - [all wordlists from every DNS enumeration tool ever](https://gist.github.com/jhaddix/86a06c5dc309d08580a018c66354a056)

- Port scanning
  - [masscan](https://github.com/robertdavidgraham/masscan)
  - nmap (much slower)
  
- Credential bruteforcing
  - [BruteSpray](https://github.com/x90skysn3k/brutespray) -- brute-Forcing from nmap output - automatically attempts default creds on found services

- Visual identification
  - [EyeWitness](https://github.com/FortyNorthSecurity/EyeWitness) -- take screenshots of websites, RDP services, and open VNC servers, provide some server header info, and identify default credentials if possible

- Wayback enumeration
  - [waybackurls](https://github.com/tomnomnom/waybackurls) -- fetch all the URLs that the Wayback Machine knows about for a domain

- Platform identification and CVE searching
  - [Retire.js](https://retirejs.github.io/retire.js/)
  - [Wappalyzer](https://www.wappalyzer.com)
  - [BuiltWith](https://builtwith.com/)
  
- Parse source code
  - [LinkFinder](https://github.com/GerbenJavado/LinkFinder) -- a Python script that finds endpoints in JavaScript files
  - [JSParser](https://github.com/nahamsec/JSParser) -- parse relative URLs from JS files for discovering AJAX requests

- Content discovery / directory bruting
  - gobuster
  - directory brute-forcing lists
    - [RobotsDisallowed](https://github.com/danielmiessler/RobotsDisallowed)
    - [RAFT](https://github.com/danielmiessler/SecLists/tree/master/Discovery/Web-Content)
    - [jhaddix/content_discovery_all.txt](https://gist.github.com/jhaddix/b80ea67d85c13206125806f0828f4d10) -- RobotsDisallowed + RAFT
    - [SVN Digger](https://github.com/danielmiessler/SecLists/tree/master/Discovery/Web-Content/SVNDigger)

- Parameter bruting
  - (parameth)[https://github.com/maK-/parameth], a tool  to brute discover GET and POST parameters, can be paired with [params from backslash-powered-scanner](https://github.com/PortSwigger/backslash-powered-scanner/blob/master/resources/params)
  
- [Intrigue-core](https://github.com/intrigueio/intrigue-core), framework for external attack surface discovery and automated OSINT

- [The Exploit Database](https://www.exploit-db.com/) -- exploits, Shellcode, 0days, Remote Exploits, Local Exploits, Web Apps, Vulnerability Reports, Security Articles, Tutorials and more


## Meta infotmation
 - [ExifTool](https://www.sno.phy.queensu.ca/~phil/exiftool/), a program for reading, writing, and manipulating image, audio, video, and PDF metadata
 
## SSL analysis
 - [SSL Server Test (Powered by Qualys SSL Labs](https://www.ssllabs.com/ssltest/), online service performs a deep analysis of the configuration of any SSL web server on the public Internet


## Network analysis
- [Wireshark](https://www.wireshark.org/), network protocol analyzer
- [Nmap](https://nmap.org/), network discovery/security auditing/server fingerprinting (also see [Zenmap](https://nmap.org/zenmap/), a GUI for the Nmap Security Scanner)
- [Angry IP Scanner](https://angryip.org/), network scanner
- [hping3](https://tools.kali.org/information-gathering/hping3), TCP/IP packet assembler/analyzer
## Firewalking
- [Firewalk](https://tools.kali.org/information-gathering/firewalk)

## XSS
- [XSStrike](https://github.com/s0md3v/XSStrike) --  a Cross Site Scripting detection suite equipped with four hand written parsers, an intelligent payload generator, a powerful fuzzing engine and an incredibly fast crawler (in Kali)
- [XSS polyglots](https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/Polyglots/XSS-Polyglots.txt)
- [AwesomeXSS](https://github.com/s0md3v/AwesomeXSS), a collection of Awesome XSS resources
- [XSS Filter Evasion Cheat Sheet](https://www.owasp.org/index.php/XSS_Filter_Evasion_Cheat_Sheet)
- [Browser's XSS Filter Bypass Cheat Sheet](https://github.com/masatokinugawa/filterbypass/wiki/Browser's-XSS-Filter-Bypass-Cheat-Sheet)
- [HTML5 Security Cheatsheet](https://github.com/cure53/H5SC) + https://html5sec.org

- Blind XSS
  - [XSS hunter](https://xsshunter.com)
  - [ezXSS](https://github.com/ssl/ezXSS)
  - [bXSS](https://github.com/LewisArdern/bXSS)

## Server-Side Template Injection/Code Injection
- [tplmap](https://github.com/epinna/tplmap) -- Server-Side Template Injection and Code Injection Detection and Exploitation Tool


## SQLi
## CSRF
- [Multi-Staged/Multi-Form CSRF](http://blog.opensecurityresearch.com/2014/05/multi-stagedmulti-form-csrf.html)
## SSRF
- [jhaddix/cloud_metadata.txt](https://gist.github.com/jhaddix/78cece26c91c6263653f31ba453e273b) -- Cloud Metadata Dictionary useful for SSRF Testing
- [IP Address Converter](https://www.psyon.org/tools/ip_address_converter.php)
- [SSRF Bible cheatsheet](https://github.com/jivoi/offsec_pdfs/blob/master/SSRF-Bible-Cheatsheet.pdf)
## Command injection
- [commix](https://github.com/commixproject/commix) -- automated All-in-One OS command injection and exploitation tool

## Security misconfiguration
- Subdomain takeover
  - [Can I take over XYZ?](https://github.com/EdOverflow/can-i-take-over-xyz) -- a list of services and how to claim (sub)domains with dangling DNS records
  - [Knockpy](https://github.com/guelfoweb/knock) -- subdomain scan
  - [Certificate Search](crt.sh)
  - [SubOver](https://github.com/Ice3man543/SubOver)
  - [tko-subs](https://github.com/anshumanbh/tko-subs) -- A tool that can help detect and takeover subdomains with dead DNS records
- AWS
  - [S3Scanner](https://github.com/sa7mon/S3Scanner) -- a tool to find open S3 buckets and dump their contents
- GitHub
  - [Gitrob](https://github.com/michenriksen/gitrob) -- reconnaissance tool for GitHub organizations
  - [truffleHog](https://github.com/dxa4481/truffleHog) -- searches through Git repositories for high entropy strings and secrets, digging deep into commit history

## Misc
### Screenshots
- [Flameshot](https://flameshot.js.org)
- [CyberChef](https://gchq.github.io/CyberChef/) -- a swiss army knife providing all kinds of encoding/decoding tools



## Fuzzing
### LFI -- double-check
- [Liffy](https://github.com/hvqzao/liffy), Local File Inclusion Exploitation tool [OLD]
- [LFI-Jhaddix list](https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/LFI/LFI-Jhaddix.txt)


## Swiss-army-knife proxies
- [ ] Burp Suite [WIP]
  - [x] [Web Application Penetration Testing with Burp Suite](https://app.pluralsight.com/library/courses/web-application-penetration-testing-with-burp-suite)
  - [x] [Advanced Web Application Penetration Testing with Burp Suite](https://app.pluralsight.com/library/courses/advanced-web-application-penetration-testing-burp-suite)
  - [x] [Introduction to Burp Suite](https://www.bugcrowd.com/resources/webinars/introduction-to-burp-suite/)
  - [ ] [Self-Study Resources](https://portswigger.net/training#self-study)
  - [ ] [The Burp Methodology](https://support.portswigger.net/customer/portal/articles/2326039-the-burp-methodology)
- [ ] ZAP
  - [x] [Getting Started with OWASP Zed Attack Proxy (ZAP) for Web Application Penetration Testing](https://app.pluralsight.com/library/courses/owasp-zap-web-app-pentesting-getting-started) [WIP]
  - [ ] [How to Use Zap + using Zap HUD in your browser](https://www.bugcrowd.com/resources/webinars/how-to-use-zap-using-zap-hud-in-your-browser)
## Other tools
- [ ] [Common Vulnerabilities and Exposures](https://cve.mitre.org/)
## Fuzzing
- [SecLists](https://github.com/danielmiessler/SecLists)
- [fuzzdb](https://github.com/fuzzdb-project/fuzzdb)
- [PayloadsAllTheThings](https://github.com/swisskyrepo/PayloadsAllTheThings) -- A list of useful payloads and bypass for Web Application Security and Pentest/CTF

## Cheat Sheets
- [ ] [OWASP Cheat Sheet Series](https://cheatsheetseries.owasp.org/)


# Vulnerable web apps/CTFs
- [ ] Hacker101 CTF [WIP]
  - [ ] [Challenges](https://ctf.hacker101.com/ctf)
  - [ ] [Hacker101 CTF Writeup](https://github.com/testerting/hacker101-ctf)

- [ ] OWASP Juice Shop [WIP]
  - [ ] [Repo](https://github.com/bkimminich/juice-shop)
  - [ ] [Pwning OWASP Juice Shop](https://bkimminich.gitbooks.io/pwning-owasp-juice-shop/content/)
  - [ ] [Hacking(and automating!) the OWASP Juice Shop](https://incognitjoe.github.io/hacking-the-juice-shop.html)

- [x] BadStore.net
  - [x] [Quiz](https://www.coursera.org/learn/software-security/exam/Bn04I/badstore-quiz)
  - [x] [Manual](https://d28rh4a8wq0iu5.cloudfront.net/softwaresec/virtual_machine/BadStore_net_v2_1_Manual.pdf)
  - [x] [Pen-testing: Badstore v1.2.3 Walkthrough — Vulnhub](https://medium.com/syscall59/badstore-1-2-3-walkthrough-vulnhub-7816f3001333)
  - [x] [BadStore SQLi Writeup](https://armerj.github.io/SQLi-BadStore/)

- [ ] [bWAPP](http://www.itsecgames.com/)

- [ ] [Damn Vulnerable Web Application (DVWA)](http://www.dvwa.co.uk/)

# Books
- [ ] [Web Hacking 101](https://leanpub.com/web-hacking-101) [WIP]
- [ ] [The Ultimate Guide to Managed Bug Bounty](https://www.bugcrowd.com/resources/guides/the-ultimate-guide-to-managed-bug-bounty/#bcform)
- [ ] [The Web Application Hacker's Handbook](https://repo.zenk-security.com/Magazine%20E-book/The%20web%20application%20hackers%20handbook%20finding%20and%20exploiting%20security%20flaws%20-ed2%202011.pdf) -- see Web Security Academy
- [ ] [OWASP Testing Guide v4](https://www.owasp.org/images/1/19/OTGv4.pdf)
- [ ] [Breaking into Information Security: Learning the Ropes 101](https://kyhwana.keybase.pub/books/breaking%20into%20infosec%20.pdf)
- [ ] [Mastering Modern Web Penetration Testing](https://github.com/thecyberhex/books/blob/master/Mastering%20Modern%20Web%20Penetration%20Testing.pdf)
- [ ] [Kali Linux Revealed – Mastering the Penetration Testing Distribution](https://kali.training/downloads/Kali-Linux-Revealed-1st-edition.pdf) (or [the online course](https://kali.training/lessons/introduction/))

# Articles
- [ ] [Top 20 Data Reconnaissance and Intel Gathering Tools](https://securitytrails.com/blog/top-20-intel-tools)
- [ ] [Recon — my way.](https://medium.com/@ehsahil/recon-my-way-82b7e5f62e21)

# Reconnaissance -- flow and tools
- [ ] [GitHub for Bug Bounty Hunters](https://edoverflow.com/2017/github-for-bugbountyhunters/)
- [ ] [Pentester Land](https://pentester.land/)
  - [ ] [Conference notes: Practical recon techniques for bug hunters & pen testers](https://pentester.land/conference-notes/2018/10/17/levelup-2018-practical-recon-techniques-for-bug-hunters-and-pentesters.html)
  - [ ] [Conference notes: Esoteric subdomain enumeration techniques](https://pentester.land/conference-notes/2018/04/25/levelup-2017-Esoteric-subdomain-enumeration-techniques.html)
- [ ] [Offensive Approach to Hunt Bugs (Manual Bug Bounty Hunting)](https://www.youtube.com/watch?v=w5MZ6xdCci0)

# Bug hunting
## Presentations
- [x] [DEF CON 23 - Brent White - Hacking Web Apps](https://www.youtube.com/watch?v=I8AhfDEKUQ4)
- [x] [DEF CON 23 - Jason Haddix - How to Shot Web: Web and mobile hacking in 2015](https://www.youtube.com/watch?v=-FAjxUOKbdI)
- [x] [Bug Bounty Hunting Methodology v2 - Jason Haddix from Bugcrowd's LevelUp 2017](https://www.youtube.com/watch?v=C4ZHAdI8o1w&feature=youtu.be)
- [x] [The Bug Hunter's Methodology 2.0](https://www.youtube.com/watch?v=HI1mTQ7ovFY)
- [x] [LevelUp 0x02 - Bug Bounty Hunter Methodology v3](https://www.youtube.com/watch?v=Qw1nNPiH_Go)

## Resources
- [The Bug Hunters Methodology](https://github.com/jhaddix/tbhm)

# Penetration testing / vulnerability scanning tools
## Commercial
- [Metasploit](https://www.metasploit.com/), penetration testing framework
- [Nessus](https://www.tenable.com/products/nessus), vulnerability assessment
- [Acunetix,](https://www.acunetix.com/) website security scanner
- [Netsparker](https://www.netsparker.com/), web application security solution
## Free
- [Kali Linux Tools Listing](https://tools.kali.org/tools-listing)

# Conferences
- [DEF CON](https://www.defcon.org/)
