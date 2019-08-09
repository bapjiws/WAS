First try polyglots, for exanple: https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/Polyglots/XSS-Polyglots.txt

[Using Burp with SQLMap](https://support.portswigger.net/customer/en/portal/articles/2791040-using-burp-with-sqlmap)

# Input Vectors for XSS
- Customizable Themes & Profiles via CSS
- Event or meeting names
- URI based
- Imported from a 3rd party (think Facebook integration)
- JSON POST Values (check returning content type)
- File Upload names
- Uploaded files (swf, HTML, ++)
- Custom Error pages
- fake params - ?realparam=1&foo=bar’+alert(/XSS/)+’
- Login and Forgot password forms


# Tactical Fuzzing - FI & Uploads
## Local file inclusion
Core Idea: Does it (or can it) interact with the server file system?

[Liffy] (https://github.com/rotlogix/liffy) is new and cool here but you can also use [Seclists] (https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/JHADDIX_LFI.txt):

## ￼￼Malicious File Upload
This is an important and common attack vector in this type of testing. A file upload functions need a lot of protections to be adequately secure.

Attacks:

Upload unexpected file format to achieve code exec (swf, html, php, php3, aspx, ++) Web shells or...
Execute XSS via same types of files. Images as well!
Attack the parser to DoS the site or XSS via storing payloads in metadata or file header
Bypass security zones and store malware on target site via file polyglots
File upload attacks are a whole presentation. Try this one to get a feel for bypass techniques:

content type spoofing
extension trickery
[File in the hole! presentaion] (https://www.nds.rub.de/media/attachments/files/2012/11/File-in-the-hole.pdf)
As referenced file polyglots can be used to store malware on servers! [See @dan_crowley ‘s talk] (http://goo.gl/pquXC2) [and @angealbertini research:] (corkami.com)

## Remote file includes and redirects
Look for any param with another web address in it. Same params from LFI can present here too.

Common blacklist bypasses:

escape "/" with "/" or “//” with “//”
try single "/" instead of "//"
remove http i.e. "continue=//google.com"
“//\” , “|/” , “/%09/”
encode, slashes
”./” CHANGE TO “..//”
”../” CHANGE TO “....//”
”/” CHANGE TO “//”
Redirections Common Parameters or Injection points￼:

dest=
continue=
redirect=
url= (or anything with “url” in it)
uri= (same as above)
window=
next=
RFI Common Parameters or Injection points:

File=
document=
Folder=
root=
Path=
pg=
style=
pdf=
template=
php_path=
doc=
