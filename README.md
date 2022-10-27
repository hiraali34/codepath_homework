# Project 7 - WordPress Pen Testing

Time spent: 4 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pen Testing Report

### 1. Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds

- [ ] Summary: 
  - Vulnerability types: XSS (CVE-2017-6817)
  - Tested in version: 4.2 (affects versions 4.0 - 4.7.2)
  - Fixed in version: 4.2.13
- [ ] GIF Walkthrough: https://github.com/hiraali34/codepath_homework/blob/6947cc082e33e355991a2c128ac86452376bf0c4/youtube.gif
- [ ] Steps to recreate: 
- [ ] Sign in as an admin
- [ ] Create a new Post
- [ ] Switch from Visual editing mode to Text (HTML) editing mode
- [ ] Insert the malicious YouTube embed shortcode:
- [ ]   [embed src='https://www.youtube.com/embed/dQw4w9WgXcQ\x3csvg onload=alert("exploit!")\x3e'][/embed]
- [ ] Affected source code:
- [ ] https://core.trac.wordpress.org/browser/branches/4.2/src/wp-admin/admin-post.php
- [ ] Referneces:
- [ ]  https://wpscan.com/vulnerability/8768
- [ ]  https://blog.sucuri.net/2017/03/stored-xss-in-wordpress-core.html
  
### 2. Authenticated Stored Cross-Site Scripting (XSS)

- [ ] Summary: 
  - Vulnerability types: XSS (CVE-2015-5622 and CVE-2015-5623)
  - Tested in version: 4.2 (affects versions 4.0 - 4.2.2
  - Fixed in version: 4.2.3
- [ ] GIF Walkthrough: https://github.com/hiraali34/codepath_homework/blob/6947cc082e33e355991a2c128ac86452376bf0c4/XSS%20vulnerability.gif
- [ ] Steps to recreate:
- [ ] Sign in as an administrator
- [ ] Create a new Post
- [ ] Switch from Visual editing mode to Text (HTML) editing mode
- [ ] Insert the malicious a href code:
- [ ]   <a href="[caption code=">]</a><a title=" onmouseover=alert('exploit!') ">link</a>
- [ ] Affected source code:
- [ ] https://blog.knownsec.com/2015/09/wordpress-vulnerability-analysis-cve-2015-5714-cve-2015-5715/
- [ ] https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-5714
- [ ] https://wordpress.org/news/2015/09/wordpress-4-3-1/
- [ ] https://wpscan.com/vulnerability/8111
- [ ] https://blog.checkpoint.com/2015/09/15/finding-vulnerabilities-in-core-wordpress-a-bug-hunters-trilogy-part-iii-ultimatum/
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

### 3. Authenticated Stored Cross-Site Scripting (XSS) 

- [ ] Summary: 
  - Vulnerability types:  XSS (CVE-2015-5622)
  - Tested in version: 4.2.2
  - Fixed in version: 4.2.3
- [ ] GIF Walkthrough: https://github.com/hiraali34/codepath_homework/blob/edc6291d1a9feb1b0664127b97fca423eefb26ea/comment.gif
- [ ] Steps to recreate: Have version 4.2 installed
- [ ] Create a wordpress account and login
- [ ] Create/go to a post and add a comment that contains js:
- [ ]   <script>alert(document.cookie);</script>
- [ ]   When comment is added/page is refreshed, script will run on user visiting the page.
- [ ] Affected source code:
- [ ] https://wpscan.com/vulnerability/0f027d7d-674b-4a63-9603-25ea68069c1d
- [ ] https://twitter.com/klikkioy/status/624264122570526720
  - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)





## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with  ...
<!-- Recommended GIF Tools:
[Kap](https://getkap.co/) for macOS
[ScreenToGif](https://www.screentogif.com/) for Windows
[peek](https://github.com/phw/peek) for Linux. -->

## Notes

Chellenges:
This assignment had alot of chellenges from getting the wpdistillery started to finding vulnerability
the vulnerabilites i tried (3) of them it was easy to figure out through few searches but one of them that i wanted to do it took me 2 hours to do that one but i still could not figure it out (https://packetstormsecurity.com/files/131644/)

## License

    Copyright [2022] [Hira Ali]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
