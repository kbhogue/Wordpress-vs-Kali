# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required)  XSS in Embedded Youtube Videos
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: ![](https://github.com/kbhogue/Wordpress-vs-Kali/blob/master/gif1.gif)
  - [ ] Steps to recreate: Retrieve iframe embedded video link from Youtube. Add new post in Wordpress with the embedded video as the content. Add your XSS to the end of the main embedded video statement. I used onload=alert(123). The final post was <iframe width="560" height="315" src="https://www.youtube.com/embed/9SGHPQ2FVm8" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen onload=alert(123)></iframe>. Alert will pop up every time the video loads.
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) XSS in Page Comments
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2
  - [ ] GIF Walkthrough: ![](https://github.com/kbhogue/Wordpress-vs-Kali/blob/master/gif2.gif)
  - [ ] Steps to recreate: Go to the comments section of a published Wordpress page. Insert a XSS command. I used "<script>onload=alert(document.cookie);</script>" to make endless alerts pop up outputting the document cookies. 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) XSS at the End of an URL
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.5
  - [ ] GIF Walkthrough: ![](https://github.com/kbhogue/Wordpress-vs-Kali/blob/master/gif3.gif)
  - [ ] Steps to recreate: Create a new post and paste in a website URL. At the end, add your XSS command, with svg at the beginning. I used the following command: "<onload=alert(123)>". An alert will pop up every time the post loads. 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

- https://ithemes.com/2017/01/16/wordpress-security-issues/

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

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
