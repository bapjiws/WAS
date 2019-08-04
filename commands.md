```wget --mirror –w 2 –p --adjust-extension –-convert-links –P localhost:3000```

```
wget --mirror --convert-links --adjust-extension --page-requisites --no-parent http://example.org
```
OR
```
wget -mkEpnp http://example.org
```
(Note that the last p is part of np (--no-parent) and hence you see p twice in the flags.)



- `mirror` – Makes (among other things) the download recursive.
- `convert-links` – convert all the links (also to stuff like CSS stylesheets) to relative, so it will be suitable for offline viewing.
- `adjust-extension` – Adds suitable extensions to filenames (html or css) depending on their content-type.
- `page-requisites` – Download things like CSS style-sheets and images required to properly display the page offline.
- `no-parent` – When recursing do not ascend to the parent directory. It useful for restricting the download to only a portion of the site.




```grep -E -o ".{0,1}path.{0,20}" *.js```

The -o switch tells grep to only show the match and -E to use an extended regular expression. Make sure to put the quotes around your expression, else it might be interpreted by the shell.
