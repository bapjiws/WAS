```
wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://example.org
```
or
```
wget -mkEpnp http://example.org
```
- `--mirror`/`-m` – Turn on options suitable for mirroring. This option turns on recursion and time-stamping, sets infinite recursion depth and keeps FTP directory listings. It is currently equivalent to ‘-r -N -l inf --no-remove-listing’.
- `--convert-links`/`-k` – After the download is complete, convert the links in the document to make them suitable for local viewing. This affects not only the visible hyperlinks, but any part of the document that links to external content, such as embedded images, links to style sheets, hyperlinks to non-HTML content, etc.
- `--adjust-extension`/`-E` – If a file of type ‘application/xhtml+xml’ or ‘text/html’ is downloaded and the URL does not end with the regexp ‘\.[Hh][Tt][Mm][Ll]?’, this option will cause the suffix ‘.html’ to be appended to the local filename. This is useful, for instance, when you’re mirroring a remote site that uses ‘.asp’ pages, but you want the mirrored pages to be viewable on your stock Apache server. Another good use for this is when you’re downloading CGI-generated materials. A URL like ‘http://site.com/article.cgi?25’ will be saved as article.cgi?25.html.
- `--page-requisites`/`-p` – This option causes Wget to download all the files that are necessary to properly display a given HTML page. This includes such things as inlined images, sounds, and referenced stylesheets.
- `--no-parent`/`-np` – Do not ever ascend to the parent directory when retrieving recursively. This is a useful option, since it guarantees that only the files below a certain hierarchy will be downloaded.

---

```grep -r -E -o -i ".{0,1}path.{0,20}" *.js```

-o print only the matching string
-r (--recursive) recursively search for a pattern. This will search through all files in the specified directory, skipping the symlinks that are encountered recursively. To follow all symbolic links, use the -R option (or --dereference-recursive).
-E (--extended-regexp)
-i case insensitive search

Make sure to put the quotes around your expression, else it might be interpreted by the shell.

---

```nmap -sS -A -Pn -p- --script=http-title dontscanme.bro```

`-sS` (TCP SYN scan)
SYN scan is the default and most popular scan option for good reasons. It can be performed quickly, scanning thousands of ports per second on a fast network not hampered by restrictive firewalls. It is also relatively unobtrusive and stealthy since it never completes TCP connections. SYN scan works against any compliant TCP stack rather than depending on idiosyncrasies of specific platforms as Nmap's FIN/NULL/Xmas, Maimon and idle scans do. It also allows clear, reliable differentiation between the open, closed, and filtered states.

This technique is often referred to as half-open scanning, because you don't open a full TCP connection. You send a SYN packet, as if you are going to open a real connection and then wait for a response. A SYN/ACK indicates the port is listening (open), while a RST (reset) is indicative of a non-listener. If no response is received after several retransmissions, the port is marked as filtered. The port is also marked filtered if an ICMP unreachable error (type 3, code 0, 1, 2, 3, 9, 10, or 13) is received. The port is also considered open if a SYN packet (without the ACK flag) is received in response. This can be due to an extremely rare TCP feature known as a simultaneous open or split handshake connection (see https://nmap.org/misc/split-handshake.pdf).

`-A`
Detect OS and Services.

`-Pn`
Tells Nmap to skip the ping test and simply scan every target host provided. Other options for controlling host discovery are described in [Chapter 3, Host Discovery (“Ping Scanning”)](https://nmap.org/book/host-discovery.html).

`-p-`
Omit beginning and end numbers to scan the whole range (excluding zero).

`--script=http-title` / `--script http-title`
 Get the title of the web page from a web server.
 
 ```nc -z <IP> 20-500``` - port scanning with netcat
