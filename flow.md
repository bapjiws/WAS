- [ ] [Recon — my way.](https://medium.com/@ehsahil/recon-my-way-82b7e5f62e21)

- CVE
- Chrome plugins to find out the stack
- [XSS Filter Evasion Cheat Sheet](https://www.owasp.org/index.php/XSS_Filter_Evasion_Cheat_Sheet)


# Data Driven Assessment

1. Visit the search, registration, contact, password reset, and comment forms and hit them with your polyglot strings
2. Scan those specific functions with Burp’s built-in scanner
3. Check your cookie, log out, check cookie, log in, check cookie. Submit old cookie, see if access.
4. Perform user enumeration checks on login, registration, and password reset.
5. Do a reset and see if; the password comes plaintext, uses a URL based token, is predictable, can be used multiple times, or logs you in automatically
6. Find numeric account identifiers anywhere in URLs and rotate them for context change
7. Find the security-sensitive function(s) or files and see if vulnerable to non-auth browsing (idors), lower-auth browsing, CSRF, CSRF protection bypass, and see if they can be done over HTTP.
8. Directory brute for top short list on SecLists
9. Check upload functions for alternate file types that can execute code (xss or php/etc/etc)

# My flow
- subdomain scraping - sublist3r
  ```python sublist3r.py -d website.com```
- subomain bruteforcing - gobuster with list
  ```gobuster dns -d website.com -t 50 -w SecLists/Discovery/DNS/deepmagic.com-prefixes-top50000.txt```
  ```gobuster dns -d website.com -t 50 -w SecLists/Discovery/DNS/subdomains-top1million-110000.txt```
- port scanning - masscan/(Ze)nmap
- visual identification - Eyewitness
- directory bruteforcing/content discovery - gobuster with list
  ```gobuster dir -u website.com -l -t 50 -w SecLists/Discovery/Web-Content/SVNDigger/all.txt```
- parameter discovery
