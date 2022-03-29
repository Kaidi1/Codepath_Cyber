# Project 7 - WordPress Pentesting

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

### 1. (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS or cross site scripting. 
    - Tested in version: 4.2
    - Fixed in version: 4.2.1
  - [X] GIF Walkthrough: 
    - ![GIF #1](https://user-images.githubusercontent.com/62517289/160701662-fd6ea029-be1d-4d4e-8f31-a869cce1dabd.gif)
  - [X] Steps to recreate:
    - First I opened the wpdistillery.vm website through the web browser. 
    - Then I posted a comment in the comment box with a comment in the format 
    - "\<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'>\</a>". 
    - This then was posted as a comment to the web page. 
    - The admin will get a notification about the comment. 
    - Once the admin clicks view page or view comment, the script will be run. 
    - This script can be used to do alot of malicious stuff. 
  - [X] Affected source code: 
    - [Link 1](https://wpscan.com/vulnerability/8051e64b-f73e-45ce-a853-02b8e425155b)
    - [Link 2](https://klikki.fi/wordpress-4-2-core-stored-xss/)
### 2. (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting via Image Filename
  - [X] Summary: 
    - Vulnerability types: XSS or cross site scripting.
    - Tested in version: 4.2
    - Fixed in version: 4.6.1
  - [X] GIF Walkthrough: 
    - ![GIF #2](https://user-images.githubusercontent.com/62517289/160707738-2134113d-4179-4773-90a5-6e8241e3f07e.gif)
  - [X] Steps to recreate: 
    - First I uploaded an image as "attachment page" to the media library. This image contains malicious html script that dumps out cookies.
    - Then this image is uploaded to the website. 
    - When a user clicks on an image the script will execute and display important data. 
  - [X] Affected source code:
    - [Link 1](https://wpscan.com/vulnerability/e84eaf3f-677a-465a-8f96-ea4cf074c980)
    - [Link 2](https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html)
### 3. (Required) WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [X] Summary: 
    - Vulnerability types: XSS or cross site scripting.
    - Tested in version: 4.2
    - Fixed in version: 4.2.3
  - [X] GIF Walkthrough: 
    - ![GIF #3](https://user-images.githubusercontent.com/62517289/160724861-3b547e62-b486-4265-843c-d190a40a0022.gif)

  - [X] Steps to recreate: 
    - First this has to be done by someone with an elevated privilage, possibly hacker got elevated privilage through CSRF.
    - Then I create a post with a link embedded inside the title of the post.
    - Then I can either choose to have an alert on mouse over the title(which is scary) or I can decide to have a user click on the title. 
    - The former will execute when the user simply hovers over the title, the latter will execute when user clicks on the title. 
  - [X] Affected source code:
    - [Link 1](https://wpscan.com/vulnerability/0f027d7d-674b-4a63-9603-25ea68069c1d)
    - [Link 2](https://klikki.fi/wordpress-core-stored-xss/)
### 4. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
### 5. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2022] [Kaidi Gao]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
