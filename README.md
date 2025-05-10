### Use absolute ISO-style dates (YYYY-MM-DD HH:MM:SS) on sites which use the \<relative-time\> tag, with "git" in the URL like GitHub or Gitea

```
// ==UserScript==
// @name        Use absolute ISO-style dates (YYYY-MM-DD HH:MM:SS) on sites which use the <relative-time> tag, with "git" in the URL like GitHub or Gitea
// @description After loading, the document is searched for all <relative-time> tags and configured to use a readable, standard, language-independent format
// @namespace   https://github.com/t00/no-relative-date
// @match       *://*git*/*
// @grant       none
// @version     1.0
// @author      -
// ==/UserScript==
document.querySelectorAll('relative-time[datetime]').forEach(ele => {
  ele.setAttribute('format', 'datetime');
  ele.setAttribute('lang', 'sv-SE');
  ele.setAttribute('month', 'numeric');
  ele.setAttribute('hour', '2-digit');
  ele.setAttribute('minute', '2-digit');
  ele.setAttribute('second', '2-digit');
  ele.setAttribute('weekday', '');
});
```

### Use absolute ISO-style dates (YYYY-MM-DD HH:MM:SS) on all sites which use the \<relative-time\> tag

```
// ==UserScript==
// @name        Use absolute ISO-style dates (YYYY-MM-DD HH:MM:SS) on all sites which use the <relative-time> tag
// @description After loading, the document is searched for all <relative-time> tags and configured to use a readable, standard, language-independent format
// @namespace   https://github.com/t00/no-relative-date
// @match       *://*/*
// @grant       none
// @version     1.0
// @author      -
// ==/UserScript==
document.querySelectorAll('relative-time[datetime]').forEach(ele => {
  ele.setAttribute('format', 'datetime');
  ele.setAttribute('lang', 'sv-SE');
  ele.setAttribute('month', 'numeric');
  ele.setAttribute('hour', '2-digit');
  ele.setAttribute('minute', '2-digit');
  ele.setAttribute('second', '2-digit');
  ele.setAttribute('weekday', '');
});
```
