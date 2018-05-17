## Project 7 - WordPress Pentesting

Time spent: **15** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: Current versions of WordPress are vulnerable to a stored XSS. An unauthenticated attacker can inject JavaScript in WordPress comments. The script is triggered when the comment is viewed. If triggered by a logged-in administrator, under default settings the attacker can leverage the vulnerability to execute arbitrary code on the server via the plugin and theme editors. Alternatively the attacker could change the administrator’s password, create new administrator accounts, or do whatever else the currently logged-in administrator can do on the target system.  
    - Vulnerability types: XSS
    - Tested in version: 4.2, 4.1.2, 4.1.1, 3.9.3 
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: https://gph.is/2IgKfUu 
  - [ ] Steps to recreate: Reading the above vulnerabilty, this is how I went about it,
        1) I looked up the vulnerabilty in this website https://klikki.fi/adv/wordpress2.html
        2) I copied the code that shows the vulnerabilty for the XSS attack. 
            ***<a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;                height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>***
        3) I as a user injected the above code into the the comments section. In this scenerio I was the attacker. Injecting the code      
           above exploited the vulnerability. It displays a "Hello World" box whenever a user loads a page.
  - [ ] Affected source code:
     <textarea id="comment" name="comment" cols="45" rows="8" aria-describedby="form-allowed-tags" aria-required="true"      required="required" data-gramm="true" data-txt_gramm_id="bd582786-fe34-3cf3-2756-b92e2409e51c" data-gramm_id="bd582786-fe34-3cf3-2756-b92e2409e51c" spellcheck="false" data-gramm_editor="true" style="background: transparent none repeat scroll 0% 0% !important; z-index: auto; position: relative; line-height: 24px; font-size: 16px; transition: none 0s ease 0s;"></textarea>
     
2. FingePrinting Exposed Readme
  - [ ] Summary: A file exist exposing a version number.
    - Vulnerability types: This can be found in various versions of Wordpress
    - Tested in version: 4.2
    - Fixed in version: Can be fixed in any version. readme.html must be deleted whenever a user updates wordpress.
  - [ ] GIF Walkthrough: https://gph.is/2rTQcvF 
  - [ ] Steps to recreate: 1)visit wpdistillery.vm
                           2)In the url add /readme.html
  - [ ] Affected source code:vmdistillery.vm/readme.html
    
1. (Required) Vulnerability Name or ID
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

List any additional assets, such as scripts or files

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
