First try polyglots, for exanple: https://github.com/danielmiessler/SecLists/blob/master/Fuzzing/Polyglots/XSS-Polyglots.txt

# Probably temp stuff
Input Vectors for XSS:
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
