```
// ==UserScript==
// @name        Use absolute ISO-style dates (YYYY-MM-DD HH:MM:SS) on sites using <relative-time>
// @description After loading document is searched for all relative-time tags and configured to use a readable, standard, language-independent format
// @namespace   Violentmonkey Scripts
// @match       *://*/*
// @grant       none
// @version     1.0
// @author      -
// ==/UserScript==
document.querySelectorAll('relative-time[datetime]').forEach(ele => { ele.setAttribute('format', 'datetime'); ele.setAttribute('lang', 'sv-SE'); ele.setAttribute('month', 'numeric'); ele.setAttribute('hour', '2-digit'); ele.setAttribute('minute', '2-digit'); ele.setAttribute('second', '2-digit'); ele.setAttribute('weekday', '') });
```
