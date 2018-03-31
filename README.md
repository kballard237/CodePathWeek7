# Project 7 - WordPress Pentesting

Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability 2015-5622
  - [x] Summary: 
    - Vulnerability types: Authenticated Stored Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [x] GIF Walkthrough: ![link](https://github.com/kballard237/CodePathWeek7/blob/master/Authenticated_Stored_XSS.gif)
  - [x] Steps to recreate: 
    - Create a new post
    - In the body of the post insert <code>< a href="[caption code=">]</a >< a title=" onmouseover=alert('test')  " >link< /a></code>
    - Publish the post
    - Scroll over the link, and an alert should appear
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. (Required) Vulnerability 2015-5714
  - [x] Summary: 
    - Vulnerability types: Authenticated Shortcode Tags Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [x] GIF Walkthrough: ![link](https://github.com/kballard237/CodePathWeek7/blob/master/Authenticated_Shortcode_Tags_XSS.gif)
  - [x] Steps to recreate: 
    - Create a new post
    - In the body of the post insert <code>[caption width="8" caption='<a href="' ">]</a >< a href="http://onMouseOver='alert(1)'">Click me< /a></code>
    - Publish the post
    - Scroll over the link, and an alert should appear 
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. (Required) Vulnerability WPVDB ID 7979
  - [x] Summary: 
    - Vulnerability types: Unauthenticated Genericons Cross-Site Scripting (XSS)
    - Tested in version: 4.2
    - Fixed in version: 4.2.2
  - [x] GIF Walkthrough: ![link](https://github.com/kballard237/CodePathWeek7/blob/master/Unauthenticated_Genericons_XSS.gif)
  - [x] Steps to recreate: 
    - Go to the URL for genericons 
    - Insert the following at the end of the URL: <code><img/ src=1 onerror= alert(1)></code>
    - An alert should appear upon loading the page 
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

No additional scripts or files. 

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

In some cases, when I entered the code into the post body, it generated &lt;code&gt; tags. Therefore, the alerts were not appearing. I had to switch from visual to text mode to remove the tags and update the post. 

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
