```
wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://example.org
```
OR
```
wget -mkEpnp http://example.org
```
(Note that the last p is part of np (--no-parent) and hence you see p twice in the flags.)


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

```nmap -sS -A -PN -p- --script=http-title dontscanme.bro```

(syn scan, OS + service fingerprint, no ping, all ports, http titles)
